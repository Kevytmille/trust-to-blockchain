# X)

## Public key Cryptography

It all started in 1976 when Whitfield diffe and Martin Hellman described public-key cryptography and changed the field forever. The public key contains the instructions for encryption but only the person with the private key knows how to decrypt the message.

The following example is given in chapter 2.5 of Schneier 2015: Applied Cryptography:
This is how Alice can send a message to Bob using public-key cryptography:

(1) Alice and Bob agree on a public-key cryptosystem.

(2) Bob sends Alice his public key.

(3) Alice encrypts her message using Bob's public key and sends it to Bob.

(4) Bob decrypts Alice's message using his private key.

The same function, described above, works for public-key cryptosystems, but in that case nobody needs to send the public key to eachother. The public keys are stored in public database.

## Digital signatures

Digital signatures use the same principal but through a trusted arbitrator who helps to verify what all parties involed are to be trusted.
If there was no arbitrator how can Bob in the example know that the he is working for alice and not an imposter?

Alice enrypts her message to bob and sends the message to Trent (using a public key obtained from Trent).
Trent then decrypts the message with his private key match for Alice, and re-crypts the message with Bobs public key and sends it to Bob.
Bob decrypts the message with his private key and is now certain that the message is from Alice as this was verified by Trent.

If Bob wants to show Alices message to other people, he will need to go through Trent again to verify to the other people that the message came from Alice and that Bob is not just making it up.
Essentially mimicin the entire process but with Bob switched with the other people.

## Signing documents with public-key cryptography

With the help of public-key cryptography the above becomes a bit more hassle free. Alice and Bob simple need to give Trent their public keys for verification but otherwise:
Alice can simply encrypt the message with her private key and this proves it was signed by Alice
Bob can then decrypt the message with Alices public key, and now knows the it was indeed Alice who signed the document

The above requires Trent in the role of an arbitror who verifies that the public keys are obtained from the actual people involed, but Trent is not needed in the process at any point during the 
encrypting and decrypting of the message unlike above.

## Signing documents with public key cryptography and one-way hash functions

Alice can produce a one-way hash of a document she has, she encrypts the hash with her private key, which essentially confirms that she has signed the document
Bob can then either verify that Alice did sign the document or produce his own one-way hash and sign that, allowing for multiple signs
Carol can then verify the signatures alone without needing the other and Alice and Bob can sign the document in paralell or in series without affecting the validation.

## Digital signatures with encryption

If you really think about it, the smart thing would be to sign with one key and encrypt the message with another. This way you get security and validation. Without it, a dangerous person like Mallory could 
try to intercept Aliecs message to Bob, claim he sent it and in this way hope to be able to decrypt the orignal message with the help of Bobs.

To stop the attack you use a seperate key for the signature and in this way Bob would always know exactly who the message is orignally from. Alice just needs to sign the document with one key and encrypt it with another.
Since Bob is able to get Alices public keys from a trusted source like "Key Certification Authority or Key Distribution Center (KDC)". Mallory would need to get access to the KDC and change the public keys from Alice to his own to be able to fool Bob. Making the process much safer.

## Different levels of random

In the machine world there is no "true" random. Machines are deterministic and finite which means that a philosophical "true" random does not exist within them. But we can get close enough for it to be useful:
## Pseudo-random
It looks random. This means that it passes all the statistical tests of randomness that we can find.

## cryptographically secure pseudo-random
It is unpredictable. It must be computationally infeasible to predict what the next random bit will be, given complete knowledge of the algorithm or hardware generating the sequence and all of the previous bits in the stream.

## Real random: 
It cannot be reliably reproduced. If you run the sequence generator twice with the exact same input (at least as exact as humanly possible), you will get two completely unrelated random sequences.

# A)
Our internal ERP system sends information (WorkOrders, Invoices) over a VPN tunnel to the HQ SAP system. The VPN tunnel itself has been set up using public key exchange to verify that both parties can trust the other
and that the data moving between the two VPN points are encrypted. At the same time, the we are encrypting the messages sent with the SAP public key that they decrypt using their private key. 
(no source, just how i remember it being... i might be wrong on sooo many points)

# B)
I was able to follow Teros guide and create an encrypted message from Alice to my other user Mille, I followed Teros guide to the T. but here is a link to a word file with all the screenshot and short commentary:
https://github.com/Kevytmille/trust-to-blockchain/blob/main/H4-gpg.docx

I was unable to get it working the other way around, and i have some serious issues with copying the documents using the commandline and cp -v command, so i used the OS GUI like windows peasent IT-person i am... 

# C)
does using outlook with a message encryptiong count for this task?
Atleast the reference material found at: https://support.microsoft.com/en-us/office/encrypt-email-messages-373339cb-bf1a-4509-b296-802a39d801dc

lists that it using a public-key pair for the encryption. "Only the recipient who has the private key that matches the public key used to encrypt the message can decipher the message for reading."

So Microsoft is working like Trent (from the earlier material) as the arbitrer who handles who has access rights to the private key used to encrypt the message and what key is used depening on who you send the message to. This ofcourse requires you to validate yourself and to use Microsoft O365.

# D)
Eve is unable to eavesdrop on the converstaions between Bob and Alice as long as their private keys are kept private. Eve is able to intercept and copy the encrypted messaged between them, she is also able to get her
hands on both Alice and Bobs public keys. However without a private key, she is unable to decrypt the message and is only able to know the amount of messages Bob and Alice send to eachother and at what time. 

Mallory is able to fool Bob into helping him decrypt Alices message, this is explained in chapter 2.7 of Schneier 2015: Applied Cryptography. If Mallory can fool Bob into thinking he is Alice:
Mallory encrypts Alices message with his own private key and sends it to Bob
Bob will decrypt it with Mallorys public key and the message is gibberish, but if Bob then signs it with his own key and sends it back
Mallory can then decrypt it with his own private key, then re-encrypt it with Bobs private key, use his private key again to encrypt it and then finally encrypt it with Alies public key he will have access to alices message
Its hard to summarise, but the mathematical formula presnted in the chapter helps to understand this a bit better.

# F)

Not using a keypass system will most likely lead to over-use of the same password making multiple systems at risk if even one system is hacked. This makes you far less vulnerable to phising attacks.
We use keypass: https://keepass.info/ , as a centralized tool to store our work related internal password for different servers and systems that do not need or have personalized accounts for the daily work.

## Refered tasks from:
  https://terokarvinen.com/2023/trust-to-blockchain/


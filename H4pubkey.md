## X)

# Public key Cryptography

It all started in 1976 when Whitfield diffe and Martin Hellman described public-key cryptography and changed the field forever. The public key contains the instructions for encryption but only the person with the private key knows how to decrypt the message.

The following example is given in chapter 2.5 of Schneier 2015: Applied Cryptography:
This is how Alice can send a message to Bob using public-key cryptography:

(1) Alice and Bob agree on a public-key cryptosystem.

(2) Bob sends Alice his public key.

(3) Alice encrypts her message using Bob's public key and sends it to Bob.

(4) Bob decrypts Alice's message using his private key.

The same function, described above, works for public-key cryptosystems, but in that case nobody needs to send the public key to eachother. The public keys are stored in public database.

# Digital signatures

Digital signatures use the same principal but through a trusted arbitrator who helps to verify what all parties involed are to be trusted.
If there was no arbitrator how can Bob in the example know that the he is working for alice and not an imposter?

Alice enrypts her message to bob and sends the message to Trent (using a public key obtained from Trent).
Trent then decrypts the message with his private key match for Alice, and re-crypts the message with Bobs public key and sends it to Bob.
Bob decrypts the message with his private key and is now certain that the message is from Alice as this was verified by Trent.

If Bob wants to show Alices message to other people, he will need to go through Trent again to verify to the other people that the message came from Alice and that Bob is not just making it up.
Essentially mimicin the entire process but with Bob switched with the other people.

# Signing documents with public-key cryptography

With the help of public-key cryptography the above becomes a bit more hassle free. Alice and Bob simple need to give Trent their public keys for verification but otherwise:
Alice can simply encrypt the message with her private key and this proves it was signed by Alice
Bob can then decrypt the message with Alices public key, and now knows the it was indeed Alice who signed the document

The above requires Trent in the role of an arbitror who verifies that the public keys are obtained from the actual people involed, but Trent is not needed in the process at any point during the 
encrypting and decrypting of the message unlike above.

# Signing documents with public key cryptography and one-way hash functions

Alice can produce a one-way hash of a document she has, she encrypts the hash with her private key, which essentially confirms that she has signed the document
Bob can then either verify that Alice did sign the document or produce his own one-way hash and sign that, allowing for multiple signs
Carol can then verify the signatures alone without needing the other and Alice and Bob can sign the document in paralell or in series without affecting the validation.

# Digital signatures with encryption

If you really think about it, the smart thing would be to sign with one key and encrypt the message with another. This way you get security and validation. Without it, a dangerous person like Mallory could 
try to intercept Aliecs message to Bob, claim he sent it and in this way hope to be able to decrypt the orignal message with the help of Bobs.

To stop the attack you use a seperate key for the signature and in this way Bob would always know exactly who the message is orignally from. Alice just needs to sign the document with one key and encrypt it with another.
Since Bob is able to get Alices public keys from a trusted source like "Key Certification Authority or Key Distribution Center (KDC)". Mallory would need to get access to the KDC and change the public keys from Alice to his own to be able to fool Bob. Making the process much safer.

# Different levels of random

In the machine world there is no "true" random. Machines are deterministic and finite which means that a philosophical "true" random does not exist within them. But we can get close enough for it to be useful:
# Pseudo-random
It looks random. This means that it passes all the statistical tests of randomness that we can find.

# cryptographically secure pseudo-random
It is unpredictable. It must be computationally infeasible to predict what the next random bit will be, given complete knowledge of the algorithm or hardware generating the sequence and all of the previous bits in the stream.

# Real random: 
It cannot be reliably reproduced. If you run the sequence generator twice with the exact same input (at least as exact as humanly possible), you will get two completely unrelated random sequences.





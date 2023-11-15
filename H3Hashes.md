# Hashes

## X)
One-way function is an umberalla term for anything that is easy to do in one way and nearly impossible to do in reverse.

One-way Hash function is the central piece of modern cryptography that many of the current protocols lean on. It is a way to fingerprint your files by attaching a certain hash to it, if anything in the file changes
the has would also change, thus it becomes a reliable way of saying with an extremely likely accurace that if the hash matched what you expected. Then the file is also the one you want.


## A)
  after some minor trying i was unable to get a 0 at the start of the hash, but google is your friend and i found this: https://stackoverflow.com/questions/3180374/can-an-md5-hash-begin-with-a-zero 

##  B)
  Oh no! it changed!

## C)
  Token lenght exception

## D)
  Exausted

## E)
  Absolute rubbish, it had 3000+ hashrate in the earlier steps but now it dropped to 1943,6 kH/s

## M)
  Hyper-v only supports GPU Pass-through on certain GPU models, i am unable to complete this task :(

## N)
  cd827c33216d4e6e46bc60699f3e18a1 | mille , with a hashrate of 2311,6 kH/s

# ----------------------------------------------------------------------------------------------------

## late entry but after doing the evaluation of others i realized my mistake and im a bumbling idiot...

# C vol2)
  I managed to try on the correct hash this time (I had massive tehcnical issues and typed them by hand the last time...) 

  now it managed to crack it, and the hash was "admin"

# D vol2)
  After realizing that hashcat has different modes i got this working as well with -m 1000 and the hash was "monkey"

# E) 
  hashid '$2y$18$axMtQ4N8j/NQVItQJed9uORfsUK667RAWfycwFMtDBD6zAo1Se2eu' ( i realized you need to put it withing '' or you get a seperator error)

  gave me the options of Blowfish(openBSD), Woltlab runing board 4.x and bcrypt, i looked up the modes from: https://hashcat.net/wiki/doku.php?id=example_hashes
  https://github.com/Kevytmille/trust-to-blockchain/blob/main/Hashcat-pic1.PNG?raw=true

  and tried it with hashcat mode -3200 for blowfish, it seemd to be right one and after a minute or so it gave me the hash of "12345". However the hashrate was a stable 0 H/s


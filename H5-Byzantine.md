# X)
## Introduction
  Currently it is impossible to have a trusted exchange of “value” without a trusted exchange in the middle. This trusted exchange creates a necessary transaction fee in order to have the resources to validate and serve all the people exchanging value between them. Bitcoin aims to undo the needs for a trusted exchange by allowing the people to freely move value between them while the bitcoin cryptographic proof will serve as the trust that no data is falsified.
## Transactions
  A coin is defined as a chain of digital signatures. When you transfer a coin you digitally sign the coin and add the public key of the next owner. This creates a chain of ownership that if the chain includes all previous owners on a public chain. The chain be trusted that nobody used the same coin twice, or that a coin is fraudulent.
## Timestamp server
  A timestamp server acts by taking a hash of a block of items on the chain and timestamps them. This proves that the block existed at the time of the timestamp. Each timestamp includes the previous timestamps, thus creating a chain that verifies the trust of the full chain.
## Proof-of-work
  The proof-of-work involves scanning for a value that when hashed, the hash begins with the number of zero bits. As far as I can tell, the zero bits was chosen for “reasons” and it could be any other chosen amount of bits. The idea is that you need to do the “work” of finding the correct hash that meets the requirements of the proof-of-work. After you have expended your CPU on the task, it is impossible to change the block of your outcome without re-doing the block. As there are multiple blocks in the chain, you would also need to re-do all the work of the previous blocks. This creates a nearly impossible chain to break that functions as the trust in the chain. This method stops a bad actor from trying to overtake the chain as he would need do undo the work of the full chain before they would gain control of the current chain.
## Network
  The steps are:
  1) New transactions are broadcast to all nodes. 
  2) Each node collects new transactions into a block. 
  3) Each node works on finding a difficult proof-of-work for its block. 
  4) When a node finds a proof-of-work, it broadcasts the block to all nodes. 
  5) Nodes accept the block only if all transactions in it are valid and not already spent. 
  6) Nodes express their acceptance of the block by working on creating the next block in the chain, using the hash of the accepted block as the previous hash.
  The nodes always consider the longest chain to be correct, so if two nodes send out the same block. The nodes will wait which one becomes the longer and the block will be allocated to that node. At the same time the nodes are not required to be in prefect sync with each other. As long as many nodes have received the block, the rest will realize they missed a message and request it after they realize they are missing a block.
##  Incentive
  The incentive is that the first transaction in a new block starts a new coin that is given to the creator of the block. This works as the incentive to stay honest and keep the nodes running. The basic premise is the same as gold mining, but instead you are sacrificing your CPU time and power to generate and uphold the blockchain. Even without the possibility of new coins, a transaction fee can be imposed on the nodes that provide value to the CPU power used without the need for a trusted third party handling every transaction or inflation of

## A) and B)
  I was able to complete this task during the last lecture and sent 0.01mBTC to Tero
  https://github.com/Kevytmille/trust-to-blockchain/blob/main/electrum-working.PNG

## C)
  I asked for 0.01mBTC more from testnet faucet and tried sending them to Teros wallet listed on the webpage: https://terokarvinen.com/2023/trust-to-blockchain/

## D)
i looked at random a block from the block explorer: https://blockstream.info/block/0000000000000000000323449ea45ec3467b2c6ba9a9471d2de8a778cf8dd68f?expand
https://github.com/Kevytmille/trust-to-blockchain/blob/main/bitcoin-block-explorer.PNG
It lists various information about the block and i googled what the different attributes mean:
### Height
The current block height is simply the number of blocks in the blockchain minus one.
### Status
Self-explanatory, the current status of the block
### Timestamp
The timestamp when the block was discovered.
### Size
The actual size of the block in KB
### Virtual Size
Virtual size (vsize), also called virtual bytes (vbytes), are an alternative measurement, with one vbyte being equal to four weight units. That means the maximum block size measured in vsize is 1 million vbytes.
### Weight Units
Weight units are a measurement used to compare the size of different Bitcoin transactions to each other in proportion to the consensus-enforced maximum block size limit. Weight units are also used to measure the size of other block chain data, such as block headers. As of Bitcoin Core 0.13.0 (released August 2016)[1], each weight unit represents 1/4,000,000th of the maximum size of a block.
### Version
The block version number indicates which set of block validation rules to follow. However, I am unable to get a specific answer via google on what in this block does the 0x2c000004 actually mean.
### Merkle Root
The Merkle root is made up of all of the hashed transaction hashes within the transaction
### Bits
This 4-byte field contains the target difficulty of the current Bitcoin block which determines how difficult the target hash will be to find.
### Difficulty
The difficulty is a measure of how hard it is to mine a block. In order to mine a block, miners must provide Proof-of-Work in the form of a valid hash of the block they intend to publish.
### Nonce
Nonce, a portmanteau of "number used only once," is a random number that bitcoin miners try to find in order to mine a new block in the Bitcoin blockchain and receive a block reward for their efforts. The number is a critical element to the Bitcoin blockchain running smoothly.

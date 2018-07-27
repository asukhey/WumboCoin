# WumboCoin

## Objective:

To understand the working of transactions on a decentralized network using blockchain with the help of cryptocurrency created. After reading about bitcoin, I was more interested in creating a cryptocurrency similar to that rather than investing in one ,P.S. Also it values at 7869.31 USD (dated 7/27/2018) , I don't have that much money.

## Introduction:

WumboCoin (Thanks to Patrick Star from Spongebob Squarepants) is a cryptocurrency I created to understand working of cryptocurrency transactions on a decentralized network using blockchain technology pragmatically. Blockchain is defined as a chain of blocks linked to each other where each block is hashed using SHA-256. Reason why SHA-256 is used cause it follows "Avalanche effect"- A slight change in the text will render a completely different hash code from first to 64th HEX value.

### In this project, block has following important properties:

#### i. Index Number
Determines where's the block situated in the blockchain

#### ii. Previous Hash
Holds the SHA-256 encoded hash of the block before. Also confirms that it is linked to the block before.

#### iii. Nonce
Number used only once (Nonce) is the only property that can be altered by the user to get a respective hash number below target hash (We'll get to that in the Mining section).

#### iv. Timestamp
Tells when the block was created, this is an important property of a block.

#### v. Data
In this case all the transactions made i.e sender, reciever and amount.

### Hash Number

Using the properties above generates a 64 hexadecimal hash number using 256 bit Secure Hashing Algorithm (SHA-256). 
**Target Hash** is a hash set by software and a block mush have hash number less than that. In this case To mine a block, hash should have starting 4 Hex digits as 0.

### Mining

The process is mining a block is to generate a hash code that is less than target hash - Hash generated by the software of a respective cryptocurrency. The properties of a block compose a hash code. Nonce is the only property that can be changed by the user and with that number ranging from 1 to 4 billion. There are 4 billion possible hash numbers that can be generated. Mining takes place with multiple systems (miners) connected in a decentralized network where each node has a copy of blockchain which is updated from time to time. Miner that generates the least possible hash value mines a block and gets rewarded for it.

## Practical Implementation

#### i. Block Initialization
I've currently tested the program in postman and have used three consoles as miners using Spyder IDE. Ports 5001,5002 and 5003 are miners and have initialized blocks in blockchain as mentioned below. The first block is defined as **genesis block**. Since it has no block before it, previous hash is set to 0.

![alt text](https://github.com/asukhey/WumboCoin/blob/master/Snaps/1_block_initialize.PNG "Block Initialization")


#### ii. Mine Block
This is a process of creating a block with hash number less than the target hash in hexadecimal format. The rule in the cryptocurrency is to ensure that atleast 4 digits in the start must be 0. Node with the least hex value mines the block and gets rewarded.

![alt text](https://github.com/asukhey/WumboCoin/blob/master/Snaps/2_mine_block.PNG "Mining Block")

#### iii. Connecting nodes
It is a post method that implements decentralized connection of various miners. In this case it's simply 3 separate consoles in Spyder IDE.

![alt text](https://github.com/asukhey/WumboCoin/blob/master/Snaps/3_connect_nodes.PNG "Blockchain Synchronization")

#### iv. Check if the blockchain in all nodes are synchronized
Each node has a blockchain attached to it and it is important to make sure that the number of nodes as well as it's contents are equal, when a block is mined, the blockchain is updated not only with the node that mined it but with other nodes in a network as well, Using a blockchain with more number of nodes.

![alt text](https://github.com/asukhey/WumboCoin/blob/master/Snaps/4_equalizing_blockchain.PNG "Blockchain Synchronization")

**I'll be studying about smart contracts and will update readMe asap**



 *Shoutout to my bud and a fellow spongebob fan Prerna Kapoor for suggesting the cryptocurrency name*

---
layout:     post
title:      Cryptocurrency explained
date:       2019-10-05 12:31:19
summary:    Understanding why were cryptocurrencies created and how bitcoin works. 
categories: blockchain
tags: [Blockchain]
comment: true

---


<!-- # cryptocurrency explained.  -->

Over the past few days I have been going through various blogs, research papers, youtube videos, books to read and gain knowledge about Cryptocurrency, which has been a pretty talked about topic recently. Unless you have been living under a rock, it is highly unlikely that you have never heard of _(bitcoin, blockchain, ethereum, mining)_ before. Through this post, I will try to explain how these technologies/currencies work and why were they created, and how can they change the way we do transactions now. 

To understand this Digital Currency, let us understand, how currency works and has been working so far. 
Initially, we had [barter](https://en.wikipedia.org/wiki/Barter) system, which was replaced by money mainly because exchange is not always convenient and efficient. 
Due to this, currency started to mint. The exchange problems were solved and this system was largely based on trust. The kings used to have their [royal seal](https://en.wikipedia.org/wiki/Alyattes_of_Lydia) on the coin signifying that this currency is valid. However forgery was very common as making a coin and copying the seal was not that a difficult task, but still way much better than Barter. 
With time, the gold coins transformed into paper money, which was widely circulated across the world by [explorers](https://en.wikisource.org/wiki/The_Travels_of_Marco_Polo/Book_2/Chapter_24). Trade flourished across countries through this paper money, and exchange of currency started around that time too, and by around 1860, Western Union, spearheaded e-money with electronic func transfer via telegram. With time cards came, and with the rise of internet the e-money started to boom. 
The reason, why I am focussing on the history of currency, is because I want you to understand what is common between all these systems of currency. From exchanging coins with royal seals, to exchanging paper currency, with issuance from bank/government, to starting e-money (banks giving cards). If you try to find the pattern, you will see that all of these currencies are **Centralized**.

By centralized, what I mean is that everytime there is an authority that is responsible for issuing the currency. Someone who says that, Yes, I am accountable for this currency and this currency is valid. Be it a king, who imprints the coin with its royal seal, or the government. The transactions have always been based on **Trust**. If I pay ₹100 to X, the bank issuing the currency is responsible to pay that ₹100 to X. Hence the currency so far being used is based on Trust, and is Centralized. Due to this we are always bound to law, cannot be innovative and creative with our money, always under control and at a risk of interference. Also, the banks would charge some amount for transactions as _transaction fee_. The point to be noted is that, crypto currency is not flawless, so it just provides as an alternative currency as of now. Due to all this, a currency was needed which was not based on trust, and is not centralized. 
> `Cryptocurrency is a decentralized trustless verification system + Math.`

Now, one thing I would like to mention here is that just like normal currency, you need not know how cryptocurrency is made or how it works to use it. Diving into the technical details, let us understand everything with an example.


Say there are 4 friends A, B, C and D who hang out pretty often, and hence they need a system to keep track of money. What they do is, they keep a ledger and add all the transactions in it. At the end of the month they take all the transactions and then total it up and settle it and pay accordingly.


```
* ledger *
A gives B 200 rupees
B gives C 500 rupees
C gives A 1000 rupees
D gives B 300 rupees
..............and so on
```

The catch here is that the ledger is accessible to all four of them, i.e anyone can add or delete the transactions. D might just add that, `C gives D 500 rupees`, as there is no one stopping D. He can keep on adding fraudulent transactions until someone catches him, and resolve this. So, what we need is a system to verify that the correct person is writing the ledger. The solution to this is *Digital Signatures*. 

Before I start with explaining what Digital Signatures are, I would like to mention Cryptographic Hashing. Hashing is a method that converts any form of data in a unique string of text. Typically the output of every hash function is a fixed length of string. Now what cryptographic hash functions are, are hash functions which cannot be reversed. 
So cryptographic hash functions will take any input, no matter how big or small, and output a fixed length of string which is irreversible. It is practically impossible to determine what input caused that hash except hit and trial. Now coming to digital signatures, these are used to verify the identity of the person signing a message. Through digital signatures we can be sure that the person signing the message is actually the person writing the message. It mainly consists of _private key and public key._ Private key can be thought of your PIN card and public key as your A/C number. You keep the private key with yourself, but can give everyone your public key. Now to make a transaction, you write a message and encrypt that with your private key. And you send the hash message to the receiver. The receiver would see the hashed message, and verify if it was sent by you using the public key. The cryptographic hash function used is mainly SHA-256. The bit string generated is 256 digits long, i.e there can be 2<sup>256</sup> combinations. 2 <sup>256</sup> is an extremely large large number. 


![](/images/bitcoin2.png)

The functions would look something like this: 

```
dig_sign(message, private key) -> signature

verify(message, signature, public key) -> true/false

```


Now that you have a fair idea of how digital signatures work, we can go back to the example. D can no longer write any fraudulent transactions in the ledger as they all will be from now on digitally signed. The verification system apart from checking if the message was signed from the trusted party or not, it also checks if the party sending the money actually has it or not. 


The problem with this solution is that the fate of the entire money system depends on the company running the mint, with every transaction having to go through them, just like a bank. We need a way for the payee to know that the previous owners did not sign any earlier transactions.

One thing which you might have noticed, is that this system of ledger that I just explained is centralized as well, which I had focussed on earlier. We have found a way to secure the transactions but there is only one ledger, and everyone is making transactions in their own ledger. As I had mentioned earlier, the cryptocurrency is decentralized. To make this currency decentralized, we will give one copy of the ledger to all four friends (A B C and D). Now this ledger becomes a decentralized currency.


So now, all have personal copies of the ledger, and now adding the transaction has become a different process. Like they can still add the transaction in their personal ledger, but it wont match with the ledger of someone else. Say, B adds `B gave ₹5000 to C` to his ledger, but that information wont be added on the ledger of A or C or D. To have all the ledgers on the same track, one must broadcast their ledger so that everyone in the network updates their ledgers with the most recent transactions. So, B would update its ledger, and then broadcast his ledger so that everyone verifies the transaction and update their ledgers as well. Hence through this example, we have made a trustless decentralized verification system.


A big problem with this system is that, what if D broadcasts that he has sent 500 rupees to A, and at the same time, it broadcasts that he has sent 500 rupees to B. This is how D can double spend his money. This problem has been address in the original [Bitcoin Paper](https://bitcoin.org/bitcoin.pdf). 


The bitcoin paper mainly said to trust the block/ledger with the most computational work being done _(proof of work)_. This ledger is mainly the blockchain. The below diagram will help you understand the chain structure of the ledger.

![](/images/bitcoin1.png) 

The proof of work involves scanning for a value that when hashed, such as with SHA-256 the hash begins with a number of `n zero bits`. 
For our network, we implement the proof of work by incrementing a nonce in the block until a value is found that gives the blocks hash the required zero bits. Finding this number is called *mining*, and the people who do this are called *miners*. The paper also said to trust that chain with the most number of nodes, hence while updating their ledger, they also keep track of all other chains, and then eliminate the smaller chains as miners start working on the longest chain. 
Proof-of-work is essentially one-CPU-one-vote. The majority decision is represented by the longest chain, which has the greatest proof-of-work effort invested in it. If a majority of CPU power is controlled by honest nodes, the honest chain will grow the fastest and outpace any competing chains. To modify a past block, an attacker would have to redo the proof-of-work of the block and all blocks after it and then catch up with and surpass the work of the honest nodes the number of zeros vary a lot. What the miner gets in return is a block reward. With every block added to the network, the total amount of money increases in the economy, as there is no one issuing the block reward. Hence through this proof of work, it is nearly impossible to create fraudulent transactions. This miniature lottery is such that there is one winner every 10 minutes (in case of  bitcoin). This time may change for other cryptocurrencies.  


We can understand the whole network through these steps


The steps to run the network are as follows:

1. New transactions are broadcast to all nodes.
2. Each node collects new transactions into a block.
3. Each node works on finding a difficult proof-of-work for its block.
4. When a node finds a proof-of-work, it broadcasts the block to all nodes.
5. Nodes accept the block only if all transactions in it are valid and not already spent.
6. Nodes express their acceptance of the block by working on creating the next block in the chain, using the hash of the accepted block as the previous hash. Nodes always consider the longest chain to be the correct one and will keep working on extending it. If two nodes broadcast different versions of the next block simultaneously, some nodes may receive one or the other first. In that case, they work on the first one they received, but save the other branch in case it becomes longer. The tie will be broken when the next proof of work is found and one branch becomes longer; the nodes that were working on the other branch will then switch to the longer one.



Through this post, I hope you have a fair idea of how cryptocurrencies work. 
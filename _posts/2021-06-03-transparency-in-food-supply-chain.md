---
layout:     post
title:      Restoring trust in food through Blockchain (In Progress 🚧)
date:       2021-06-03 11:21:29
summary:    transparency and traceability.
categories: blockchain
tags: [hyperledger, project]
comment: true
---

If I go to my nearest grocery store to purchase vegetables or fruits, the only proof of it being fresh are the claims made by the seller/vendor. They even put messages over the racks which tell the consumer that every vegetable they have is free from any harmful chemicals, and are 💯% fresh. The problem I noticed with this is that these claims are almost never true, and establishing trust amongst the consumer becomes an issue. The end consumer has to rely on how fresh and juicy the fruit looks, but again all that glitters is not gold.

On discussion with some local farmers around Delhi-NCR, it was found that 70% of the produce that they grow, use very harmful chemicals and water being used for growing the crops literally comes from the drain. When they try exporting the produce, the produce never passes the stringent quality checks and are rejected due to very low nutritional values. That produce is dumped to the mandis and end up in our plates. Due to such malpractices of using harmful fertilisers and poor quality water in growing the crops, the farmers are able to fill the plates of the consumer, but at what cost? *Just to mention*, the crops that they grow for their personal use is actually very different in terms of nutritional value from the ones they dump in the market. Some farmers even have some part of their land reserver for crops to be consumed by their family. 

Removing all the malpractices in the food supply chain is something that is not really achievable, but what is achievable is to provide the end consumer *transparency*. Allowing them to trace where their food comes from, and what all goes into their plates. By making the consumer more informed, they can make better decisions on what to eat and not to eat. In this post, I will be talking about how we can use blockchain to create trust amongst the consumer and the farmers, and how consumers can just trust the network and not what the vendor or the message on the racks say.

If we capture the journey of the food, from seed to plate and show it to the end consumer, it can eventually help the consumer make well informed decisions about what they wish to buy. We could have used a central database for this, which would be updated whenever the farmer does a task. But again, how would that be different from the vendor telling the consumers that the produce is 100% fresh. We needed something that is immutable. Here comes blockchain into picture. I am pretty sure you must be familiar with what blockchain is, if not you can read the underlying concepts [here](https://vaibhavahuja.github.io/blockchain/understanding-bitcoin). In short, blockchain is a digital ledger of transactions which is duplicated and distributed across the entire network, thus making it immutable. This means, that once something is written on the network, no one can change it, not even us! Bitcoin and Ethereum are the two most famous and biggest blockchain networks available. Ethereum provides us with the option of developing Decentralized Applications (dapps) on the network, however they are public networks. Public network, means that anyone in this world can see all the transactions which are made on the network, which is something we would not want in our network, since we wish it to be somewhat private. Also, the process of adding new blocks to the network is through mining. Mining is a process where a large number of machines race to solve a computationally expensive mathematical problem in order to get a reward. This consensus algorithm (Proof of work) is great when there is no trust amongst the different stakeholders of the network (which is true in a public network), but in our case, the stakeholders do have some trust amongst each other, and we wish to have faster times of getting a transaction validated. We also wish participants to not interact anonymously, which is not true in the case of public blockchain networks.

Keeping the above points in picture, using Hyperledger Fabric was the best choice. Hyperledger Fabric is an open source enterprise-grade permissioned distributed ledger technology (DLT) platform, designed for use in enterprise contexts, that delivers some key differentiating capabilities over other popular distributed ledger or blockchain platforms. The best thing is that it is open source.

--- to be continued....

Things to add : 
- How database works in HLF
- State Transition Diagram
![](../images/foodBlockchain1.png)
- Your database (world state) (what would be in the blockchain)
- How the transactions were recorded



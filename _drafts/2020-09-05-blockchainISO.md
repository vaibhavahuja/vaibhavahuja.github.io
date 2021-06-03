---
layout:    post
title:      A Blockchain Alternative for Storing Individual Insurance Claim Data
date:       2020-08-10 00:00:00
summary:    sharing claims data between different insurers.
categories: project
tags: [project, Blockchain]
comment: true

green: "#d5e9dd"
red: "#ddafb6"
yellow: "#FCF4A3"
---

In this post, I will be talking about a blockchain solution for storing Individual Insurance Claim Data. I will be explaining why storing the claim data is needed, how it is being done right now and why do we need a blockchain alternative. After this, I will be diving deep in the proposed blockchain solution and will demonstrate a sample network. 


The insurance industry in the United States is the largest in the world in terms of revenue. It is a trillion dollar industry and with that much money involved, the insurers need to prevent fraud and evaluate risk while processing claims. A single person might have multiple insurance contracts with multiple insurers, and while processing a claim, it gets important for the insurers to check all the recent claim data of an individual, to detect and prevent fraud.
The individual insurance claim data helps insurers, self insurers, law enforcement agencies, and state fraud bureaus detect and prevent fraud, evaluate risk, and process meritorious claims.

Currently, all of this data is being provided by all the *participating insurers* to a private company whch in turn stores everything in a **single database** and lets the insurers search for their data at a cost. Using this data, every company can protect itself against paying questionable or possibly fraudulent claims. The insurers research prior loss histories, identify claim patterns, and try to detect fraudulent claims. In a nutshell, this data is important for an analyst to investigate on a particular case, by providing them more information which was very difficult to retrieve otherwise. This database has over 1 billion claims, mainly property and casualty claims. The participating insurers give the claim data to the *private company*, the company stores them in the database, and lets the insurers query this data for a cost. When a insurer requests the claim data, it is processed and matched against million of other claims and if the system finds a *match*, a report is returned to help identify claim patterns which might indicate suspicious activity or *duplicate coverage*. Due to this data, the insurers can identify whether the claimant has had a claims history or has filed duplicate claims across multiple lines of insurance. The thoroughness of a database search depends on the timely reporting, accuracy and extent of information furnished. What is the problem with this system? Everything looks fine, it is a win win situation for the insurers and for the private company that is providing this storage service. The problem is that the *private company* is an Intermediary. 

All the claims data is stored with that intermediary in one single database. There are a lot of problems with this thing. All insurers will have to be dependent on the intermediary *forever* for their data and will have to trust the intermediary on any data, since all the data is stored in *one* central location. There is a high cost for getting the data. In the end, all insurers are sharing the data which should be at a very minimal cost. Storing everything at one place poses a higher risk of systematic failure. Also, getting data from a central database is a very slow process. (takes around 2-3 days for getting the matched claims). While this helps insurers expand their knowledge and improve accuracy, the process is expensive, due to non-standardized fee structure and the need to develop numerous partnerships to gain access to third-party data. 

Having everything centralized is not good for the insurance industry, and the industry can highly benefit by eliminating intermediaries. Eliminating intermediaries and achieving trust between the parties(on the data) is what we need, and here comes **Blockchain** in the picture. Blockchain can be characterized by the following : 

1. Decentralized Data
1. Mutual consensus by Participants
1. Digital Signatures and identity verification
1. Direct, Secure and immediate access to data. 

As blockchain gains traction, the insurance industry will draw benefits from this game-changing technology platform. Insurance Carriers that build these capabilities will be better positioned to price policies competitively and increase revenue. The adoption of blockchain would generate data from a single true source which would be far more cost-effective for insurers. The blockchain technology has a high potential in this sector, and through this solution the insurance industries can access larger data, access complete information and share claim information with other insurers in a simple way. Collaborating with other service providers and sharing claim information is cost effective and fast. It will accelerate the investigation. Through this, the claim status can be shared with the agents/brokers, and customers effectively. Blockchain's innate immutability and distributed ledger promise greater data integerity and a single version of truth.

Blockchain is a nascent technology as standards/platforms are still emerging. The hype is ahead of development; it will take time for the technology to mature, become cost-effectivefor mass adoption, and more importantly, to be tested under real-world adversarial condi-tions Blockchain could be an enabler and catalyst to accelerate digitisation, shift the mindset towards change and transformaton and foster further innovation. Below I will be talking about this blockchain solution that I have created. 

Will implement it in hyperledger.

// to continue this
// to finish this by january.
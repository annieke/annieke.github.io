---
layout: post
title: "Explaining Crypto Through Bitcoin"
categories: [explanations]
tags: [crypto, tech, united states]
---

My opinion on the future of crypto changes about twice a quarter, ranging from half-ironically giving investment advice at parties to "maybe everything is fake in this industry but at least the code is cool." Either way, the code IS cool. Though no one knows what will happen, the future of cryptocurrencies is determined by its builders and users. I want to share my enthusiasm, so more people can become crypto builders and users who propel the ponzi scheme and its benefits.

<!--more-->

Bitcoin is the granddaddy of cryptocurrencies, so it's hard to discuss the rest without understanding Bitcoin. Though Bitcoin wasn't the first attempt at a decentralized currency, it is the first one that's used and traded for value. Its [whitepaper](https://bitcoin.org/bitcoin.pdf) blew my mind. A few themes stuck out especially.

### Decentralization

The favorite buzzword of crypto. Its concept wasn't meaningful to me until this diagram:

![centralized vs decentralized vs distributed](https://i.stack.imgur.com/4IF1r.png)

The left would be our banking and payments systems today. Though you can venmo anyone with an account, you're out of luck if you don't have access to that centralized server managed by Venmo the company/PayPal. 

The middle is the Bitcoin network. Every center of connection is a **node**: they connect to each other, sync a copy of all the transactions to ever happen (the "blockchain" or **ledger**), open their ports to you to submit transactions, and other complicated shit. The network can't ban anyone specific, since if one node bans someone from submitting transactions, another node can still accept it. There are ~10k full nodes on the Bitcoin network as of today, so it's difficult to make them agree on a blacklist, a feat Greek houses with <200 members sometimes can't accomplish. Decentralization thus makes the Bitcoin network *uncensorable*. Transactions, partly due to decentralization, are also *irreversible*, as reversing the transaction on one ledger isn't enough -- all ~10k of them would need to be reversed.

The right looks cool but idk what to do with it. 

### Truth-keeping

This is the most technical section. If you don't have the appetite for [cryptographic hashes](https://en.wikipedia.org/wiki/Cryptographic_hash_function), the takeaway is that Bitcoin pioneered a way to get all those nodes to agree on ONE (1) history of transactions through using computing power to vote. If you want to be lightly tortured with stimulating concepts, continue.

The task of keeping those 10k-ish ledgers in sync is crucial to making bitcoin usable as a currency. If all those nodes keep different copies of transactions, then we might as well have a centralized network at each node. This task is logistically difficult. With modern networking, nodes can propagate transactions quickly, but different transactions are submitted to different nodes and the ledger will quickly go out of sync, if they just accept by order of receiving. 

What if we added timestamps to the transactions? This makes ordering transactions easier, but nothing stops a node from erasing its own transactions to keep its own bitcoin. If every node starts doing this, we end up with a broken network again. There needs to be a way for nodes to agree on one ledger. 

Introducing the **blockchain** and **proof of work**. The blockchain is made up batches of transactions (blocks) that link back to the last block for order. However, without the "chain," these blocks are just a fancy linked list. To chain the blocks together, each contains the hash of the previous block and a nonce (a random number), in addition to the batch of transactions. Cryptographic hashes work such that changing even one letter in the previous block hash changes the hash of the whole block. 

![blockchain](https://hackernoon.com/photos/EQeID6yCCkTiup8cwmHf2RBGtEE2-sy2ak2bti)

And why does the hash of the block matter? These hashes are what bitcoin **miners** mine for. Instead of digging through dirt, miners dig through piles of random numbers to find one that produces a block hash with a specific number of zeroes in front of it. When a miner finds this hash, they have produced a new block, which their node can propel to the network. The block's batch of transactions will include an additional transaction rewarding bitcoins to the miner.

Each block hash is difficult to come by, and can be altered with the smallest change to the block. Because each block is linked to the last, changing a transaction within any block means producing new hashes for every block on top of it. Thus, the longer a blockchain is, the more computation power that's gone into finding these block hashes, and the "safer" it is that its transactions will not be reversed.  

The true copy of transactions, as agreed upon by the nodes, is the longest chain of blocks, with the most computational work spent to calculate its block hashes.

### Monetary Supply + Disagreements

New bitcoins are only produced when new blocks are mined. How much bitcoin is produced for each block is halved every 4 years, so that only 21 million bitcoin is ever in circulation. Again, if a node wants to change this value, they would need the entire network to agree. Though I've mentioned how hard it is to enact change on the blockchain, it is possible to [fork the chain](https://en.wikipedia.org/wiki/Fork_(blockchain)). Generally people don't want an irreversible fork, since it splits the network into weaker parts and de-values the currency, so major forks only happen over extreme disagreements. Think of forking as seceding from a country, but the civil war is just internet screaming. Bitcoin has forked over issues but still remains standing, so I'm comfortably assuming the 21mil limit won't change.

The supply of dollars, on the other hand, is determined by the Federal Reserve. Though the US has democracy, citizens can't vote on their exact approval of direct bills like the stimulus. Crypto-hardos distrust the government more than I do, but no country has a monetary policy directly accessible to citizens. This is probably for the best. Still, Bitcoin can fill in as the alternative currency: deflationary, limited, and accessible through CPU. Some people buy bitcoin as a hedge against their national currency's instability.

## Concluding thoughts

While this whole writeup is Bitcoin-heavy, decentralization and truth-keeping are universal to all major cryptocurrencies. One of my pipe dreams is for Bitcoin/crypto voting patterns (CPUs, forks) to evolve into something usable by democracy. While it's even less ready than that voting app today, [more-advanced-than-forking governance schemes](https://messari.io/resource/on-chain-governance) are experimented through newer chains, and new consensus algorithms seem to be invented every day. Crypto has created an exciting time to make big group decisions.

No one knows where crypto is going and whether it'll destroy society. Part of the excitement, however, is knowing this future is yet to be shaped, and anyone can become the crypto-fascist of tomorrow. I stress out at least once a month about whether I'm contributing to impending human misery. But, so much has yet to be built that doom seems avoidable! At least the code is cool.
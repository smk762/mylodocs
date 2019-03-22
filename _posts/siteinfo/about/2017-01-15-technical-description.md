---
date: 2019-03-22
title: Technical description
description: What does a notary node do
type: Document
categories:
  - about
---
A more technical description about what the notary node network does:
* To understand the role of a Komodo Notary Node, you first need to understand Komodo’s Delayed Proof of Work (dPoW) security mechanism.
* Essentially, the dPoW security mechanism uses a series of cross-chain notarizations to provide Bitcoin-level security to every dPoW-protected blockchain. Komodo’s Notary Nodes perform the notarizations.
* Every 10 minutes or so, Komodo’s Notary Node essentially backups each chain on Komodo Platform by recording the block hash, block height, and name of the coin being notarized. This is done by performing a Komodo transaction, and storing the data as a message in “OP_Return”.
* Then, using the same procedure, Komodo’s Notary Node network writes the same important chain data from the Komodo blockchain onto the Bitcoin blockchain.
* The transaction ID (txid) of this Bitcoin transaction is then written back to the Komodo blockchain, providing a verifiable link of the chain state history, providing protection against 51% attacks at a cost of approximately 180 BTC per year. 
* The role of Notary Nodes in the dPoW system is to come to a consensus on the height and hash to be written to the BTC ledger.
* In order for a notarization to take place, 13 Notary Nodes must agree on the block height and block hash. Then, the notarization transaction needs to be validated by the entire Komodo network, just like any other transaction. 
* Even in a worst case scenario of Notary Node Operators trying to disrupt the Komodo network, the only power the malicious nodes would have is to withhold a notarization. It would limit the effectiveness of dPoW security but would not cause any real harm.
* Underperforming Notary Nodes are easily identified and risk losing their seat at the next election. Since the 28 top-performing notary nodes are automatically elected each year, Notary Node Operators are incentivized to run their diligently. 
* Notary Node teams also contribute to the betterment of Komodo’s ecosystem through core code updates, app/dapp development, representation at events, and community outreach. There is a high level of autonomy regarding methods of contribution, outlined in the proposals of each node standing for election, allowing the voting community to evaluate the merit of each proposal and progress toward achievement of previously-stated goals.

It is important to note that Notary Nodes are not Master Nodes. They do not have the power to refuse or change transactions. Notary Nodes are not intended to be purchased as an investment without ongoing maintenance and ecosystem contribution.

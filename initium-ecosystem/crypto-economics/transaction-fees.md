---
description: >-
  This article describes the transaction fees on the Initium network. This
  article is subjected to the change.
---

# Transaction Fees

### Low-Cost Transactions&#x20;

Leptons, a fraction of INIX, will be used to pay transaction fees on the Initium network. The proposed basic transaction fee on the Initium network is 5000 leptons, equal to 0.000005 INIX.&#x20;

### Initium Fee ModelI

Initium will benefit from the [Feodis](../../about-initium/feodis-fee-model.md) transaction fee model.&#x20;

### Transaction Fees

Each transaction sent through the Initium network, to be processed by the current Prime Node and the validators and confirmed as a global state transaction, contains a transaction fee. Transaction fees offer many benefits in the Initium economic design, including;

* They provide unit compensation to the validator network for the CPU/GPU resources necessary to process the state transaction,
* They reduce network spam by introducing real cost to transactions,
* and provide potential long-term economic stability of the network through a protocol-captured minimum fee amount per transaction.

Network consensus votes are sent as normal system transfers, which means that validators pay transaction fees to participate in consensus.&#x20;

The proposed basic transaction fee (minimum fee) on the Initium network is 0.000005 INIX which makes Initium one of the most cost-effective networks for users and developers. It means that even if the INIX price becomes $1,000, a transaction on the Initium network will be as cheap as $0.005!

### Use of Transaction Fees

To create a sustainable economy through protocol-based rewards and transaction fees, a fixed portion (50%) of each transaction fee will be added to the Staking Rewards Pool for [staking rewards](initium-tokenomics/staking-rewards.md), with the remaining fee going to the Fee Pool to be distributed among the validators as below:

* Prime Node: 5%
* Supervisor Node: 5%
* Validator Squad: 90% (will be distributed based on the transactions they verify)

The Inflation Schedule provides a source for rewards distributed to all validators. The transaction fee mechanism incentivizes the validators to increase their % Staked INIX, up-time, contribution to the network, and investing in their CPU/GPU resources.&#x20;

As mentioned earlier, the Prime Node and Supervisor Node will receive 5% of the Fee Pool. This design intents to retain a given Prime Node incentive to include as many transactions as possible within its prime-slot time while providing an inflation limiting mechanism that protects against "tax evasion" attacks (i.e. side-channel fee payments).


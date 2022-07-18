---
description: >-
  This article describes the transaction fees on the Initium network. This
  article is subjected to the change.
---

# Transaction Fees

### Low-Cost Transactions&#x20;

Transaction fees on the Initium network will be paid by leptons, a fraction of INIX. The proposed basic transaction fee on the Initium network is 5000 leptons, equal to 0.000005 INIX.&#x20;

### Transaction Fees

Each transaction sent through the Initium network, to be processed by the current Prime Node and the validators and confirmed as a global state transaction, contains a transaction fee. Transaction fees offer many benefits in the Initium economic design, including;

* They provide unit compensation to the validator network for the CPU/GPU resources necessary to process the state transaction,
* They reduce network spam by introducing real cost to transactions,
* and provide potential long-term economic stability of the network through a protocol-captured minimum fee amount per transaction.

Network consensus votes are sent as normal system transfers, which means that validators pay transaction fees to participate in consensus.&#x20;

The proposed basic transaction fee (minimum fee) on the Initium network is 0.000005 INIX which makes Initium one of the most cost-effective networks for users and developers. It means that even if the INIX price becomes $1,000, a transaction on the Initium network will be as cheap as $0.005!

To create a sustainable economy through protocol-based rewards and transaction fees, a fixed portion (50%) of each transaction fee will be added to the Staking Rewards Pool, with the remaining fee going to the Fee Pool to be distributed among the validators as below:

* Prime Node: 5%
* Supervisor Node: 5%
* Validator Squad: 90% (will be distributed based on the transactions they verify)

The Inflation Schedule provides a source for rewards distributed to all validators. The transaction fee mechanism incentivizes the validators to increase their % Staked INIX, up-time, contribution to the network, and investing in their CPU/GPU resources.&#x20;

As mentioned earlier, the Prime Node and Sypervisor Node will receive 5% of the Fee Pool. This design intents to retain a given Prime Node incentive to include as many transactions as possible within its prime-slot time while providing an inflation limiting mechanism that protects against "tax evasion" attacks (i.e. side-channel fee payments).

Since 50% of the transaction fees will be added to the Staking Rewards Pool, the increase in the number of transactions that a Prime Node includes within its prime-slot increases the APY of the participants. This issue is discussed in [Staking Rewards](initium-tokenomics/staking-rewards.md#important-considerations).

### Initium Fee Model

Normally, networks like Ethereum transactions include a fee field that indicates the maximum fee field a slot leader is permitted to charge for processing a transaction. The cluster, on the other hand, agrees on a minimum fee. If the network is congested, the slot leader may prioritize the transactions offering higher fees. That means the client won't know how much was collected until the transaction is confirmed by the cluster and the remaining balance is checked. This is what we would see in networks like Ethereum which results in unexpected higher gas fees.&#x20;

However, Initium will benefit from the _Congestion Driven Fee_ model in a very reliable way. In this Congestion Driven Fee model, each validator uses _signatures per slot_ (SPS) to estimate network congestion and _SPS target_ to estimate the desired processing capacity of the cluster. The validator learns the SPS target from the genesis config, whereas it calculates SPS from recently processed transactions.&#x20;

The genesis config also defines a target`lepton_per_signature`, the fee to charge per signature when the cluster operates at the _SPS target_. The client uses the `JSON RPC API` to query the cluster for the current fee parameters. Those parameters are tagged with a block hash and remain valid until that block hash is old enough to be rejected by the slot's Prime Node.

Before sending a transaction to the cluster, a client may submit the transaction, and fee _codex_ data to an SDK module called the _fee calculator_. So long as the client's SDK version matches the slot's prime node version, the client is assured that its account will be charged the same number of leptons as the _fee calculator_.


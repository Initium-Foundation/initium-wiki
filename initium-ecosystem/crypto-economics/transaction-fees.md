---
description: >-
  This article describes the transaction fees on the Initium network. This
  article is subjected to the change.
---

# Transaction Fees

### What is Nip?

Nip is the smallest amount of INITIUM. 1 Nip equals 0.000000001 or 10^-9 of INITIUM. 1 INITIUM is 10^9 Nip. Nip is used to calculate the transaction fee on the Initium network. In another word, transaction fees on the Initium network will be paid by a fraction of INITIUM. The proposed basic transaction fee on the Initium network is 5000 Nips, equal to 0.000005 INITIUM.&#x20;

### Transaction Fees

Each transaction sent through the Initium network, to be processed by the current Prime Node and the validators and confirmed as a global state transaction, contains a transaction fee. Transaction fees offer many benefits in the Initium economic design, including;

* They provide unit compensation to the validator network for the CPU/GPU resources necessary to process the state transaction,
* They reduce network spam by introducing real cost to transactions,
* and provide potential long-term economic stability of the network through a protocol-captured minimum fee amount per transaction.

Network consensus votes are sent as normal system transfers, which means that validators pay transaction fees to participate in consensus.&#x20;

The proposed basic transaction fee (minimum fee) on the Initium network is 0.000005 INITIUM which makes Initium one of the most cost-effective networks for users and developers. It means that even if the INITIUM price becomes $1,000, a transaction on the Initium network will be as cheap as $0.005!

In an attempt to create a sustainable economy through protocol-based rewards and transaction fees, a fixed portion (initially 50%) of each transaction fee is destroyed, with the remaining fee going to the Fee Pool to be distributed among the validators participated with the Prime to process and confirm the transactions.&#x20;

The fee burning schedule on the Initium network is subjected to decrease by 15% every four years cycle. The table below shows this schedule.&#x20;

|                       |                 |
| --------------------- | --------------- |
| Cycle (every 4 years) | Fee Buring Rate |
| 1                     | 50%             |
| 2                     | 42.50%          |
| 3                     | 36.13%          |
| 4                     | 30.71%          |
| 5                     | 26.10%          |
| 6                     | 22.19%          |
| 7                     | 18.86%          |
| 8                     | 16.03%          |
| 9                     | 13.62%          |
| 10                    | 0               |

A scheduled global inflation rate provides a source for rewards distributed to validators, through the process described before. In the meantime, the Prime Node will receive the block reward for setting the global state and leading the state. The block reward is an initiative to encourage the validators to invest in their CPU/GPU resources.&#x20;

This minimum portion of each transaction fee can be dynamically adjusted depending on historical _signatures-per-slot_. In this way, the protocol can use the minimum fee to target the desired hardware utilization. By monitoring a protocol specified _signatures-per-slot_ with respect to a desired, target usage amount, the minimum fee can be raised/lowered which should, in turn, lower/raise the actual _signature-per-slot_ per block until it reaches the target amount. This adjustment process can be thought of as similar to the difficulty adjustment algorithm in the Bitcoin protocol, however in this case it is adjusting the minimum transaction fee to guide the transaction processing hardware usage to the desired level.

As mentioned, a fixed proportion of each transaction fee is to be destroyed. The intent of this design is to retain a given Prime Node incentive to include as many transactions as possible within its prime-slot time while providing an inflation limiting mechanism that protects against "tax evasion" attacks (i.e. side-channel fee payments).

Additionally, the burnt fees can be a consideration in fork selection. In the case of a PoSync fork with a malicious, censoring prime, we would expect the total fees destroyed to be less than a comparable honest fork, due to the fees lost from censoring. If the censoring prime is to compensate for these lost protocol fees, they would have to replace the burnt fees on their fork themselves, thus potentially reducing the incentive to censor in the first place.

### Initium Fee Model

Transaction fees are set by the network cluster based on recent historical throughput, which is called the _Congestion Driven Fee_ model. Normally, transactions include a fee field that indicates the maximum fee field a slot prime is permitted to charge to process a transaction. The cluster, on the other hand, agrees on a minimum fee. If the network is congested, the slot prime may prioritize the transactions offering higher fees. That means the client won't know how much was collected until the transaction is confirmed by the cluster and the remaining balance is checked. This is what we would see in networks like Ethereum which results in unexpected higher gas fees.&#x20;

However, Initium will benefit from the _Congestion Driven Fee_ model. In the Congestion Driven Fee model, each validator uses _signatures per slot_ (SPS) to estimate network congestion and _SPS target_ to estimate the desired processing capacity of the cluster. The validator learns the SPS target from the genesis config, whereas it calculates SPS from recently processed transactions.&#x20;

The genesis config also defines a target `nip_per_signature`, which is the fee to charge per signature when the cluster is operating at _SPS target_. The client uses the JSON RPC API to query the cluster for the current fee parameters. Those parameters are tagged with a blockhash and remain valid until that blockhash is old enough to be rejected by the slot Prime Node.

Before sending a transaction to the cluster, a client may submit the transaction and fee account data to an SDK module called the _fee calculator_. So long as the client's SDK version matches the version of the slot prime, the client is assured that its account will be charged exactly the same number of nip as returned by the fee calculator.


---
cover: ../.gitbook/assets/wiki-header3.png
coverY: 0
---

# Network Design

Initium is a multi-network blockchain that benefits from robust network architecture to enhance the network's scalability, security, and decentralization. As illustrated in the figure below, a system node is designated as the Prime node at any given time to generate a Proof of Synchronization sequence (Covenant), providing the network global read consistency and a verifiable time frame for verifying the transaction. The Prime Node sequences user messages and orders them such that they can be efficiently processed by other nodes in the system, maximizing throughput. It executes the transactions on the current state stored in RAM, publishes them, and sends a final state signature to the replication nodes called Supervisor.&#x20;

The Supervisor node plays a vital role as it checks the transactions to be valid in the [Initium Constitution](../appendix/contribution.md). If a transaction meets the constitution rules, then the Supervisor node keeps it in the message order. Otherwise, the transaction will be rejected. The state will proceed with the approved transactions and will be sent to the Verifier Squad.&#x20;

The Verifier Squad is a set of 20 replication nodes in the Initium network that work under the supervision of the Supervisor node. The Supervisor node will ask the honest nodes to join the squad. If 14 out of 20 nodes agree to join, the squad will be formed, and the state transactions will be distributed among the agreed nodes for verification.&#x20;

In a Verifier Squad, all Verifiers execute the same transactions on their copies of the state and publish their computed state signatures as confirmations. The published confirmations serve as votes for the consensus algorithm. Verifiers send their votes to the Supervisor Node. Then it sends them as the aggregated votes to the Prime node. Verifiers receive transaction fees for the transactions they process and verify.&#x20;

Initium benefits from an innovative fee model called Feodis which prevents unexpected higher gas fees while incentivizing the validators processing the transactions with different priorities set by the user.

The [transaction fees](../initium-ecosystem/crypto-economics/transaction-fees.md) are paid for processing and confirming the transactions. 50% of the transaction fees will be allocated to the Staking Rewards Pool for the Staking Rewards. The remaining 50% of the transaction fees will be distributed among the cluster participants, including The Prime, the Supervisor, and the validators that contributed to the squad.

![Initium Network DesignT](<../.gitbook/assets/Screen Shot 2022-07-14 at 4.39.54 PM.png>)

The disagree verifiers in a squad will improve their reputation by signing the state, which makes them eligible to be among the honest validators in the next cluster.

The Prime Node and Supervisor are temporary roles in the network since the verifiers vote to choose the next Prime and Supervisor nodes to set and supervise the new state. Every validator has the equal right to vote and the chance to be elected as the next Prime and Supervisor nodes. This election takes place based on the PoS mechanism.


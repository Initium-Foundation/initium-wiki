---
cover: ../.gitbook/assets/wiki-header3.png
coverY: 0
---

# Network Design

The Initium benefits from robust network architecture to enhance the network's scalability, security, and decentralization. As illustrated in the figure below, at any given time, a system node is designated as Prime Node to generate a Proof of Synchronization sequence (Covenant), providing the network global read consistency and a verifiable time frame for verifying the transaction. The Prime Node sequences user messages and orders them such that they can be efficiently processed by other nodes in the system, maximizing throughput. It executes the transactions on the current state stored in RAM, publishes them, and sends a final state signature to the replication nodes called Supervisor.&#x20;

The Supervisor node plays a very important role as it checks the transactions to be valid in the Initium Constitution. If a transaction meets the constitution rules, then the Supervisor node keeps it in the message order, otherwise the transaction will be rejected. The state will proceed with the approved transactions and will be send to the Verifier Squad.&#x20;

The Verifier Squad is a set of 20 replication nodes in the Initium network that work under supervision of the Supervisor node. To organize a Verifier Squad, the Supervisor node will ask the honest nodes to join the squad for the squad. If 14 nodes out of 20 nodes agree to join the squad, the squad will be formed and the state transactions will be distributed among the agreed nodes for verification.&#x20;

In a Verifier Squad, all Verifiers execute the same transactions on their copies of the state and publish their computed signatures of the state as confirmations. The published confirmations serve as votes for the consensus algorithm. Verifiers send their votes to the Supervisor Node and the the Supervisor node send the aggregated votes to the Prime node. Verifiers receive transaction fees for the transactions they process and verify.&#x20;

The Prime Node is not receiving transaction fees, but will receive the block rewards for the new block that it leads it. The supervisor node will receive supervision fee from the verifiers which is 20% of their received fees.&#x20;

![Initium Network DesignT](<../.gitbook/assets/Screen Shot 2022-07-14 at 4.39.54 PM.png>)

The disagree verifiers in a squad will improve their reputation by signing the state which makes them eligible to be among the agree verifiers in the next cluster.&#x20;

The Prime Node and Supervisor are temporary roles in the network since the verifiers vote to choose the next Prime Node and Supervisor Node to set the new state. The Supervisor Node is chosen by the verifiers' vote to supervise the integrity of the new state throughout the network. Every Verifier has the equal right to vote and the equal chance to be elected as the next Prime Node and or Supervisor Node. This election takes place based on the PoS mechanism.

#### Initium Constitution&#x20;

The Initium Constitution (`Constitution`) is a unique feature of the Initium protocol which significantly improves the confidence and the security of the ecosystem. It is actually a set of rules that govern the protocol. This rules are called `Regula`. Every Regula is set for a purpose on the Constitution.&#x20;

The Constitution is governed by the Initium community and they can set new a Regula and alter or terminate a an existing Regula in Covenant DAO. The implementation of changes to the Constitution needs at least 51% of the Initium validators execute it.

#### The Advantages of Constitution&#x20;

Most of the existing blockchain network suffer from spams and spoiling activities (e.g., hacker attacks to the DeFi platform). To solve such problems, Initium benefits from the Constitution concept for regulating the network by its community.&#x20;

Initium community can set Regulas for preventing any harmful activity or attack that threatens their funds and the stability of the ecosystem.&#x20;

In the meantime, the constitution prevents the abuses from the network by the illegal activities.&#x20;

The Constitution can cover a wide range of Regulas, ranging from changes in the transaction fees to soft forks, etc.&#x20;

#### Role of Constitution in Transactions&#x20;

The Supervisor node is responsible to check every transaction for meeting the transaction regulas of the Constitution. For example, if the funds of Initium community on an exchange is stoles by the hackers, they can propose a Regula for blocking that tokens in the ecosystem and prevent their laundry by the hackers. In such a case, the Supervisor nodes won't let those funds being moved from the hackers wallets. The Initium community even can propose the elimination of such tokens from the Current Total Supply of the network, which makes the hackers stolen funds useless.&#x20;

#### Constitution and Decentralization&#x20;

We believe that this is the absolute right of the Initium community to rule and control the entire ecosystem without manipulation from the founder team or any other parties. The Initium Constitution is a mechanism that ensures the decentralization of the ecosystem by assigning the governance rights to the community. It ensures that no centralized body can control the Initium protocol and the community has the full control of the ecosystem.&#x20;




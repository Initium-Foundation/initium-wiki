---
cover: ../.gitbook/assets/wiki-header3.png
coverY: 0
---

# Network Design

The Initium benefits from robust network architecture to enhance the network's scalability, security, and decentralization. As illustrated in the figure below, at any given time, a system node is designated as Prime Node to generate a Proof of Synchronization sequence (Covenant), providing the network global read consistency and a verifiable time frame for verifying the transaction. The Prime Node sequences user messages and orders them such that they can be efficiently processed by other nodes in the system, maximizing throughput. It executes the transactions on the current state stored in RAM, publishes them, and sends a final state signature to the replication nodes called Verifiers. Verifiers execute the same transactions on their copies of the state and publish their computed signatures of the state as confirmations. The published confirmations serve as votes for the consensus algorithm. Verifiers receive transaction fees for the transactions their process and verify. In addition to the fees, the verifiers that participated in producing a block will also receive the block reward.

![Initium Network Design](<../.gitbook/assets/Screen Shot 2022-06-29 at 4.22.32 PM.png>)

The Supervisor node (Supervisor) is a random node selected by the verifiers to supervise the transaction verification and the integrity of the state throughout the network.&#x20;

The Prime Node rule is a temporary role in the network since the verifiers vote to choose the next Prime Node to set the new state. The Supervisor Node is also chosen by the verifiers' vote to supervise the integrity of the new state throughout the network. Every Verifier has the equal right to vote and the equal chance to be elected as the next Prime Node and or Supervisor Node. This election takes place based on the PoS mechanism.


---
description: The Consensus of Initium
cover: ../.gitbook/assets/wiki-header3.png
coverY: 0
---

# Covenant Consensus

### What means the Covenant?

The "Covenant" means a usually formal, solemn, and binding agreement. This term refers to the unique consensus of the Initium network, the Proof of Synchronization (PoSync), which is a mixture of Proof of Importance (PoI), Proof of Time (PoT), Proof of Stake, and Proof of Replication. This makes Covenant a complex consensus that enables complex events to take place on the Initium blockchain.&#x20;

Therefore, whenever you see the term `Covenant` in Initium's terminology, it refers to the consensus of the Initium network.&#x20;

To its easiest definition, `Covenant` is a cluster-based synchronization protocol that uses clustering to achieve energy efficiency and resilience to faulty nodes in the system. Clustering techniques are known to reduce the energy expenditure of the nodes and provide routing through representative nodes called Cluster heads (CH). We refer to this `Cluster Head` (CH) node in `Covenant` the protocol as `Prime Node`. Since communication in `Covenant` (Proof of Synchronization) involves only `Prime` and `Supervisor` nodes, the number of messages exchanged is reduced significantly compared to other protocols. Our preliminary results show that Covenant achieves a worst-case synchronization error of 37 _µs (_0.037 _ms_) __ in a multi-hop network of up to 10 hops.

![Figure 1. Covenant Protocol with two phases of operations](<../.gitbook/assets/Screen Shot 2022-06-30 at 8.39.07 PM.png>)

&#x20;

Covenant protocol operates in two phases of 1) _clustering_ and 2) _consensus_ and adopts a slotted operation mode where synchronization is performed in fixed time slots while applications are executed in the remaining time slots, as shown in Figure 1.&#x20;

### 1/2) Cluster Phase of Covenant&#x20;

In the first phase of Covenant, the nodes are grouped into clusters. A clustering process is a state machine of 3 states: 1) neighbor discovery, 2) election, and 3) connection, as indicated in Figure 2.

![Figure 2. Covenant Protocol clustering phase with state transitions](<../.gitbook/assets/Screen Shot 2022-06-30 at 8.44.12 PM (1).png>)

Nodes become aware of their neighboring nodes in the neighbor discovery state. Time information is added to the messages to achieve an implicit synchronization during this state, similar to Gradient Time Synchronization Protocol (GTSP). GTSP achieves time synchronization by averaging neighbor time information and provides resilience for the clustering phase (C-GTSP). During the election phase, a representative node, the `Prime Node`, is chosen as a cluster head (CH) based on the maximum degree (number of connections) of a node. Lastly, the connection state selects a representative bridge node (nodes that belong to multiple clusters) as a cluster bridge (CB) and other bridge nodes as supervision cluster bridges (SCB) (the `Supervisor`)  to ensure inter-cluster connectivity and resilience.

### 2/2) **Consensus Phase of Covenant**

Consensus Control (Cons-Ctrl) is the second phase of Covenant which repeats periodically after specific time slots to maintain the synchronization. The cluster heads exchange time information to find _local centers_ of their neighborhood.&#x20;

![Figure 3. Convergence and consensus phase with TDMA communication](<../.gitbook/assets/Screen Shot 2022-06-30 at 8.48.08 PM.png>)

The configuration limits the maximum number of hops before reaching the consensus. Local centers bound the maximum error across the network. The time information of the local centers is propagated back to the CHs in the reverse direction after the convergence. The order of the Prime Node receiving data is the reverse of finding local centers; hence, the time-division multiple access (_TDMA)_ slots for each cluster are created accordingly for the _synchronize and supervise_ phase. Thus, the protocol scales very well for more extensive network sizes without additional energy loss and additional delay for consensus. However, given the dynamic nature of the network, some nodes may fail, or new nodes may join the network. If there are significant changes (e.g., change in CH), clustering is triggered again to establish new clusters with the optional _correction_ state of the consensus phase in Figure 3.

The elected cluster bridge (CB) and supervision cluster bridge (SCB) nodes act as supervision nodes to monitor the broadcast data of Prime nodes to their cluster member nodes. SCB also ensures reliable and accurate information propagation during consensus. In the case of a byzantine fault, e.g., the Prime node sending corrupt time information, CBs and SCBs intervene and share the legitimate value of time. As Cluster Bridges are connected to other clusters, they further forward the valid time information along the network path. Hence, the impact of a byzantine event can be detected and contained within a single cluster.

### **Hashing Function**

Covenant uses the SHA256 algorithm to hash the data. Hashing new data starts with a cryptographic hash function, whose output is not predictable without running the function (e.g., SHA256). It runs the function from some random starting value, takes its output, and passes it as the input into the same function again. Record the number of times the function has been called and the output at each call.


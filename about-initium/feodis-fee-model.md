# Feodis Fee Model

Usually, networks like Ethereum transactions include a fee field that indicates the maximum fee field a slot leader is permitted to charge for processing a transaction. The cluster, on the other hand, agrees on a minimum fee. If the network is congested, the slot leader may prioritize the transactions offering higher fees. That means the client won't know how much was collected until the cluster confirms the transaction and the remaining balance is checked. This mechanism would result in unexpected higher gas fees.

**Feodis Fee Model**

Initium will benefit from an innovative congestion-driven fee model called _Feodis_. In the Feodis fee model, each validator uses _signatures per slot_ (SPS) to estimate network congestion and _SPS target_ to estimate the desired processing capacity of the cluster. The validator learns the SPS target from the genesis config, whereas it calculates SPS from recently processed transactions.&#x20;

The genesis config also defines a target`lepton_per_signature`, the fee to charge per signature when the cluster operates at the _SPS target_. The client uses the `JSON RPC API` to query the cluster for the current fee parameters. Those parameters are tagged with a block hash and remain valid until that block hash is old enough to be rejected by the slot's Prime Node.

Before sending a transaction to the cluster, a client may submit the transaction, and fee _codex_ data to an SDK module called the _fee calculator_. So long as the client's SDK version matches the slot's prime node version, the client is assured that its account will be charged the same number of leptons as the _fee calculator_.

The Feodis also allows the users to conduct different transactions with different priorities. For example, in a multi-level transaction, a user may prefer to prioritize the transactions by various parameters to be executed on the network. This is a handy capability, especially for smart contracts to prioritize transactions with complex varieties.

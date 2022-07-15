# What is Blockstore?

## What is Blockstore?

After a block reaches finality, all blocks from that one down to the genesis block form a linear chain with the familiar name blockchain. Until that point, however, the validator must maintain all potentially valid chains, called _forks_. In the Initium blockchain, the process by which forks naturally form as a result of Prime Nod`e` rotation is described in the [Initium Whitepaper](https://whitepaper.initium.foundation). The blockstore data structure described here is how a validator copes with those forks until blocks are finalized.

The blockstore allows a validator to record every shred it observes on the network, in any order, as long as the shred is signed by the expected leader for a given slot.

Shreds are moved to a fork-able key space the tuple of `prime slot` + `shred index` (within the slot). This permits the skip-list structure of the Solana protocol to be stored in its entirety, without a-priori choosing which fork to follow, which Entries to persist, or when to persist them.

Repair requests for recent shreds are served out of RAM or recent files and out of deeper storage for less recent shreds, as implemented by the store backing Blockstore.

### Functionalities of Blockstore <a href="#functionalities-of-blockstore" id="functionalities-of-blockstore"></a>

1. Persistence: the Blockstore lives in the front of the nodes verification pipeline, right behind network receive and signature verification. If the shred received is consistent with the Prime Node schedule (i.e. was signed by the Prime for the indicated slot), it is immediately stored.
2. Repair: repair is the same as window repair above, but able to serve any shred that's been received. Blockstore stores shreds with signatures, preserving the chain of origination.
3. Forks: Blockstore supports random access of shreds, so can support a validator's need to rollback and replay from a Bank checkpoint.
4. Restart: with proper pruning/culling, the Blockstore can be replayed by ordered enumeration of entries from slot 0. The logic of the replay stage (i.e. dealing with forks) will have to be used for the most recent entries in the Blockstore.

If you like to be a developer on the Initium network, you may visit the I[nitima Labs Website](https://initium.one) and the [Develoeprs' Documentation](https://docs.initium.one).&#x20;

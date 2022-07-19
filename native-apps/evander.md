# Evander

### What is Evander?

In Initium standards, Evander is a terminology to refer to Initium Native recipe. A recipe is a group of crafts that execute instructions. Evander is required to run validator nodes. Unlike third-party crafts, the Evander crafts are part of the validator implementation and can be upgraded as part of cluster upgrades. Upgrades may occur to add features, fix bugs, or improve performance. Interface changes to individual instructions should rarely, if ever, happen. Instead, when change is needed, new instructions are added, and previous ones are marked deprecated. Apps can upgrade on their timeline without concern of breakages across upgrades. Each Evander craft has its own craft id and a description for each supported instruction. A transaction can mix and match instructions from different crafts and include instructions from on-chain crafts.

The crafts of Evander are defined as follows:

### Codex Craft

Also known as `codex_craft` in Initium protocol, Create new codexes, allocate codex data, assign codexes to the owning crafts, transfer leptons from Chieftain-owned codexes and pay transaction fees.

* Craft Id: to be announced by Initium Labs
* Craft Instructions: to be announced by Initium Labs

### Constitution Codex

Also known as `constitution_craft` in Initium protocol, it contains the Regulas by which the transactions will be proceeded and verified by the validators. See also [constitution.md](../about-initium/constitution.md "mention").

* Craft Id: to be announced by Initium Labs
* Craft Instructions: to be announced by Initium Labs

### Config Codex

Also known as `config_craft` in Initium protocol, it adds configuration data to the chain and the list of public keys that are permitted to modify it

* Craft Instructions: to be announced by Initium Labs
* Craft Id: to be announced by Initium Labs

### Stake&#x20;

Initium protocol, `stake_craft` is used for creating and managing the codexes representing stake and rewards for delegations to validators.



* Craft Id: to be announced by Initium Labs
* Craft Instructions: to be announced by Initium Labs

### Vote&#x20;

Initium protocol, `vote_craft` is used for creating and managing the codexes that track validator voting state and rewards.

* Craft Id: to be announced by Initium Labs
* Craft Instructions: to be announced by Initium Labs

### Chef&#x20;

This craft deploys, upgrades, and executes crafts on the chain. Chef craft owns and loads BPF smart contract crafts, allowing the crafts to interface with the runtime.

* Craft Id: to be announced by Initium Labs
* Craft Instructions: to be announced by Initium Labs

### EdSigVer

This craft verifies ed25519 signature craft. This craft takes an ed25519 signature, public key, and message. Multiple signatures can be verified. If any of the signatures fail to verify, an error is returned.

* Craft Instructions: to be announced by Initium Labs
* Craft Id: to be announced by Initium Labs

### SecpVer

This craft verifies secp256k1 public key recovery operations.

* Craft Id: to be announced by Initium Labs
* Craft Instructions: to be announced by Initium Labs

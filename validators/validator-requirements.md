---
description: Subject to change.
---

# Validator Requirements

### Minimum INI requirements

No strict minimum amount of INI will be required to run a validator on the Initium network. However, the validators with higher staking of INI have more voting power, receive more transactions to validate, and have more chances to be elected as the Prime Node to receive the block rewards. The Initium community can stake their INI tokens on the validators to increase their staking and receive the staking rewards. For more information, you may read [Staking Rewards](../crypto-economics/staking-rewards.md).&#x20;

### Vote Booklet

A vote booklet is needed to participate in consensus.&#x20;

### Transaction Fees

Voting also requires sending a vote transaction for each block the validator agrees with, which can cost a few INI or [leptons](../crypto-economics/what-is-lepton.md) per day.

### Hardware Recommendations

Upon the launch of the Initium Testnet, we cannot have a finalized figure from the hardware requirements for a validator. However, based on our laboratory estimations, the following requirements are expected:

#### CPU

* 12 cores / 24 threads, or more
* 2.8GHz, or faster
* AVX2 instruction support (to use official release binaries, self-compile otherwise)
* Support for AVX512f and/or SHA-NI instructions is helpful
* The AMD Zen3 series is recommended.

#### RAM

* 128GB, or more
* Motherboard with 256GB capacity suggested

#### Disk

* PCIe Gen3 x4 NVME SSD, or better
* Accounts: 500GB or larger. High TBW (Total Bytes Written)
* Ledger: 1TB or larger. High TBW suggested
* OS: (Optional) 500GB, or larger. SATA OK.

#### GPUs

* Not strictly necessary

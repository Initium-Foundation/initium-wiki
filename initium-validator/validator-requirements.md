---
description: Subject to change.
---

# Validator Requirements

### Minimum INIX requirements

A minimum amount of 2,000 INIX will be required to run a validator on the Initium network. The validators with higher staking of INIX have more voting power, receive more transactions to validate, and have more chances to be elected as the Prime Node to receive the block rewards. The Initium community can stake their INIX tokens on the validators to secure the Initium, increase validators' stakings, and acquire the staking rewards. For more information, you may read Staking Rewards.

### Vote Booklet

A vote booklet is needed to participate in consensus.&#x20;

### Transaction Fees

Voting also requires sending a vote transaction for each block the validator agrees with, costing around 1 INIX per day.&#x20;

### Hardware Recommendations

Upon the launch of the Initium Testnet, we cannot have a finalized figure from the hardware requirements for a validator. However, based on our laboratory estimations, the following requirements are expected. We plan to decrease the hardware cost for the running validators for the mainnet. The hardware costs at the time of writing this article are around $850-$1,300, depensing on the manufacturer's brand. &#x20;

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

* Not strictly necessary. Motherboard and power supply specs to add one or more high-end GPUs in the future are suggested.

### Networking

Internet service should be at least 300Mbit/s symmetric, commercial. 1GBit/s is highly preferred for blockchain validators by most of the networks.&#x20;

#### Port Forwarding <a href="#port-forwarding" id="port-forwarding"></a>

The following ports should be open to the internet for both inbound and outbound. It is not recommended to run a validator behind a NAT. Operators who choose to do so should be comfortable configuring their networking equipment and debugging any traversal issues on their own.

**Required**

* 8000-10000 TCP/UDP - P2P protocols (gossip, turbine, repair, etc). This can be limited to any free 13-port range with `--dynamic-port-range`

**Optional**

For security purposes, it is not suggested that the following ports be open to the internet on staked, mainnet-beta validators.

* 8899 TCP - JSONRPC over HTTP. Change with \`--rpc-port RPC\_PORT\`\`
* 8900 TCP - JSONRPC over Websockets. Derived. Uses `RPC_PORT + 1`

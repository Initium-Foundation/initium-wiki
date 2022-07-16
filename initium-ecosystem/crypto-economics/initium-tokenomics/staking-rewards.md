# Staking Rewards

### Introduction&#x20;

The main channels of participant rewards remittances are reserves on the [Staking Rewards Pool](initial-supply-distribution.md#staking-rewards-pool), protocol-based rewards, and transaction fees. Protocol-based rewards are generated from inflationary issuances from a protocol-defined [inflation schedule](inflation-schedule.md).&#x20;

n Initium's chronology, there are two periods for staking INIX tokens, including the Pre-Genesis and Post-Genesis periods.

## Pre-Genesis Staking Rewards

This period is between the end of Public Sales Options and the [Genesis Event](../teminology.md#genesis-event). During this period, the following INIX HODLers are eligible to receive the staking rewards:

* **Private Sales' Investors**: as mentioned in Initial Supply Distribution, these HODLers' tokens are subject to 5% APY during the vesting period.&#x20;
* **Validators Staking Investors**: as mentioned in Initial Supply Distribution, these HODLers' tokens are subject to 20% APY during the vesting period.&#x20;
* **Public Sales Option A**: as mentioned in Initial Supply Distribution, these HODLers' tokens are subject to a 20% APR for the vesting period (12 months). As these tokens will be unlocked after the vesting period, these HODLers can stake their INIX token on available pools to obtain rewards based on the regular APR.&#x20;
* **Public Sales Option B**: as mentioned in Initial Supply Distribution, these HODLers' tokens are subject to a 15% APR for the vesting period (18 months). As these tokens will be unlocked after the vesting period, these HODLers can stake their INIX token on available pools to obtain rewards based on the regular APR. &#x20;
* **Public Sales Option C**: since these tokens are not subject to any vesting period, the HODLers' of these tokens can stake their INIX token on available pools to obtain rewards based on the regular APY. &#x20;

### Regular Staking APY

The regular APY for Pre-Genesis period is 10%.&#x20;

### Staking Rewards Impact on Staking Rewards Pool

Initium Foundation expects 60% of the unlocked tokens during the Pre-Genesis period to be staked for obtaining the rewards by the owners.&#x20;

During the first year of the staking, a total amount of 17,650,000 INIX is estimated to be distributed among all staking HODLers as table below.&#x20;

|                       |              |           |                |                     |
| --------------------- | :----------: | :-------: | :------------: | :-----------------: |
| Stakers               | Staking INIX |  APY/APR  | Rewards (INIX) | Total INIX Holdings |
| Validators            |  20,000,000  |    20%    |    4,000,000   |     24,000,0000     |
| Private Investors     |  45,000,000  |     9%    |    4,050,000   |    49,050,000,000   |
| Public Sales Option A |  30,000,000  |    20%    |    6,000,000   |      36,000,000     |
| Public Sales Option B |  30,000,000  |    20%    |    6,000,000   |      36,000,000     |
| Public Sales Option C |   9,000,000  | 10% (APR) |     900,000    |      9,900,000      |
| Total                 |  134,000,000 |           |   19,150,000   |     153,150,000     |

### Validation Clients Rewards

These rewards will constitute the total protocol-based reward delivered to validation clients, the remaining sourced from transaction fees.&#x20;

In the early days of the network, it is likely that protocol-based rewards, deployed based on a predefined issuance schedule, will drive the majority of participant incentives to participate in the network. These protocol-based rewards are calculated per epoch and distributed across the active delegated stake and validator set (per validator commission). As discussed further in this document, the per annum inflation rate is based on a pre-determined disinflationary schedule. That provides the network with supply predictability, supporting long-term economic stability and security.&#x20;

Transaction fees are participant-to-participant transfers attached to network interactions as motivation and compensation for the inclusion and execution of a proposed transaction. A mechanism for long-term economic stability and forking protection through partial burning of each transaction fee is also discussed in this document.

### INITIUM HODLers Rewards

the main channels of the HODLers remittances are protocol-based rewards that are generated from the inflationary issuance from the protocol-defined inflation schedule. These rewards will be distributed among the wallets staked IOT coins on the partner platforms. Validator clients also can provide staking services to the HODLers. The staking service providers would receive 5% of the total rewards distributed among the staking HODLers.

### Rewarding Periods

This document will discuss the rewards in three stages of the Initium network during three different periods as follows:

#### 1) Pre-Genesis Rewards

This period is the period between the issuance of the INITIUM initial supply as a token and the launch of the mainnet of the Initium network. During this period, the HODLers of the INITIUM who participated in the public sales of the INITIUM token would receive an APY for staking their INITIUM on the partner staking platforms. For this, the snapshots from the wallets will be acquired by the staking providers, and the rewards will be distributed based on the average staking amount and the effective staking days.&#x20;

The source of these rewards is the Rewards Pool Reserves (RPR) which is managed by the Initium Foundation. This reserve will be created during the [INITIUM TGE](../teminology.md#initium-tge) with the primary reserves of 30% of the [Initial Supply](../teminology.md#initial-supply) (estimated to be 150,000,000 IOT).&#x20;

#### 2) Genesis Rewards

This period is the first year of the launch of the mainnet. Since this year, the validation clients will receive the rewards' inflationary issuance. The estimated inflation rate for the Genesis Year (Year 1 of the mainnet) is 10%. This amount will be split as follows (note that we have considered no changes in the Initial Supply):

|                         |            |                       |
| ----------------------- | ---------- | --------------------- |
| Receiver(s)             | Percentage | Est. Amount (INITIUM) |
| Validators Rewards Pool | 40%        | 20,000,0000.00        |
| Initium Foundation      | 10%        | 5,000,000.00          |
| Staking Rewards Pool    | 40%        | 20,000,000.00         |
| Dao Funds               | 10%        | 5,000,000.00          |
| Total                   | 100%       | 50,000,000.00         |

The **HOLDers** (excluding the validation clients) will receive their rewards from the Staking _Rewards Pool._ &#x20;

In the meantime, the validation clients will be incentivized with transaction fees and block rewards, which will be discussed further in this document. &#x20;

#### 3) Post-Genesis Rewards

This period starts in the second year of the mainnet (the year after the Genesis Year), by which the inflation rate of INITIUM will be reduced every year by 15%. This reduction will continue to tend the inflation rate to zero. During this period, the fee burning will be reduced to tend to zero, which gives more incentives for the validation clients to secure the network. In the meantime, block rewards during this period are subjected to halving, which tends to be zero for longer terms. This mechanism will be discussed further in this document. &#x20;

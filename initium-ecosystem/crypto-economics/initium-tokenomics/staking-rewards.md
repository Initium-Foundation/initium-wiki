---
description: Subject to change.
---

# Staking Rewards

### Introduction&#x20;

The main channels of participant rewards remittances are reserves on the [Staking Rewards Pool](initial-supply-distribution.md#staking-rewards-pool), protocol-based rewards, and transaction fees. Protocol-based rewards are generated from inflationary issuances from a protocol-defined [inflation schedule](inflation-schedule.md).&#x20;

n Initium's chronology, there are two periods for staking INIX tokens, including the Pre-Genesis and Post-Genesis periods.

## Pre-Genesis Staking Rewards

This period is between the end of Public Sales Options and the [Genesis Event](../teminology.md#genesis-event). The main channel of participants' rewards is the Staking Rewards Pool with basic reserves of 100,000,000 INIX allocated from the Initial Supply. During this period, the following INIX HODLers are eligible to receive the staking rewards:

* **Private Sales' Investors**: as mentioned in Initial Supply Distribution, these HODLers' tokens are subject to 5% APY during the vesting period.&#x20;
* **Validators Staking Investors**: as mentioned in Initial Supply Distribution, these HODLers' tokens are subject to 15% APY during the vesting period.&#x20;
* **Public Sales Option A**: as mentioned in Initial Supply Distribution, these HODLers' tokens are subject to a 20% APY for the vesting period (12 months). As these tokens will be unlocked after the vesting period, these HODLers can stake their INIX token on available pools to obtain rewards based on the regular APR.&#x20;
* **Public Sales Option B**: as mentioned in Initial Supply Distribution, these HODLers' tokens are subject to a 15% APY for the vesting period (18 months). As these tokens will be unlocked after the vesting period, these HODLers can stake their INIX token on available pools to obtain rewards based on the regular APY. &#x20;
* **Public Sales Option C**: since these tokens are not subject to any vesting period, the HODLers of these tokens can stake their INIX token on available pools to obtain rewards based on the regular APY. &#x20;

### Regular Staking APY

The regular APY for the Pre-Genesis period is 10%.&#x20;

### Staking Rewards Impact on Staking Rewards Pool

Initium Foundation expects 60% of the unlocked tokens during the Pre-Genesis period to be staked for obtaining the rewards by the owners.&#x20;

During the first year of the staking, \~18,150,000 INIX is estimated to be distributed among all staking HODLers, as shown in the table below.

![Estimated Staking Rewards for the First Year. Source: INIX Whitepaper. ](<../../../.gitbook/assets/Screen Shot 2022-07-17 at 11.43.56 AM.png>)

In the second year, the following assumptions are considered:

* Tokens subject to Public Sales Option A are unlocked. The owners probably stake them with a 60% staking rate. We will consider them via tokens subject to Public Sales Option C as _Others_.
* Tokens subject to Public Sales Option B will still be locked for six months and eligible to receive 20% APY for this period. After unlocking, the owners may stake them with a 60% staking rate to obtain the regular APY.

In the second year, \~14,292,500 INIX is estimated to be distributed among all staking HODLers, as shown in the table below.

![Estimated Staking Rewards for the Second Year. Source: INIX Whitepaper. ](<../../../.gitbook/assets/Screen Shot 2022-07-17 at 12.41.41 PM.png>)

In the third year, by assuming the 60% staking rate of tokens from Public Sales Options A, B, & C, it's estimated that \~12,230,925 INIX to be distributed among all HODlers, as shown in the table below.

![Estimated Staking Rewards for the Third Year. Source: INIX Whitepaper. ](<../../../.gitbook/assets/Screen Shot 2022-07-17 at 12.48.14 PM.png>)

## Post-Genesis Staking Rewards

By the [Genesis Event](../teminology.md#genesis-event) in the Initium network, the mechanism for the staking rewards will change since the rewards will become protocol-based and various factors will affect the obtained APY by the staking users.&#x20;

During this period, all INIX coins in the ecosystem are eligible to be staked and obtain APY. The main channels of participant rewards remittances are the remained reserves from the [Staking Rewards Pool](initial-supply-distribution.md#staking-rewards-pool), protocol-based rewards (block rewards and new INIX released by the Inflation Schedule), and transaction fees.

Generally, there are two major participants for receiving staking rewards:

* **Validators**: these participants will receive staking rewards from the Staking Rewards Pool based on staked INIX, transaction fees (for the transactions they verify), block rewards (for the clusters they lead as Prime Node), and Supervision fees (from the Prime Nodes for the validator squads that they supervise).
* **Staking HODLers (Stakers)**: these participants will receive staking rewards from the Staking Rewards Pool based on staked INIX.&#x20;

### Staking Methods&#x20;

There will be three main staking methods for the Post-Genesis period, including:

**1) Validator Staking Method**

Everyone can run an Initium Validator by meeting the validator requirements. Validators receive a significant reward compared to the other participants as they secure the network.&#x20;

**2) Assisted Staking Method**&#x20;

The participants who cannot run a validator can stake their INIX tokens with the validators. Validators that provide these services need to have Certified Validator Badge from IVC. In this method, validators can offer various incentives to the participants for staking their INIX tokens. The assisted staking Method is profitable for both validators and participants since:

* Validators can increase their staked INIX to become more eligible for being elected as _Prime_ or _Supervisor_ of the clusters and receive more transactions to verify in a _Validator Squad_.
* Participants can obtain more APY as their contributed validator obtains more rewards from the network.&#x20;

**3) Proxy Staking Method**

Decentralized and centralized cryptocurrency exchanges, wallets, and other staking service providers can offer their staking plans for INIX tokens. The providers of this staking method also need to run their validators to be eligible to obtain staking rewards.&#x20;

### Staking Rewards Pool

All INIX staking rewards will be remitted from the Skating Rewards Pool. Based on the [INIX Inflation Distribution Plan](inflation-schedule.md), the new generated INIX by the Inflation Schedule will be distributed as follows:

* Staking Rewards Pool: 70%
* Initium Foundation: 15%
* Initium Labs: 10%
* Initium VC: 5%

This mechanism guarantees the sufficient INIX supply to the Staking Rewards Pool and distributes most of the Inflation Rate to the participants.&#x20;

### Staking Rewards Calculation

The staking rewards during the Post-Genesis period are calculated in each epoch (about 48 hours) and distributed to the participants after the related epoch. The frequent unstaking during the epoch will significantly decrease the obtaining of rewards by the participants.&#x20;

The key factors in calculations of staking rewards are:

**1) % INIX Staked**

It refers to the ratio of total INIX staked by a given participant during an epoch to the [Total Current Supply](../teminology.md#total-current-supply). % INIX Staked is calculated as below:

$$S = INIX_s / TCS_e$$

Where

* _S_= % INIX Staked
* _INIXs_= the current staked INIX by the participant during the epoch
* _TCSe_= the Total Current Supply during the epoch

**2) Epoch Effective Rewarding Rate**

It refers to a measure for ensuring that a given participant's _S_ is reliable. If the participant frequently unstake/stake the INIX during the epoch, this rate will decrease or increase. Epoch Effective Rewarding Rate (_Er_) as below:

![](<../../../.gitbook/assets/Screen Shot 2022-07-17 at 5.47.59 PM.png>)

where:

* _n_ is the number times of changes in _Si_
* _Si is the value of S every time the S changes_
* _i variers from 1 to n_

Hint: if the participants change the _S_ five times (_n_) during an epoch, then the sum of all _S_ (_S1+S2+S3+S4+S5_) will be divided by five.&#x20;

Effective Epoch

The Effective Epoch (_e_) refers to the number of effective epochs during a calendar year. In the basic design of Initium, an epoch is valid for two days, however, this can be changed in network upgrades. Therefore, the Effective Epoch (_e_) is applied to determine the staking rewards for each epoch. The Effective Epoch (_e_) is calculated as below:

$$
e = T/d_e
$$

where&#x20;

* _T_ is the amount of time during a calendar year in seconds
* _de_ is the duration of an epoch in second

The current reserves of INIX in the subpool during an epoch are represented as below:

* _Rv_ which represents the current reserve of _Validators Rewards Subpool_, and
* _Rp_ which represents the current reserve of _Proxy Rewards Subpool._

By considering the above-mentioned variants, the staking rewards of participants will be calculated as followings:

### **Rewards Calculation**&#x20;

The following formula will be used to calculate the staking rewards for Staking Rewards **(S**_**r**_**)**

$$
Sr = E_r*R_v*e
$$

For example if:

* a validator has initially staked 10,000 INIX
* TCSs is 500,000,000 INIX
* the validator has changed the stakings during the epoch three times as (1) 10,000 INIX, (2) 12,000, and (3) 5,000&#x20;
* &#x20;the Rv is 70,000,000 INIX
* and epoch is valid for 172,800 seconds (48 hours)

then the validator estimated reward for the epoch is \~ 6.9 INIX. The estimated ROI of this validator is \~0.035 per day and 12.6% per year.&#x20;

In this example, the rewards decreased because the validator's % Staked INIX (S) decreased, which affected its Epoch Effective Rewarding Rate during the epoch. However, suppose the validator can keep its Epoch Effective Rewarding Rate stable during this epoch. In that case, his rewards from the same period will increase to \~7.672 INIX, making its daily ROI \~0.0385% and its annual ROI 14%.&#x20;

### Important Considerations&#x20;

The staking rewards in Initium are designed to incentivize the participants to contribute to the network security by running their validators or assisting them in securing the network more.&#x20;

The APY rate for the staking rewards will be dynamic in Initium and depends on various factors including:

* The number of validators: the increasing number of validators can decrease the time of the epoch which can increase the ROI of all validators as it increases the effect of _e_ in the equation. This mechanism encourages the decentralization of the network by joining more validators to the network to secure it.&#x20;
* The amount of staked INIX tokens: the increase in the staking rate of each participant will increase his APY in each epoch as it directly increases the effect of _Er_ in the equation.&#x20;
* Since the Proxy Staking Method providers also need to run their validators or cooperate with Initium Certified Valitodors, staking via these providers will make the network more secure and increase the ROI of validators.
* If in any case, the participants receive lower rewards in a given epoch, as the new tokens will be added to Staking Rewards Pool based on the Inflation Schedule, they can receive higher rewards in the next epoch.&#x20;
* The participants can conduct various staking strategies to increase their rewards.&#x20;


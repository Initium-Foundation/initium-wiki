---
description: >-
  Many terms are thrown around when discussing the crypto economic and the
  related components, we try to define and clarify some commonly used concept
  here. The article is subjected to changes.
---

# Teminology

### INITIUM

INITIUM is the native coin of the Initium network. Before launching the mainnet of the Initium network, INITIUM will be in the form of tokens on various blockchain networks including Ethereum, BSC, Polygon, etc.&#x20;

### INITIUM Conversion&#x20;

After launching the mainnet of the Initium network, all INITIUM tokens need to be converted to the INITIUM coin using the initium Bridge.&#x20;

### INITIUM TGE

Refers to the Token Generation Event of the INITIUM token, by which, the initial supply of the INITIUM will be generated and distributed among the owners.&#x20;

### Initial Supply

Refers to the supply of the tokens generated during the INITIUM TGE. The initial supply will be 500,000,000 (five hundred million) INITIUM.&#x20;

### INITIUM Distribution Plan&#x20;

Refers to the distribution plan of  INITIUM's initial supply among the stakeholders. For more information, you may visit the [INITIUM Tokenimics](../).&#x20;

### Annual Percentage Yield (APY)

The annual percentage yield (APY) is the real rate of return earned on an investment, taking into account the effect of compounding interest. Unlike simple interest, compounding interest is calculated periodically and the amount is immediately added to the balance. With each period going forward, the account balance gets a little bigger, so the interest paid on the balance gets bigger as well.

* APY is the actual rate of return that will be earned in one year if the interest is compounded.
* Compound interest is added periodically to the total invested, increasing the balance. That means each interest payment will be larger, based on the higher balance.
* The more often interest is compounded, the higher the rate will be.

The formula for calculating APY is:

$$
APY = (1+r/n)^{n-1}
$$

Where:

* r = period rate&#x20;
* n = number of compounding periods

### Total Current Supply

The total amount of coins/tokens (locked or unlocked) that have been generated (via genesis block or protocol inflation) minus any tokens that have been burnt (via transaction fees or other mechanisms) or slashed. At the network launch, 500,000,000 INI will be instantiated in the genesis block. Since then the Total Current Supply will be reduced by the partial burning of transaction fees and planned token reduction events.&#x20;

### Inflation Rate \[%]

The Initium protocol will automatically create new coins on a predetermined inflation schedule (discussed below). The _Inflation Rate \[%]_ is the annualized growth rate of the _Total Current Supply_ at any point in time.

### Inflation Schedule

A deterministic description of token issuance over time. The Initium Foundation is proposing a dis-inflationary _Inflation Schedule_. I.e. Inflation starts at its highest value, the rate reduces over time until stabilizing at a predetermined long-term inflation rate (see discussion below). This schedule is completely and uniquely parameterized by three numbers:

* **Initial Inflation Rate \[%]**: The starting _Inflation Rate_ for when inflation is first enabled. The coin issuance rate can only decrease from this point.
* **Dis-inflation Rate \[%]**: The rate at which the _Inflation Rate_ is reduced.
* **Long-term Inflation Rate \[%]**: The stable, long-term _Inflation Rate_ is to be expected.

### Effective Inflation Rate \[%]

The inflation rate actually observed on the Initium network after accounting for other factors that might decrease the _Total Current Supply_.&#x20;

* Block Rewards: as an incentive for the validators to make the network more secure, the Initium protocol will reward the validators for new block generation by block rewards. The block reward will be rewarded to the _Prime Node_ (which is elected randomly by the validators' votes).  The _Block Reward_ is subjected to halving every 4 years cycle and tends to be zero after 36 years.&#x20;
* While the _Inflation Schedule_ determines how the protocol issues INITIUM, this neglects the concurrent elimination of tokens in the ecosystem due to various factors. The primary token burning mechanism is the burning of a portion of each transaction fee. For the first 4 years, 50% of each transaction fee is burned, with the remaining fee retained by the validator that processes the transaction. Burning the transaction fees is subjected to the _Transaction Fee Burn Schedule_ and will be decreased by 15% every 4 years and will tend to zero 36 years.&#x20;
* Additional factors such as loss of private keys and slashing events should also be considered in a holistic analysis of the _Effective Inflation Rate_. For example, it’s estimated that 10-20% of all BTC have been lost and are unrecoverable and that networks may experience similar yearly losses at the rate of 1-2%.&#x20;
* Initium DAO would decide on the burning of some portion of the Initium Foundation reserves via proposals. In case of the approval of such proposals, the burning of some portion of the Initium Foundation's reserves will take place.&#x20;

### Block Rewards&#x20;

This is an incentive for the validators to keep the Initium network more secure and increase their uptime. The _Block Reward_ is determined by the _Block Reward Schedule_ and is subjected to halving every 4 years. The initial _Block Reward_ will be 1 INITIUM per Block in the first 4 years and will be zero after 36 years. The _Block Reward_ will be granted to the _Prime Node_ of each block.&#x20;

### epoch

An epoch is a time that the prime validator (Prime Node) is still valid to produce blocks of transactions. An epoch lasts roughly 2 days.

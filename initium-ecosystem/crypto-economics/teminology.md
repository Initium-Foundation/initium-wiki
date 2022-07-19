---
description: >-
  Many terms are thrown around when discussing Initium crypto economics and the
  related components, we try to define and clarify some commonly used concepts
  here. The article is subjected to changes.
---

# Teminology

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

### Block Rewards&#x20;

This is an incentive for the validators to keep the Initium network more secure and increase their uptime. The _Block Reward_ is determined by the _Block Reward Schedule_ and is subjected to halving every 4 years. The initial _Block Reward_ will be 1 INITIUM per Block in the first 4 years and will be zero after 36 years. The _Block Reward_ will be granted to the _Prime Node_ of each block.&#x20;

### **Dis-inflation**

It refers to a series of mechanisms and measures (e.g., [Fee Burning Schedule](teminology.md#fee-burn-schedule)) for reducing the [Inflation Rate](teminology.md#inflation-rate) effect on the [Total Current Supply](teminology.md#total-current-supply).&#x20;

### Effective Inflation Rate

The [Inflation Rate](teminology.md#inflation-rate) actually observed on the Initium network after accounting for other factors that might decrease the [_Total Current Supply_](teminology.md#total-current-supply). There are various factors affecting this rate, including;

* [Block Rewards](teminology.md#block-rewards)
* While the [_Inflation Schedule_](teminology.md#inflation-schedule) determines how the protocol issues [INIX](teminology.md#inix), this neglects the concurrent elimination of tokens in the ecosystem due to various factors. The primary token burning mechanism is the burning of a portion of each transaction fee. For the first 4 years, 50% of each transaction fee is burned, with the remaining fee retained by the validator that processes the transaction. Burning the transaction fees is subjected to the _Fee Burn Schedule_ and will be decreased by 15% every 4 years and will tend to zero after 36 years.&#x20;
* Additional factors such as loss of private keys and slashing events should also be considered in a holistic analysis of the _Effective Inflation Rate_. For example, it’s estimated that 10-20% of all BTC have been lost and are unrecoverable and that networks may experience similar yearly losses at the rate of 1-2%.&#x20;
* Initium DAO would decide on the burning of some portion of the Initium Foundation reserves via proposals. In case of the approval of such proposals, the burning of some portion of the Initium Foundation's reserves will take place.&#x20;

### Epoch

An epoch is a time that the prime validator (Prime Node) is still valid to produce blocks of transactions. An epoch lasts roughly 2 days. This concept is an [Initium](teminology.md#initium-1) mainnet concept.&#x20;

### Fee Burn Schedule

It refers to a protocol base schedule in [Initium](teminology.md#initium-1) for burning the transaction fees to reduce the [Total Current Supply](teminology.md#total-current-supply) of [INIX](teminology.md#inix). Fee Burn Schedule is a [Dis-Inflation](teminology.md#dis-inflation) mechanism of [Initium](teminology.md#initium-1). See [Transaction Fees](transaction-fees.md).&#x20;

### Genesis

See [Initium Genesis](teminology.md#initium-genesis).&#x20;

### Genesis Block

The genesis block is the first-ever block recorded on the Initium blockchain network, also occasionally referred to as Block 0 or Block 1. See [Initium Genesis](teminology.md#initium-genesis).&#x20;

### Genesis Event

Refers to the very first event of the [Genesis Year](teminology.md#genesis-year) by which the [genesis block](teminology.md#genesis-block) of [Initium](teminology.md#initium-1) is generated and the mainnet will be launched.&#x20;

### Genesis Inflation Rate

Refers to the [Inflation Rate](teminology.md#inflation-rate) of [INIX](teminology.md#inix) at the [Genesis Year](teminology.md#genesis-year). See also [Inflation Schedule](teminology.md#inflation-schedule).&#x20;

### Genesis Version

See [Initium Genesis](teminology.md#initium-genesis).&#x20;

### Genesis Year

In [Initium Chronology](teminology.md#initium-chronology), it refers to the first year of the launching of the Initium mainnet. The Genesis Year is a [Post-Genesis](teminology.md#post-genesis) era.&#x20;

### Inflation Rate&#x20;

The Initium protocol will automatically create new coins on a predetermined [Inflation Schedule ](teminology.md#inflation-schedule)(discussed below). The _Inflation Rate_ is the annualized growth rate of the [Total Current Supply ](teminology.md#total-current-supply)at any point in time. See [Inflation Schedule](teminology.md#inflation-schedule).&#x20;

### Inflation Schedule

Refers to the deterministic description of INIX token issuance over time. The Initium Foundation is proposing a dis-inflationary _Inflation Schedule_. I.e. Inflation starts at its highest value, the rate reduces over time until stabilizing at a predetermined long-term inflation rate (see discussion below). This schedule is completely and uniquely parameterized by three numbers:

* **Initial Inflation Rate**: The starting[ _Inflation Rate_](teminology.md#inflation-rate) for when inflation is first enabled. The coin issuance rate can only decrease from this point.
* **Dis-inflation Rate**: The rate at which the [_Inflation Rate_](teminology.md#inflation-rate) is reduced.
* **Long-term Inflation Rate**: The stable, long-term _Inflation Rate_ is to be expected.

See [Inflation Schedule](teminology.md#inflation-schedule) for further information.&#x20;

### Initial Supply

Refers to the supply of the tokens generated during the[ INIX TGE](teminology.md#initium-tge). The initial supply will be 500,000,000 (five hundred million) [INIX](teminology.md#ini).&#x20;

### INITIUM

INITIUM is the [native token](teminology.md#native-token) of the [Initium](teminology.md#initium-1). Before launching the mainnet of the [Initium](teminology.md#initium-1), INITIUM will be in the form of tokens on various blockchain networks including Ethereum, BSC, Polygon, etc. See [INIX](teminology.md#inix).&#x20;

### Initium&#x20;

When written as Initium, it refers to the Initium protocol.&#x20;

### Initium Bridge

The Initium Bridge (RedWrap) is a native application of the Initium for converting the INIX and the other tokens on the Initium to compatible versions with the different blockchains, e.g., Ethereum, BSC, Polygone, etc. The Initium Bridge commercial name is RedWrap and will be available on [https://wrap.red](https://wrap.red).&#x20;

### Initium Chronology

It refers to the different eras in the Initium ecosystem lifecycle. There are three eras as [Pre-Genesis](teminology.md#pre-genesis), [Genesis Year](teminology.md#genesis-year), and [Post-Genesis](teminology.md#post-genesis). See also [Genesis Event](teminology.md#genesis-event).&#x20;

### Initium Genesis

Refers to the main version of the [Initium](teminology.md#initium-1) by which, the mainnet of the Initium blockchain will be launched. See [Versions Design](../../about-initium/versions-design.md).&#x20;

### INIX

INIX is the symbol of [INITIUM](teminology.md#initium), the native token of the  Initium network.

### INIX Conversion&#x20;

After launching the mainnet of the Initium network, all INIX tokens need to be converted to the INIX coin using the Initium Bridge. See [Token vs. Coin](initium-tokenomics/what-is-inix/token-vs.-coin.md).&#x20;

### INIX Distribution Plan&#x20;

Refers to the distribution plan of the [initial supply](teminology.md#initial-supply) of [INIX](teminology.md#inix) among the stakeholders.&#x20;

### INIX TGE

Refers to the Token Generation Event of the token, by which, the [initial supply](teminology.md#initial-supply) of the [INIX](teminology.md#inix) will be generated and distributed among the owners.&#x20;

### Native Coin

See [Native Token](teminology.md#native-token).&#x20;

### Native Token

The native token is the primary token of a blockchain or ecosystem, which is used for various purposes like paying transaction fees, receiving staking rewards, voting, and governance. For example, Ether (ETH) is the native token of the Ethereum blockchain, BNB is the native token of BSC and Binance Exchange, and AAVE is the native token of AAVE Protocol. A native token can be hosted on another blockchain (e.g., ERC-20 or BEP-20 tokens) or a coin using its own blockchain. See [Token vs. Coin](initium-tokenomics/what-is-inix/token-vs.-coin.md).

### Pre-Genesis

In [Initium Chronology](teminology.md#initium-chronology), it refers to the period between the end of the [INIX](teminology.md#inix) official token sales course and the launch of the Initium mainnet.

### Post-Genesis

In [Initium Chronology](teminology.md#initium-chronology), it refers to the period after the Genesis Event in the Initium blockchain. It also includes the [Genesis Year](teminology.md#genesis-year) and [Genesis Event](teminology.md#genesis-event).&#x20;

### RedWarp

Refers to the [Initium Bridge](teminology.md#initium-bridge). See [RedWap](broken-reference).&#x20;

### Stakeholders

Refers to the individuals, teams, projects, platforms, validators, institutions, and organizations who contribute to the Initium ecosystem. See [Ecosystem Stakeholders](teminology.md#stakeholders).&#x20;

### Total Current Supply

The total amount of [INIX](teminology.md#inix) tokens (locked or unlocked) that have been generated (via [genesis block](teminology.md#genesis-block) or [Inflation Schedule](teminology.md#inflation-schedule)) minus any tokens that have been burnt (via transaction fees or other mechanisms) or slashed. At the network launch, 500,000,000 [INIX](teminology.md#inix) will be instantiated in the [genesis block](teminology.md#genesis-block). Since then the Total Current Supply will be reduced by the partial burning of transaction fees and planned token reduction events. See [Inflation Schedule](teminology.md#inflation-schedule).&#x20;

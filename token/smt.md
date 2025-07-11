# SMT

{% hint style="info" %}
<mark style="color:green;">Following the approval by SMT token holders of the "</mark>[<mark style="color:green;">Rewards Policy and Burn Proposal</mark>](https://vote.swarm.com/#/proposal/0xca4c31432f733cf43358df91d99c56a299ce0cc9338fcd4b8f8bc89f7da7d02e)<mark style="color:green;">", a new SMT Rewards Policy is in effect from 5th August, 2024.</mark> \
Read more [here](https://medium.com/swarm-com/swarm-adds-governance-to-smt-utility-and-proposes-to-burn-%E2%85%93-of-all-tokens-59f430a3db07).
{% endhint %}

## **Overview**

SMT is a payment token based on the ERC20 protocol on the Ethereum blockchain. SMT facilitates simplified transactions and provides a discount and reward mechanism for the Swarm platform.

SMT is part of a virtuous circle of fees, payments and [rewards](smt.md#rewards-pool) flowing through the Swarm Markets decentralized public good tools. It has the following utilities:

#### Rewards:

Special incentives are built into the token economy to reward liquidity providers who provide liquidity across the platform.

SMT Rewards will consist of three categories:

1. Liquidity Providers (Ethereum, Polygon, BASE)
2. RWA Holders (Polygon)
3. RWA Stakers (Polygon)

Regular calculations will be made to determine the TVL for each category, applying any boosts, with the weekly SMT allocated distributed proportionally to each category.

Within each category, rewards will be distributed to each wallet address proportional to their contribution to the total TVL.

### **Liquidity Provider Rewards**

Liquidity Provider rewards are distributed to wallets that make viable offers with eligible assets within the Open dOTC protocol.

**Note that as of December 2, 2024, rewards will be distributed for offers made on dOTC v2 only. Offers on dOTC v1 will no longer be eligible for rewards.**

**Boost**: Offers which include an RWA will be given a 2x boost.

**Viable offers** are those offers that are:

* live (not cancelled, expired, or fully taken),
* public (not private offers)
* in-range: priced within 20% of the current market price for the asset pair. The closer the offer price to the market price, the higher the reward.

**Eligible assets** refers to assets for which a price feed exists, including at least the following:

* Ethereum: SMT, wETH, wBTC, USDC, DAI, USDT, EUROC
* Polygon: SMT, wETH, wBTC, USDC, USDC.e, DAI, WMATIC, AAPL, TSLA, TBONDS01, TBONDS13, COIN, NVDA, MSFT, MSTR, INTC, CPNG, BLK, xGOLD

The calculated value of each offer and the period of time it is considered in-range will determine the amount of reward to the offer maker, in proportion to the total TVL of the protocol.&#x20;

### RWA Holder Rewards

Wallets which hold a balance of any of Swarm’s RWA assets (stocks, bonds and gold NFTs) will be counted by taking the value (in USD) of their RWA holdings and applying a 4x boost.

RWAs deposited as offers the Open dOTC protocol are also eligible.

### **RWA Staking Rewards**

Rewards are distributed per RWA according to the market cap of each RWA in relation to total platform TVL.

Wallets which have staked $SMT against a specific RWA will be entitled to a share of its rewards relative to all wallets staking against the same RWA.

**Other Incentives**

Swarm Markets will also distribute SMT to encourage activities that benefit the platform as a whole but may not fit one of the above criteria.

**Governance**

SMT holders an to participate in key decisions about the $SMT token, rewards policies, and the Swarm common goods services.

### **Key Data**

| **Ticker**                         | SMT                                                                                       |
| ---------------------------------- | ----------------------------------------------------------------------------------------- |
| **Type**                           | ERC20                                                                                     |
| **SMT token contract (Ethereum)**  | 0xb17548c7b510427baac4e267bea62e800b247173                                                |
| **SMT token contract (Polygon)**   | 0xE631DABeF60c37a37d70d3B4f812871df663226f                                                |
| **vSMT token contract (Ethereum)** | 0x0C033bb39e67eB598D399C06A8A519498dA1Cec9                                                |
| **Supply**                         | <p>Initial: 250 million (250,000,000 SMT)<br>Current: 158.9 million (158,879,117 SMT)</p> |
| **Initial circulating supply**     | 10.3 million tokens (10,304,259 SMT)                                                      |
| **Team allocation**                | None → 0%                                                                                 |
| **ITSA Classification**            | [https://itin.itsa.global/NS8ZK44F9](https://itin.itsa.global/NS8ZK44F9)                  |

#### Circulating Supply

{% hint style="info" %}
We recommend to use CoinGecko's metrics as reference data for token supply and circulation here: [https://www.coingecko.com/en/coins/swarm-markets](https://www.coingecko.com/en/coins/swarm-markets) which directly originates from Swarm's direct API link here: [https://api.app.swarm.com/smt\_supply/circulating/cg](https://api.app.swarm.com/smt_supply/circulating/cg)
{% endhint %}

### **Rewards Pool**

* **Up to 50% of supply**:
  * Initially 125 million tokens (125,000,000 SMT)
  * <mark style="color:green;">After the July 2024 governance vote, this has been reduced to 49.4 million SMT</mark>
  * [Currently available](https://etherscan.io/address/0x4aD8ea04079f1febCAfA345508f6b64638e936B5)
* **Launch Liquidity Program Providers:** 5 million tokens (5,000,000 SMT)
* **Distribution:**
  * Platform Rewards to (1) Liquidity provider rewards, (2) RWA Holder rewards, (3) SMT Staking rewards
  * Rewards Pool tokens will be released weekly at a diminishing rate over a 10-year period according to a regression curve representing a 11% reduction per year
  * About 1.4% will be released in the first 90 days after TGE and at a diminishing rate thereafter, starting at a rate of slightly under 0.5% per month until all Rewards Pool tokens have been released.
* **Rewards Distribution Logs:**
  * SMT reward distribution logs including a list of addresses and reward amounts are published regularly on the [Swarm Markets SMT Rewards Distribution](https://github.com/SwarmMarkets/smt-rewards-distribution) Github repo.
* **Current Rewards Policy** may be found at [https://github.com/SwarmMarkets/smt-rewards-distribution/blob/main/policies/smt\_rd\_policy.md](https://github.com/SwarmMarkets/smt-rewards-distribution/blob/main/policies/smt_rd_policy.md)

### **Reserve**

* **Up to 20% of supply:**
  * Initially 50 million tokens (50,000,000 SMT)
  * <mark style="color:green;">After the July 2024 governance vote, this has been reduced to 7 million SMT</mark>
  * [Currently available](https://etherscan.io/address/0x857cc51F07924B82e931B473131c965415d070f6)
* **Distribution:** Reserved for future use; assumed 5-year linear release starting 3 years from TGE

### **Community Pool**

* **Up to 10% of supply:**
  * Initially 25 million tokens (25,000,000 SMT)
  * [Currently available](https://etherscan.io/address/0xf0756b4150feE6deF4c9d5172DA029cc2Ca29B36)
* **Distribution:** 1.25% distributed per quarter

### **---- NO TEAM ALLOCATION! ----**

## **Vesting and Distribution**

The rate at which SMT tokens enter circulation will be controlled by Swarm in order to ensure stable valuation and adequate rewards across the platform’s various stages of growth.

![](https://lh4.googleusercontent.com/9oDacM5JXg7jCH_UzgRACl-3GRhPpGM9HwMHXVZOqfobAoSm9Xf0cNKYxbXcoRiCc6Wwt4-uGsFOyFXYjFtGP7C3Te2fvt4mUK7lE6g6WFYg4eUDnZJrsqV3ouPd_exjfPAskUBJ)

Vesting is enforced by wrapping SMT. Tokens will appear as [vSMT](https://etherscan.io/address/0x0C033bb39e67eB598D399C06A8A519498dA1Cec9) in your wallet until they are vested at which point they can be converted to SMT. vSMT cannot be transferred, staked, or traded. SMT can be transferred without restriction.

The vesting schedule and distribution model has been designed with fairness as top priority and with the goal to release about half the maximum supply towards the end of year 3. Rewards Pool tokens are released over the course of 10 years at a rate which diminishes each week.

vSMT holders are able to unwrap and convert 20% of their holdings at the Token Generation Event (TGE) on August 1st, 2021 12:00 CET. An additional 20% of vSMT (of the original purchased amount) will be available to unwrap per quarter thereafter with 100% vesting after 12 months. There is no time limit to when vSMT holders must unwrap their vSMT and convert to SMT.

#### Vesting Dates: Monday, November 1st, 2021 Tuesday, February 1st, 2022 Tuesday, 3 May 2022 Tuesday, 2 August 2022

_Note: all vesting events will take place according to block date, not calendar date. As such, the calendar date schedule listed above is an approximation only. Depending on the pace of mining on the Ethereum blockchain, the block date may be earlier or later than the estimated calendar date._

## Governance

At [vote.swarm.com](http://vote.swarm.com/) or directly at [snapshot](https://snapshot.org/#/swarm-com.eth/proposal/0xca4c31432f733cf43358df91d99c56a299ce0cc9338fcd4b8f8bc89f7da7d02e) SMT holders can participate in key decisions about the $SMT token, rewards policies, and the Swarm common goods services.

Swarm Markets DAO has been set up and registered in Marshall Islands. SMT token reserves are governed by eligible members of the Swarm Markets DAO LLC formed under the Associations Law, 52 MIRC, Part 1, of the Republic of the Marshall Islands and under License Number RMI-2024-65 under the Foreign Investment Business License Act.

{% file src="../.gitbook/assets/Swarm Markets DAO LLC - Corporate Charter and FIBL.pdf" %}

## Unwrapping vSMT to SMT

Follow the step-by-step guide below to unwrap vSMT and convert it to SMT. Once your vSMT is unwrapped to SMT, it is fully functional: it can be transferred, traded or staked on any ERC20 compatible platform.

![vSMT dapp on etherscan, click to enlarge](<../.gitbook/assets/image (33).png>)

1.  Select the wallet that holds your vSMT in [MetaMask](https://www.metamask.io) and make sure that same wallet has enough ETH to cover gas for transaction costs. You will also want to make sure both vSMT and SMT are [added as custom tokens](https://metamask.zendesk.com/hc/en-us/articles/360015489031-How-to-view-see-your-tokens-custom-tokens-in-MetaMask) in that wallet:

    vSMT token contract address: 0x0C033bb39e67eB598D399C06A8A519498dA1Cec9 symbol: vSMT, decimals: 18

    SMT token contract address: 0xb17548c7b510427baac4e267bea62e800b247173 symbol: SMT, decimals: 18
2. Go to the vSMT smart contract: [https://etherscan.io/token/0x0C033bb39e67eB598D399C06A8A519498dA1Cec9#writeContract](https://etherscan.io/token/0x0C033bb39e67eB598D399C06A8A519498dA1Cec9#writeContract)
3. Under the Contracts header, make sure Write Contract is selected.
4. Connect your wallet by clicking the red "Connect to web3" button.
5. Add bot vSMT and SMT to your wallet as custom tokens, if you haven't already:
6. To unwrap vSMT, go to the operation 4. claimMaximumAmount and click Write.
7. This should open Metamask with the transaction. Click Confirm.

## SMT - Release Schedule

{% embed url="https://docs.google.com/spreadsheets/d/13XTheJLsMDjeZUs9HGYUkjN6hA5BtsA-u6oRMrf24Ug/edit#gid=1498811951" %}

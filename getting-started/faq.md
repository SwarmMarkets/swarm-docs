# FAQ

#### Can't find the answer you're looking for? Ask your question in our [community Discord](https://discord.swarm.markets).

#### **What is an AMM?**

An AMM, or Automated Market Maker is a general term that defines an algorithm for creating and managing liquidity. [Learn More](../reference/amm.md)

#### **What is the difference between Swarm and other AMMs?**

Automated Market Maker (AMM)-based decentralized exchanges (DEX) have proven to be one of the most impactful DeFi innovations. While existing AMMs have created an exciting and thriving protocol layer, their activity is performed outside of financial market compliance. Swarm has created a regulatory layer on top of open DeFi protocols, starting with a multi-asset AMM solution pioneered by the [Balancer protocol](https://balancer.finance).

#### **What are the platform fees?**

Swarm charges no fees for adding or removing liquidity.

Traders pay fees calculated as a percentage of the swapped asset traded against a pool. Fees are specific to each pool and set by the pool creator. There are two components to these:

1. Swap Fee: a customizable fee per pool which is distributed among the pool's liquidity providers, and
2. Protocol Fee: a fee for Swarm, set as a percentage of the Swap Fee.

[Learn More](../advanced/fees.md)

#### **Is Swarm decentralized?**

Swarm makes every effort to be as trustless as possible. The core AMM protocol is built on open and battle proven trustless technology. To remain regulatory compliant, Swarm is mandated to qualify market participants and the assets allowed into the protocol.

#### **Under which regulation is Swarm operating?**

In terms of regulatory licensing requirements, Swarm Capital GmbH operates under the exemption according to section 64y of the German Banking Act (Kreditwesengesetz – “KWG) and is regulated by the German Federal Financial Supervisory Authority (BaFin). [Learn More](../about/license.md)

#### Are there any limitations on using Swarm ? <a href="#limitations" id="limitations"></a>

Transacting on Swarm is currently not available for US persons (as defined [here](https://en.wikipedia.org/wiki/United\_States\_person)) or persons that hold identities from other countries not serviced. US persons and users from non-serviced countries may connect a wallet and view their assets, but will not be able to set up a trading account.

Swarm is currently available to users resident in Argentina, Armenia, Australia, Austria, Azerbaijan, Belgium, Bermuda, Brazil, Bulgaria, Canada, Cayman, Chile, China, Croatia, Cyprus, Czech Republic, Denmark, Estonia, Eswatini (formerly Swaziland), Finland, France, Germany, Gibraltar, Greece, Hong Kong, Hungary, Iceland, India, Indonesia, Ireland, Israel, Italy, Jamaica, Japan, Jersey, Latvia, Liechtenstein, Lithuania, Luxembourg, Macau, Malaysia, Malta, Mauritius, Mexico, Monaco, Netherlands, New Zealand, Norway, Peru, Philippines, Poland, Portugal, Romania, Singapore, Slovakia, Slovenia, South Africa, South Korea, Spain, Sweden, Switzerland, Taiwan, Thailand, Turkey, Ukraine, United Arab Emirates (UAE), United Kingdom (UK), Uruguay, und Vietnam.\
\
**What is Swarm useful for?**

Firstly, to serve any market participants who value the core benefits of DeFi (self-custody, transparency, participation), but want to remain compliance confident and keep their digital assets future-proof

Secondly, on the basis of Swarm's licensed protocol layer entirely new financial products can be launched and offered, extending DeFi pretty much to any financial asset and to integrate with financial institutions.

#### I have no crypto. Where do I start? <a href="#get-crypto" id="get-crypto"></a>

To use Swarm you will need to have at least one of the supported assets in your connected wallet. A good place to start is with Ethereum (ETH) or Dai Stablecoin (DAI). Here are some options for obtaining these assets:

* Ethereum (ETH):
  * Metamask: Open Metamask, navigate to the Assets tab, select ETH and click Buy.
  * [https://ethereum.org/en/](https://ethereum.org/en/)
* Dai Stablecoin (DAI):
  * [https://oasis.app/](https://oasis.app)

#### **Why is the platform not working?**

If you have trouble loading the platform, connecting your eth address or any other kind of loading issues, please check the security settings and tracking blockers that you browser might be using. Some of these services block necessary Javascript needed to run the Swarm Markets platform properly. We recommend disabling enhanced tracking protections (including any adblockers) for our web app only so that other tracking protection is unaffected for other internet browsing. No cross-site tracking, cryptominers, or any hidden software are implemented on the platform web app.

#### **Why is my swap expected to fail?**

If you receive a general error message that your swap is expected to fail, it may be due to:

* Authorization not yet set: If you just completed Quickstart onboarding, please allow the protocol a minute or two to authorize your address on the blockchain. You will receive an email as soon as this is complete.
* Trading Limit: If you haven't fully completed setting up your Passport, your account trading limit is set to a total of 5,000 EUR. All transactions on the platform (swaps, adding and removing liquidity) count to wards your limit. Check your passport for instructions on how to remove this limit.
* Low liquidity: One of the pools required to fulfil your swap has insufficient liquidity to complete your order.
* High Slippage: Low liquidity can also result in high slippage, meaning that the actual price may be significantly unfavourable compared with the expected price. Try increasing your acceptable slippage level in advanced settings. Note that this could result in an unfavourable swap price.

#### **What are the risks?**

While DeFi and AMMs have been somewhat battle proven, they are very new protocol technologies. Swarm is introducing new layers which could introduce both additional risk and de-risk certain use cases. We are taking every precaution and doing [extensive audits](https://app.gitbook.com/@swarm/s/swarm-markets/reference/smart-contracts/smart-contract-audit), but this is still very much a beta product. Use small amounts of funds to start.

#### **What are proxy contracts and atomic transactions?**

Swarm uses proxy contracts to save you gas fees when transacting. Creating your proxy address adds a little gas to your first transaction but results in lower fees and a better user experience over time.

When making your first transaction via the UI, the Swarm protocol checks whether you have previously deployed a proxy contract and bundles the creation of one into your first transaction if you have not. Your proxy contract is a [Gnosis Safe](https://gnosis-safe.io) and can be used with any Gnosis Safe Application.

Proxy contracts allow complex multi-step transactions to be batched into a single atomic transaction that requires only a single verification. An atomic transaction will revert if any part of the transaction is expected to fail so that you won’t be charged any gas fees for a failed transaction. This saves you money over time and improves the user experience by making transactions much simpler. Proxy contracts also hold your wrapped assets and pool tokens, saving you the gas fees that would otherwise be charged when transferring these assets to your primary wallet address.

Note: your proxy contract is created, owned, and controlled by your connected primary wallet address. No other address can instruct your proxy in any way.

#### Why is there a balance in my proxy address?

Some platform transactions can result in a small percentage of your assets remaining in your proxy address. This occurs when there is a difference between the estimated amount of asset being transacted and the actual amount used when the transaction is mined.

**How do I use or claim the balance in my proxy address?**

When swapping or interacting with liquidity pools, the platform will automatically use any relevant balances from your proxy address before withdrawing funds from your user address. Therefore, the simplest way to minimise the balance in your proxy address is by transacting.

You will always have the option to simply claim your entire proxy balance through your platform [Wallet](https://trade.swarm.markets/wallet) at any time.

In the meantime, balances in the proxy wallet count towards rewards calculations.

#### How does the product roadmap look like?

Here is a [framework of what we are working on in 2023](https://swarm.com/roadmap-2023/).

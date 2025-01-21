---
description: Decentralised over-the-counter trading
---

# dOTC

Swarm’s decentralized over-the-counter trading (dOTC) service enables institutions to carry out large transactions on the Blockchain.

High-volume swap activity is increasing significantly. Large volume-based trading OTC for digitized assets is costly, complex and often difficult to execute. Our dOTC service empowers institutions and retail investors to use a block-trade smart contract in place traditional OTC trading.

#### How it works

The peer-to-peer (P2P) contract will facilitate high-value transactions, reduce slippage and remove counterparty risk, as all users on Swarm are verified.

Despite high value trades being on the rise, to date, there has not been an institutional-grade trading tool available.

Swarm clients place a buy or sell order into the market for eligible assets, using the dOTC contract. Much like an escrow account, assets held by the smart contract can only be redeemed to a crypto wallet once all terms have been fulfilled.

The smart contract replaces the need for financial intermediaries, typically found in complex and costly OTC trading arrangements in traditional financial markets.

Sign up here at [app.swarm.com](https://app.swarm.com/dotc/) or email us: [swarm@swarm.com](mailto:swarm@swarm.com).

## dOTC V2 - Now live on [app.swarm.com](https://app.swarm.com) <a href="#f4ee" id="f4ee"></a>

The release of dOTC V2 supports growing liquidity for real-world assets on-chain and beyond, making the user experience more superior and efficient.

The release consists of five new core features:

1.  **Dynamic Pricing**: Offer prices can be set in reference to an external price oracle, meaning they continually move with the market and do not need updating. This represents vast savings in transaction costs as offers need to be set only once. Dynamic prices are set as a percentage to the oracle price, allowing premiums or discounts to market price.

    <figure><img src="../.gitbook/assets/image (1).png" alt="" width="344"><figcaption></figcaption></figure>

    <figure><img src="../.gitbook/assets/image.png" alt="" width="563"><figcaption></figcaption></figure>
2.  **Order matching for instant swapping:** The new Swap page provides price quotes for any pair of assets with live offers in the order book, combinging the convenience of liquidity pool trading with the benefit of no slippage.

    <figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>
3. **Better discoverability**:
   1. app.swarm.com: dOTC will be available under [app.swarm.com](http://app.swarm.com/) while still independently accessible under [dOTC.eth](http://dotc.eth/)
   2. Discover:
      1.  Explore and filter all available offers in an easy to read orderbook, where users can also find their own offers and any private offers intended just for them.

          <figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>
      2.  &#x20;Offers can be easily viewed and managed in the My offers tab

          <figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>
   3.  Shareability: Sharing offers into social channels is as easy as sharing items on Amazon

       <figure><img src="../.gitbook/assets/image (3).png" alt="" width="563"><figcaption></figcaption></figure>

**3. Offer terms and communications**: Offers can now include links to terms and communication channels to enable comms between makers and takers who wish to negotiate a deal or highlight specific terms

**4. KYC select**: Offer makers can now require counterparties to be qualified and choose from a selection of KYC/AML service providers, including, for example, Swarm Markets. This feature provides an additional compliance layer that sits on top of open and permissionless infrastructure, to provide fully regulatory institutional trading. See [here](../reference/kyc-select.md) for more details and technical implementation.

**5. Affiliate participation**: affiliates can earn rewards from embedding dOTC offers into their platform with payouts being distributed in real-time from each transaction.

## Frequently asked questions

#### What makes your dOTC offering different to others in the market?

This is the first crypto block-trade smart contract from a compliant entity that institutions and professional investors can use in place of traditional over-the-counter (OTC) trading, which disintermediates trading.

Our offering includes additional unique features such as:&#x20;

**Partial orders** - dOTC supports partial or all-or-nothing type orders, configurable by the maker.&#x20;

**Private offers** - Makers can specify the taker address that the order is intended for. Only that address can execute on the order.&#x20;

**Offer expiration** - Makers can specify whether their offer stays live in the market indefinitely or automatically expires at a future date.

#### How do I trade using dOTC?

#### Swaps

1.  Start on the Swap page by selecting the assets you'd like to sell and the asset you would like to buy. If you cannot find the asset you're interested in, simply paste it's contract address into the token selector and we'll find it for you.&#x20;

    <figure><img src="../.gitbook/assets/image (9).png" alt="" width="240"><figcaption></figcaption></figure>
2.  Enter an amount to see the best aggregated quote currently available. The Swap page automatically selects as many offers as required to fill your order.

    <figure><img src="../.gitbook/assets/image (8).png" alt="" width="235"><figcaption></figcaption></figure>
3. Click "Preview Swap" to proceed and confirm the transaction in your connected wallet.&#x20;

#### Limit offers

Limits allow placing an offer into the orderbook at above or below market price. Limits can be set at a fixed price or to float at a specific percentage relative to the market price dynamically. The dOTC platform uses price oracles to track the current market prices of assets and maintain the offer price at the appropriate level.&#x20;

Limit offers feed into the Swap interface and can be taken individually or as part of a multi-offer transaction.

<figure><img src="../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

Dynamic priced limit offers - An example:

* AAPL is currently trading at 242 USD.
* You would like to place a dynamic limit offer to sell AAPL at 10% above market price.
* This means that as the current market price of AAPL moves up or down, your offer price always stays 10% above it.
  * When AAPL is trading at 242 USD, your offer would be priced at 266.2 USD
  * When AAPL is trading at 250 USD, your offer would be priced at 275 USD
  * When AAPL is trading at 220 USD, your offer would be priced at 242 USD

Similary, you may wish to trade at below market price, which works in the exact same way.

Offer makers can always see the current price of their offers in the Discover / My Offer tab.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

#### Making a limit offer

Similarly to Swaps, start by selecting the assets you would like to offer and buy. You then have a number of options to customize your offer:

*   **Fixed vs Dynamic Pricing:** Set a fixed price or a dynamic price for your offer. Dynamic prices can be set at market, up to 100% above market or up to 100% below market price. Note that dynamic offers are only available for assets where a price feed is available.

    <figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>


* **Expiration:** Set how long you would like your offer to be valid for. Select from the provided options or use a calendar to set the expiration as accurately as you need.
* **OTC settings:** Additional options for professional traders are available under the OTC settings menu.
  * Private offers: To restrict your offer so that it can only be taken by specific counterparties, enter their address here. Multiple addresses are supported, allowing any of the specified wallets to take part or all of your offer
  * Timelock: This is an optional feature, which allows the maker to commit to a price for a specific period of time in days. During the timelock period, the offer cannot be edited or cancelled.
  * Block order: By default, all offers are set as **partial offers,** meaning that they can be taken in parts. Checking the Block offer option restricts your offer to be taken as a single block, all or nothing.&#x20;

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

#### What is the fee for dOTC?

Fees for dOTC trading are 0.25% and are paid by the Maker only in the case of an offer being successfully taken. Canceled offers are not subject to any fees.

When making an offer, the Maker enters a price and is provided a quote for the expected amount of asset they would receive if the offer is taken, less the 0.25% fee.

#### Will SMT discounts be available on dOTC?

Discounts for paying fees in SMT will be introduced in future upgrades to the service.

#### What is the significance of this product?

dOTC simplifies one of the most complex areas of crypto OTC trading for large block trades.

dOTC enables contract-based block trades for both crypto and as well as real world assets, with verified counterparties, extending cost and time savings available to high volume traders.

#### **What assets will be available to trade dOTC?**

The dOTC system supports the full range of digital assets encompassing the ERC20, ERC721 and ERC1155 standards.

This enables participants to trade high value NFTs and to facilitate smoother liquidation of crypto positions.&#x20;

#### Will there be a minimum order size on dOTC?

There are no minimum order sizes required on dOTC.

# Pools

## **In general**

Swarm liquidity pools allow any user to provide liquidity via [app.swarm.com](https://app.swarm.com)

When adding liquidity to a pool from an Ethereum address, users receive Swarm Pool Tokens (SPT) to that address, which represent the proportion of the pool's liquidity they own. When users add liquidity they receive SPTs proportional to the amount of assets they are adding to the pool.

For example, if a user deposited $WBTC and $ETH into a pool they would receive WBTC-ETH SPT tokens. These tokens represent a proportional share of all the assets in that pool, allowing the user to reclaim their funds at any point.

Every time a trade occurs between $WBTC and $ETH using this pool, the pool-specific swap fee plus the Swarm fees is taken from the trade. The pool-specific swap fee goes back into the pool and is added to its assets, ever increasing its market cap. If previously there were 100 SPT tokens representing 100 ETH and 100 wBTC each token would be worth 1 ETH & 1 wBTC. If one user now traded 10 ETH for 10 WBTC, and another traded 10 WBTC for 10 ETH, then there would now be the 100 ETH, plus 100 WBTC, plus trading fees for two trades. This means the prorated amount that SPT represents has now increased by the same amount when it is withdrawn.

## Setting up your proxy contract.

Before you make your first transaction on the Swarm platform, you will receive this notification:

![pop up that will appear during your first transaction.](<../.gitbook/assets/image (12).png>)

Swarm uses proxy contracts to save you gas fees when transacting. Creating your proxy address adds a little gas to your first transaction but results in lower fees and a better user experience over time. You will have to sign off on activating your proxy contract on any new eth contract you might connect to Swarm and want to enact a transaction from [Learn more](https://docs.swarm.markets/getting-started/faq#what-are-proxy-contracts-and-atomic-transactions)

After you sign off on the proxy contract set up, you will be taken back to the Pools page.‌



## **Adding liquidity to an existing pool**

‌You can add tokens to a pool in two ways:

1\. **Add multiple assets**: You can provide all tokens in the configured ratio of the liquidity pool. This means that if you are adding to, say, a pool with 50% WBTC and 50% ETH, and wish to provide 2 ETH worth of liquidity, you would also need to provide an equivalent value of wBTC tokens alongside.

![](<../.gitbook/assets/image (17).png>)

2\. **Add single asset:** You can provide tokens using only one of the assets of the liquidity pool. This is particularly useful when you do not have all the assets required for a pool. You can deposit one of the assets (either WBTC or ETH in our example). There is now a price advantage to buy the token that is creating the imbalance in the pool, thereby maintaining the proper pool token ratio through swapping and trading on the platform. There are certain limits to this based on pool liquidity and making sure the pool doesn't become too imbalanced.&#x20;

![](<../.gitbook/assets/image (35).png>)

## ‌**Creating a new pool (coming soon)**

If the pool you wish to provide liquidity to does not exist, soon you will be able to create it! Any user can create a new pool using any combination of assets supported by Swarm. The caller is set as the pool creator.

![](<../.gitbook/assets/image (28).png>)

As the pool creator and first liquidity provider, you set the following parameters:

* Initial assets and amounts
* Asset weights
* Swap fee

This often quickly corrects itself through arbitrage and by more liquidity providers adding to the pool.

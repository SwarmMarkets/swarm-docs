# Fees

## Pool swap fees

Amongst the the custom settings for the pool, the pool initiator (pool owner) sets the pool swap fee.

Pool swap fees are collected out of each transaction within the pool and added to the pool liquidity reserves. This increases the value of liquidity assets, functioning as a payout to all liquidity providers proportional to their share of the pool. Fees are collected by burning liquidity tokens to remove a proportional share of the underlying reserves.

Since fees are added to liquidity pools, the invariant increases at the end of every trade. This fee is split by liquidity providers proportional to their contribution to liquidity reserves.

## Protocol Fees

The protocol fees are calculated as 25% of each Pool's swap fees, or 0.1% of the assets being swapped, whichever is larger.

Protocol Fees are taken from each swap transaction before they enter into the pool swap. The collected amounts are made claimable to Swarm.

This amount does not affect the fee paid by traders, but affect the amount received by liquidity providers.

### SMT Protocol Fee Discount

Swarm will be distributing a payment token SMT. Traders who hold a sufficient amount of SMT in their wallets can have the protocol collect the Protocol Fee in SMT instead of from the swapped asset. This reduces the protocol fees (if paid in SMT) by 50%.

Paying the Protocol Fee in SMT is optional and can be set by the user. Traders need to have sufficient SMT in their trading wallet to cover the entire reduced Protocol fee amount.

You can earn SMT e.g. [by providing liquidity and through other incentives](../token/smt.md).&#x20;

## Examples

### Standard Swap

Swap Fee for the pool is set to 0.40%. Protocol fee of 20% is 0.08% (20% x 0.40%), making the total fees 0.48% of assets being swapped. If a trader is swapping 10 ETH, the fee is 0.048 ETH (0.48% x 10 ETH).

### Swap with SMT Hodler Fee Discount

Swap Fee for the pool is set to 0.40%. Protocol fee of 10% is 0.04% (50% discount \* 20% x 0.40%), making the total fees 0.44%. The Swap fee is collected in the assets being swapped, whereas the Protocol fee is collected in SMT. If a trader is swapping 10 ETH, the fee is 0.040 ETH (0.40% x 10 ETH) and 0.04% in SMT.

\\

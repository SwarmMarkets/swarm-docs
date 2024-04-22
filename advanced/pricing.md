# Pricing

## Summary

Swarm pools are tokenized portfolios that function as AMMs.

The primary changes made to the contract are only a permission layer that creates compatibility with Swarm Passports and whitelisted assets.

<figure><img src="../.gitbook/assets/Networked Liquidity.png" alt=""><figcaption></figcaption></figure>

## How are prices determined?

Each pair on Swarm is actually underpinned by a liquidity pool. Liquidity pools are smart contracts that hold balances of two or more unique tokens and enforces rules around depositing and withdrawing them.

The primary rule is the constant product formula. When a token is withdrawn (bought), a proportional amount must be deposited (sold) to maintain the constant. The ratio of tokens in the pool, in combination with the constant product formula, ultimately determine the price that a swap executes at.

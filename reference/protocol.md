# Protocol overview

## Summary

Swarm is a compliance protocol layered on top of an AMM. The pool contract is designed to be able to allow qualified users to access liquidity for qualified digital assets without the need for a centralized entity to facilitate the trades.

The smart contracts for the Swarm AMM functionality are a fork of the [Balancer Protocol](https://github.com/balancer-labs/balancer-core/blob/master/contracts/BPool.sol). The primary changes made to the contract are only a permission layer that creates compatibility with Swarm Passports and whitelisted assets.

{% hint style="info" %}
For reference, please refer to the Balancer [Whitepaper](https://balancer.finance/whitepaper/) and [documentation](https://docs.balancer.finance) for additional context on the pool contract.
{% endhint %}

##

---
description: >-
  Overview of the xToken smart contracts and how they interact with the Swarm
  Protocol
---

# xTokens

Any transaction on the Swarm Platform (e.g. the AMM) requires the use of a xToken. An xToken is an ERC-20 compliant representation of balances (“**Token**”) supplied to the protocol. The xToken reflects that the holder of the xToken is entitled to retrieve the Token from the Swarm Platform if the holder sends the request to the Swarm Protocol. The common wording to describe an xToken is a "wrapped" token.

Such wrapped token may just mirror the functionalities of the Token or can have different functionality which is the case for the xToken as described in the following.

The xToken protocol checks that the address intending on transacting with the Token has permissions (i.e. is an onboarded user, has correct trading permissions as applicable to the given asset, etc) to interact with it. It acts as a permissioning layer for all transactions that take place on Swarm, allowing us to fulfill our compliance obligations and keep user data secure and anonymous on the platform.

The User has mandatorily a so-called proxy wallet address which is used to bundle transactions for efficiency and to save on transaction fees (see the FAQ on Proxy Contracts for more information). xTokens only are transferred to proxy wallet addresses or to pools but never to the wallet address of the User. xTokens can only be used on the Swarm platform for the purpose of either transacting with a pool or for liquidity providing into a pool. Therefore, xToken’s cannot leave the platform to be used in any other form, particularly it cannot be transferred into a wallet on the Swarm Platform or a wallet outside of it.&#x20;

Each Token provided into the Swarm Protocol will have a corresponding xToken. For example, WETH has a corresponding xWETH and WBTC has a corresponding xWBTC. Again, these xTokens are non-transferable and exist only in your Proxy Wallet or on a platform pool. &#x20;

Users must hold a qualified Swarm passport to be able to interact with the xToken assets. To have a Swarm passport, users must undergo KYC and AML checks. Each user holds the same xToken assets; there’s nothing unique to your wallet address or account.

Here's an example of a simple transaction on the platform, demonstrating how xTokens are minted, distributed on the platform, and managed by the user's proxy wallet (CPK in the illustration below). In this transaction, the user is depositing 1000 SMT into a liquidity pool:

![xToken minting and distribution in the transfer of a single asset to a liquidity pool](../.gitbook/assets/xTokenTransactions\_Cropped.png)

First, the original asset (in this case, SMT) is transferred from the user's web3 wallet address to their proxy wallet address (CPK). The proxy wallet then transfers the tokens to the xTokenWrapper, which initiates a minting of the xToken (xSMT) and sends it to the proxy wallet address. Then the pool proxy address (BPool Proxy) forwards the xSMT to the correct pool, completing the addition of liquidity to the pool. Pool tokens (xSPTs) that represent the user's proportion of the total pool’s liquidity are minted and sent back to the user’s proxy wallet.

If the user wants to exit their position in the liquidity pool and unstake their assets, the process is reversed. If the user provides two assets (or more) into a pool, this process is duplicated for each asset staked.&#x20;

## Swarm xTokens

The Swarm Protocol currently provides xToken wrapping for the following assets:

#### Ethereum Network

| Token     | Native Asset                               | xToken                                     |
| --------- | ------------------------------------------ | ------------------------------------------ |
| **SMT**   | 0xB17548c7B510427baAc4e267BEa62e800b247173 | 0xeE3A72A79D1c0f22B53BEfE1dCB9F11682126772 |
| **wETH**  | 0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2 | 0x43c28c4a103d939097dc4d9b20c327148f13c4c6 |
| **wBTC**  | 0x2260fac5e5542a773aa44fbcfedf7c193bc2c599 | 0xfc6274505d08210117c56b541794a72338ed3fb6 |
| **USDC**  | 0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48 | 0x80e32d09fbeaa6aa01d76aa68024670e8db8a953 |
| **DAI**   | 0x6b175474e89094c44da98b954eedeac495271d0f | 0x6ceb875d9e8d75e0e68040d9bb63b21de134e843 |
| **EUROC** | 0x1aBaEA1f7C830bD89Acc67eC4af516284b1bC33c | 0xd573ea715f9ad5864eb5cbb8bbbfb2b91b1cafcb |

#### Polygon Network

| Token        | Native Asset                               | xToken                                     |
| ------------ | ------------------------------------------ | ------------------------------------------ |
| **WBTC**     | 0x1BFD67037B42Cf73acF2047067bd4F2C47D9BfD6 | 0x54A3E68cA7C59Df9b95A5993FB257B455C628e54 |
| **WETH**     | 0x7ceB23fD6bC0adD59E62ac25578270cFf1b9f619 | 0x92aEB125534C08B3872f353C46453229f7af0AfF |
| **USDC**     | 0x2791Bca1f2de4661ED88A30C99A7a9449Aa84174 | 0x4A573b521b143f3e8032C3665b0Ab307b17F7bcf |
| **DAI**      | 0x8f3Cf7ad23Cd3CaDbD9735AFf958023239c6A063 | 0xd041806f89D24aa279a1d923f6127B12D03b00F5 |
| **SMT**      | 0xE631DABeF60c37a37d70d3B4f812871df663226f | 0xCF7d93aC1B6a527025Ae823B25D5D3d91389d282 |
| **WMATIC**   | 0x0d500b1d8e8ef31e21c99d1db9a6444d3adf1270 | 0xc228a3b1a514d3b8431255f0184711e9601a765e |
| **SOL**      | 0xd93f7E271cB87c23AaA73edC008A79646d1F9912 | 0xde92ed6B3c461Ed57a09819f9479885673aad14F |
| **SOLsn**    | 0xd98388bf3e062fc77a1a456a634f2b2dc5d1bb6e | 0xDBCd4A495FfE8D808eD0F3429fAD18d94D6588a6 |
| **NEARsn**   | 0x80F8AdE10c21514Eed63fA52928Ea41dE33C5365 | 0xfa5d77a560e1d23caf90bd68a7bf1e79b28bf1d1 |
| **DOTsn**    | 0x02BA39888444c6277F7A6dFcb9a58b64FB3BEff3 | 0xDef0BA801597BCa70b5de03310Cc52cBaaE9C8d2 |
| **ETHsn**    | 0xf3cDA4E9f10D81151ffBFfd2C1527E42093B4542 | 0xf300557D3490B4BDcc080b71f86811C141c3242c |
| **AVAXsn**   | 0xCF9AC0929e2195a4d1f0327D3e54EFa9D3d83523 | 0x6690cf54ab0f5c8e84952d1ad1c8f8d9aee9a511 |
| **AAPL**     | 0xa13e07B145Cd28294447DD271Ea0F158727976bE | 0xA494f2018458D9D4eaA46b488F8A7A499A740656 |
| **TSLA**     | 0x7FCFa7F21c9390eEB2C0158A892B817bCA5FBafb | 0xBAa20599efDBe274f1c1E0E24417677f2aB85F37 |
| **TBONDS01** | 0xf4D24F4E0Ce54760788B0A0FB352BCC34e7d045f | 0xCd83547F2482b2071F04a048A7AC8CAd0B78e814 |
| **TBONDS13** | 0x60f9971aEA32B1b3B369a1fabC435A15c048D0F0 | 0x7a7E7e87D7F46C262b0E2556A65BCcfF5BE76e3a |
| **COIN**     | 0x1020d03B5C19D3963484CD8AD8af7e159FD5E261 | 0x6c053946a8071ae7f52dc9a2b89dd5796a3e46f3 |
| **NVDA**     | 0x0493fA5965963AB9fc587e1DD165C03Cc8304226 | 0x650b83cab386b9dc5a33e3a9fe4de26d0e61ec9c |
| **MSFT**     | 0x7A0C829Bc6c06eC71Bf0db04e62CDc8863133553 | 0xfb9a93257715063ac0a766de5c1b3f588f21f7ac |
| **MSTR**     | 0xE61Aa4E693D3EF8Ebc8Cd901df2fE1f0a6e2ce78 | 0x1d0cc7eda325b2680669843e6deb191649893d1a |
| **INTC**     | 0x4BCDb11ac9Ed682db431cCdddbdB0Ea7d6a0F9D2 | 0x2b436b1acbc116308316909274b91a1e9bd76cab |
| **CPNG**     | 0xE979088BA73977EE0095A30A43F44AEC1D45cA0e | 0x1437e35190401a66506a0f1c5e7846ee3e5a53ff |
| **BLK**      | 0x7F72de249ed11d8d33845B8459105caf6ac604A5 | 0x609b637b2f637ca0f93da62a1b19eb07760c6be8 |

## Further Reading

{% content-ref url="xtokens.md" %}
[xtokens.md](xtokens.md)
{% endcontent-ref %}

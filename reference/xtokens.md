---
description: >-
  Overview of the xToken smart contracts and how they interact with the Swarm
  Protocol
---

# xTokens

Any transaction on the Swarm Platform (e.g. the AMM) requires the use of a xToken. An xToken is an ERC-20 compliant representation of balances (“**Token**”) supplied to the protocol. The xToken reflects that the holder of the xToken is entitled to retrieve the Token from the Swarm Platform if the holder sends the request to the Swarm Protocol. The common wording to describe an xToken is a "wrapped" token.

Such wrapped token may just mirror the functionalities of the Token or can have different functionality which is the case for the xToken as described in the following.

The xToken protocol checks that the address intending on transacting with the Token has permissions (i.e. is an onboarded user, has correct trading permissions as applicable to the given asset, etc) to interact with it. It acts as a permissioning layer for all transactions that take place on Swarm, allowing us to fulfill our regulatory obligations and keep user data secure and anonymous on the platform.

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

| Token      | Native Asset                               | xToken                                     |
| ---------- | ------------------------------------------ | ------------------------------------------ |
| **WBTC**   | 0x1BFD67037B42Cf73acF2047067bd4F2C47D9BfD6 | 0x54A3E68cA7C59Df9b95A5993FB257B455C628e54 |
| **WETH**   | 0x7ceB23fD6bC0adD59E62ac25578270cFf1b9f619 | 0x92aEB125534C08B3872f353C46453229f7af0AfF |
| **USDC**   | 0x2791Bca1f2de4661ED88A30C99A7a9449Aa84174 | 0x4A573b521b143f3e8032C3665b0Ab307b17F7bcf |
| **DAI**    | 0x8f3Cf7ad23Cd3CaDbD9735AFf958023239c6A063 | 0xd041806f89D24aa279a1d923f6127B12D03b00F5 |
| **SMT**    | 0xE631DABeF60c37a37d70d3B4f812871df663226f | 0xCF7d93aC1B6a527025Ae823B25D5D3d91389d282 |
| **WMATIC** | 0x0d500b1d8e8ef31e21c99d1db9a6444d3adf1270 | 0xc228a3b1a514d3b8431255f0184711e9601a765e |
| **BNB**    | 0x3ba4c387f786bfee076a58914f5bd38d668b42c3 | 0x6978EEb85AfDeEAf976Ee078030Ac2Be2c240676 |
| **Link**   | 0x53E0bca35eC356BD5ddDFebbD1Fc0fD03FaBad39 | 0xBDA3E7D7d3d7175FCc1A5727cfD7fB8085188B21 |
| **UNI**    | 0xb33EaAd8d922B1083446DC23f610c2567fB5180f | 0x6E50D7d2972451C9A9dAEf584b3c1376F26D6608 |
| **SAND**   | 0xBbba073C31bF03b8ACf7c28EF0738DeCF3695683 | 0xdcB44dA20f90D4287C4B4ab746486C8B9384C013 |
| **MANA**   | 0xA1c57f48F0Deb89f569dFbE6E2B7f46D33606fD4 | 0x24A80cb24Ac10dE641f92FB03f9BB54eC80A5780 |
| **GRT**    | 0x5fe2B58c013d7601147DcdD68C143A77499f5531 | 0x2e5F2C4024CB1c94D66f01f5E982b40b1ddD6850 |
| **AAVE**   | 0xD6DF932A45C0f255f85145f286eA0b292B21C90B | 0xe4262c24214A5F234ab419B912cBA3D9d187A262 |
| **Sushi**  | 0x0b3F868E0BE5597D5DB7fEB59E1CADBb0fdDa50a | 0xB3619046525e6Cb3B10d11c6BcC41B82f2407a91 |
| **Yearn**  | 0xDA537104D6A5edd53c6fBba9A898708E465260b6 | 0xda691818172fA2d335f8C2f3BE6556fA3B8646c4 |
| **SOL**    | 0xd93f7E271cB87c23AaA73edC008A79646d1F9912 | 0xde92ed6B3c461Ed57a09819f9479885673aad14F |
| **CEL**    | 0xd85d1e945766fea5eda9103f918bd915fbca63e6 | 0x15Aa2c19005e13c124A0f6DC177421993Ba19B42 |
| **1inch**  | 0x9c2C5fd7b07E95EE044DDeba0E97a665F142394f | 0xb1EC916A0e774e16d9A407b2fe1E6AABA3ae2bc7 |
| **SOLsn**  | 0xd98388bf3e062fc77a1a456a634f2b2dc5d1bb6e | 0xDBCd4A495FfE8D808eD0F3429fAD18d94D6588a6 |
| **NEARsn** | 0x80F8AdE10c21514Eed63fA52928Ea41dE33C5365 | 0xfa5d77a560e1d23caf90bd68a7bf1e79b28bf1d1 |
| **DOTsn**  | 0x02BA39888444c6277F7A6dFcb9a58b64FB3BEff3 | 0xDef0BA801597BCa70b5de03310Cc52cBaaE9C8d2 |
| **ETHsn**  | 0xf3cDA4E9f10D81151ffBFfd2C1527E42093B4542 | 0xf300557D3490B4BDcc080b71f86811C141c3242c |
| **AVAXsn** | 0xCF9AC0929e2195a4d1f0327D3e54EFa9D3d83523 | 0x6690cf54ab0f5c8e84952d1ad1c8f8d9aee9a511 |

## Further Reading

{% content-ref url="xtokens.md" %}
[xtokens.md](xtokens.md)
{% endcontent-ref %}

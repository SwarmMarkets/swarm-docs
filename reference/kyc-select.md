---
description: Built-in optional regulatory compliance into open trading infrastructure
---

# KYC Select

Within the Swarm Market's dOTC v2 trading infrastructure, offer makers can now require counterparties to be qualified and limit offers to only be taken by qualified counterparties.\
\
Offer makers can now choose from a selection of KYC/AML service providers.

This feature provides an additional compliance layer that sits on top of open and permissionless infrastructure, to provide fully regulatory institutional trading.

Qualifiers and KYC providers can very simply implement their own Authorization smart contract interface (requiring just one function) in order to provide their own qualification graph for offer makers to select from. See the technical implementation below.

### Technical implementation:

The dOTC platform simply requires the presence of a single function `isAccountAuthorized`to which a wallet address is passed, returning a true or false response, indicating whether the wallet address has been qualified.\
\
The Authorization contract can further interact with any other on-chain or off-chain logic to check the status of the wallet address.

```
// //SPDX-License-Identifier: GPL-3.0-only
pragma solidity 0.8.25;

/**
 * @title Interface for DOTC Authorizations Contracts (as part of the "SwarmX.eth Protocol")
 * @notice This interface is implemented by the Dotc contract to interact with the DotcManager.
 * ////////////////DISCLAIMER////////////////DISCLAIMER////////////////DISCLAIMER////////////////
 * Please read the Disclaimer featured on the SwarmX.eth website ("Terms") carefully before accessing,
 * interacting with, or using the SwarmX.eth Protocol software, consisting of the SwarmX.eth Protocol
 * technology stack (in particular its smart contracts) as well as any other SwarmX.eth technology such
 * as e.g., the launch kit for frontend operators (together the "SwarmX.eth Protocol Software").
 * By using any part of the SwarmX.eth Protocol you agree (1) to the Terms and acknowledge that you are
 * aware of the existing risk and knowingly accept it, (2) that you have read, understood and accept the
 * legal information and terms of service and privacy note presented in the Terms, and (3) that you are
 * neither a US person nor a person subject to international sanctions (in particular as imposed by the
 * European Union, Switzerland, the United Nations, as well as the USA). If you do not meet these
 * requirements, please refrain from using the SwarmX.eth Protocol.
 * ////////////////DISCLAIMER////////////////DISCLAIMER////////////////DISCLAIMER////////////////
 * @dev Defines the interface for the Dotc's Authorization contracts.
 * @author Swarm
 */
interface IDotcCompatibleAuthorization {
    /**
     * @notice Returns true if the provided `account` is authorized in the qualifier's ecosystem.
     * @param _account The address to be checked for authorization.
     * @return bool True if the `account` is authorized, false otherwise.
     */
    function isAccountAuthorized(address _account) external view returns (bool);
}
```

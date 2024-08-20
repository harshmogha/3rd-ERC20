# MyToken Smart Contract

## Overview

**MyToken** is a basic ERC20 token implemented in Solidity. This contract allows the contract owner to mint new tokens and any holder to burn their tokens. It also includes standard ERC20 transfer functionality.

## Features

- **ERC20 Standard**: Implements the basic ERC20 token standard.
- **Ownership**: The contract uses OpenZeppelin's `Ownable` module to restrict certain functions (like minting) to the contract owner.
- **Minting**: The contract owner can mint new tokens to a specified address.
- **Burning**: Any token holder can burn (destroy) their tokens, reducing the total supply.

## Contract Details

- **Token Name**: MyToken
- **Token Symbol**: MTK
- **Compiler Version**: 0.8.24

## Functions

### `constructor()`
- Initializes the token with the name "MyToken" and symbol "MTK".
- Sets the deployer as the contract owner.

### `mint(address to, uint256 amount) public onlyOwner`
- Allows the contract owner to mint new tokens.
- Parameters:
  - `to`: The address to receive the minted tokens.
  - `amount`: The number of tokens to mint.

### `burn(uint256 amount) public`
- Allows any token holder to burn (destroy) their tokens.
- Parameters:
  - `amount`: The number of tokens to burn.

### `transfer(address to, uint256 amount) public virtual override returns (bool)`
- Allows token holders to transfer tokens to another address.
- Parameters:
  - `to`: The address to receive the tokens.
  - `amount`: The number of tokens to transfer.

## Dependencies

This contract relies on the following OpenZeppelin libraries:

- `@openzeppelin/contracts/token/ERC20/ERC20.sol`: For implementing the ERC20 standard.
- `@openzeppelin/contracts/access/Ownable.sol`: For managing ownership.

## Deployment

1. Install the OpenZeppelin Contracts library:

   ```bash
   npm install @openzeppelin/contracts
   ```

2. Compile and deploy the contract using your preferred Ethereum development environment (e.g., Remix, Hardhat, Truffle).

## License

This project is licensed under the MIT License. See the SPDX-License-Identifier header in the contract file for details.

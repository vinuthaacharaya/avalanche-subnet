# Readme for Solidity Contracts

This repository contains two Solidity smart contracts: `Vault.sol` and `ERC20.sol`. Below is a brief overview of each contract along with usage instructions.

## Vault.sol

### Overview
`Vault.sol` is a contract that acts as a vault for storing ERC20 tokens. Users can deposit and withdraw tokens into/from the vault, and their balances are tracked through shares.

### Usage
1. **Deploying the Contract**: Deploy the contract by passing the address of the ERC20 token that you want to use with the vault.

2. **Deposit Tokens**: Users can deposit tokens into the vault by calling the `deposit` function and specifying the amount of tokens to deposit. This function calculates the number of shares to mint based on the deposited amount and the total supply of shares.

3. **Withdraw Tokens**: Users can withdraw tokens from the vault by calling the `withdraw` function and specifying the number of shares to redeem. This function calculates the amount of tokens to withdraw based on the number of shares being redeemed and the total supply of shares.

### Functions
- `deposit(uint _amount) external`: Deposits tokens into the vault and mints shares to the depositor.
- `withdraw(uint _shares) external`: Redeems shares and withdraws tokens from the vault.

## ERC20.sol

### Overview
`ERC20.sol` is a basic implementation of the ERC20 token standard. It allows for the creation of a simple ERC20 token with functionalities like transferring tokens, approving spender addresses, and allowance management.

### Usage
1. **Deploying the Contract**: Deploy the contract to create your custom ERC20 token.

2. **Token Operations**: Use the provided functions to perform token operations such as transferring tokens between addresses, approving spender addresses to transfer tokens on behalf of the owner, minting new tokens, and burning existing tokens.

### Functions
- `transfer(address recipient, uint amount) external returns (bool)`: Transfers tokens from the sender's account to the recipient's account.
- `approve(address spender, uint amount) external returns (bool)`: Approves the spender to transfer the specified amount of tokens on behalf of the owner.
- `transferFrom(address sender, address recipient, uint amount) external returns (bool)`: Transfers tokens from one address to another on behalf of the sender, given approval from the sender.
- `mint(uint amount) external`: Mints new tokens and adds them to the total supply.
- `burn(uint amount) external`: Burns existing tokens, reducing the total supply.

## Author

Vinutha acharaya 

## License
Both contracts are licensed under the MIT License.

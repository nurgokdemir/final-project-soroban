# Soroban Token Contract

This repository contains a standard token smart contract built specifically for the Soroban platform, which is Stellar's smart contract layer.

## About the Project

The Soroban Token Contract provides a full set of basic token operations. It enables functionalities like minting, transferring, burning tokens, and managing third-party token allowances through a secure and efficient design.

## Key Features

- **Token Lifecycle Management**: Mint new tokens, burn existing ones, and transfer between accounts
- **Delegated Spending**: Implement an approval system allowing others to spend tokens on your behalf
- **Administrative Controls**: Define an admin account and enforce admin-only operations
- **Token Metadata**: Store information like token name, symbol, and decimal precision

## Architecture

The contract is modular and consists of:

- **admin**: Functions for admin role management and permission enforcement
- **allowance**: Logic for managing spending permissions
- **balance**: Core balance tracking and updates
- **contract**: Main contract logic and standard token interface
- **metadata**: Token attributes such as name, symbol, and decimals
- **storage_types**: Definitions for structured data storage

## Technical Overview

This smart contract is developed in Rust and uses the `#![no_std]` directive to operate without the Rust standard library. This allows the contract to be lightweight and optimized for blockchain environments.

### Major Functions

#### Token Operations
- `mint`: Admin-exclusive function to issue new tokens
- `burn`: Destroy a specified number of tokens
- `transfer`: Move tokens from one account to another
- `balance`: Retrieve the current token balance of an address

#### Allowance Operations
- `approve`: Grant spending rights to another address
- `allowance`: Check the approved spending limit
- `transfer_from`: Move tokens on behalf of the owner using granted rights
- `burn_from`: Burn tokens using delegated allowance

#### Admin-Specific Functions
- `initialize`: Set up the contract initially
- `set_admin`: Assign a new administrator

## Getting Involved

If you have questions, suggestions, or contributions, feel free to open an issue or submit a pull request to improve the project.

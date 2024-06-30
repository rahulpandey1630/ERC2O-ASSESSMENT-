# MetaToken

MetaToken is an ERC20 token built on the Ethereum blockchain using Solidity and OpenZeppelin libraries. This token, named "metatoke" with the symbol "mtc", allows the contract owner to mint new tokens and any token holder to burn their tokens.

## Features

- **Minting**: Only the contract owner can mint new tokens.
- **Burning**: Any token holder can burn their tokens.
- **Transfer**: Tokens can be transferred between accounts.

## Contract Details

- **Name**: metatoke
- **Symbol**: mtc
- **Decimals**: 18 (default for ERC20 tokens)
- **Total Supply**: Defined during contract deployment

## Functions

### Constructor

```solidity
constructor(uint initialSupply)
Initializes the token with a specified initial supply and assigns it to the contract deployer.
Mint
solidity
Copy code
function mint(address to, uint amount) public onlyOwner
Mints a specified amount of tokens to a given address.
Only the owner can call this function.
Burn
solidity
Copy code
function burn(uint amount) public
Burns a specified amount of tokens from the caller's account.
Transfer
solidity
Copy code
function transferToken(address from, address to, uint amount) public
Transfers a specified amount of tokens from one address to another.
Modifiers
onlyOwner
Ensures that certain functions can only be called by the contract owner.
Usage
Deploying the Contract
Deploy the contract with an initial supply.
The deployer will be set as the owner of the contract.
Minting Tokens
Call the mint function with the recipient address and amount.
Only the owner can mint new tokens.
Burning Tokens
Any token holder can call the burn function to reduce their balance.
Transferring Tokens
Use the transferToken function to transfer tokens between accounts.
License
This project is licensed under the MIT License.

markdown
Copy code

## Getting Started

To interact with this contract, you will need:

- A Solidity development environment (like Remix)
- MetaMask to manage your Ethereum wallet and connect to the blockchain

## Dependencies

- OpenZeppelin Contracts

```bash
npm install @openzeppelin/contracts
Security
Ensure you understand the implications of deploying and interacting with smart contracts on the blockchain. Review the contract code and its dependencies thoroughly.


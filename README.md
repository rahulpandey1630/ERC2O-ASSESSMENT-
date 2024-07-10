## MetaToken

MetaToken is an ERC20 token built on the Ethereum blockchain using Solidity and OpenZeppelin libraries. This token, named "metatoke" with the symbol "mtc", allows the contract owner to mint new tokens and any token holder to burn their tokens.

## Features

- Minting: Only the contract owner can mint new tokens.
- Burning: Any token holder can burn their tokens.
- Transfer: Tokens can be transferred between accounts.

## Contract Details

- Name: metatoke
- Symbol: mtc
- Decimals: 18 (default for ERC20 tokens)
- Total Supply: Defined during contract deployment

# Functions
mint(address to, uint amount): Mints new tokens to the specified address. Only the contract owner can call this function.
burn(uint amount): Burns the specified amount of tokens from the caller's account.
transferToken(address from, address to, uint amount): Transfers tokens from one address to another.
# Modifiers
onlyOwner: Restricts certain functions to be callable only by the contract owner.
# How to Use
Deploy the Contract:
Specify the initial supply of tokens.
Mint Tokens:
Call the mint function with the recipient's address and the amount of tokens to mint.
Burn Tokens:
Call the burn function with the amount of tokens to burn.
Transfer Tokens:
Call the transferToken function with the sender's address, recipient's address, and the amount of tokens to transfer.
## Example
To deploy the contract with an initial supply of 1000 tokens, the owner can mint, burn, and transfer tokens as follows:

solidity
```
Copy code
// Mint 100 tokens to address 0x123...
mint(0x123..., 100);

// Burn 50 tokens from the caller's account
burn(50);

// Transfer 20 tokens from address 0x123... to address 0x456...
transferToken(0x123..., 0x456..., 20);

```
This contract leverages the OpenZeppelin ERC20 implementation for standard token functionalities.




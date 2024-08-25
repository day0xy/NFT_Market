# NFTMarket Contract

## Overview

The NFTMarket contract allows users to list NFTs for sale at any specified ERC20 price and enables the purchase of NFTs using ERC20 tokens.

## Features

- List NFTs for sale with a customizable ERC20 price.
- Purchase specified NFTs using ERC20 tokens.

## Testing Requirements

### Listing NFTs

- **Success Case**: Test successful listing of an NFT and assert the listing event.
- **Failure Cases**: Test various failure scenarios for listing, asserting the relevant error messages and events.

### Purchasing NFTs

- **Success Case**: Test successful purchase of an NFT and assert the purchase event.
- **Self-purchase**: Test the scenario where a user attempts to purchase their own NFT.
- **Duplicate Purchase**: Test the case where an NFT is purchased multiple times and assert the appropriate error messages.
- **Incorrect Payment Amounts**: Test scenarios where the payment amount is either too high or too low, asserting the relevant error messages and events.

### Fuzz Testing

- Randomly list NFTs for sale with prices ranging from 0.01 to 10,000 tokens.
- Randomly use any address to attempt to purchase NFTs.

### (TODO) Immutability Testing

- Ensure that the NFTMarket contract cannot hold any ERC20 tokens regardless of the buy/sell activities.

## Conclusion

This contract provides a robust framework for listing and purchasing NFTs while incorporating comprehensive testing to ensure reliability and correctness.
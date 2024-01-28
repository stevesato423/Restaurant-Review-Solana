# Solana Restaurant Review Smart Contract

## Overview

This Solana smart contract is designed for managing restaurant reviews. It allows users to add and update reviews for different restaurants. Each review includes a title, a numerical rating, a text description, and a location string.

## Features

1. **Add Review**: Users can add new reviews. Each review is associated with a unique Program Derived Address (PDA) based on the user's key and the title of the review.
2. **Update Review**: Users can update existing reviews. Updates are allowed for rating, description, and location.
3. **Data Validation**: The smart contract ensures that the rating is within the range of 1 to 10. It also checks the proper initialization of accounts and the validity of PDAs.

## Requirements

- Solana CLI tools
- Rust programming language and Cargo package manager
- Solana Playground (optional for easy deployment and testing)

## How to Deploy on Devnet

1. **Connect to Solana Playground**: Go to [Solana Playground](https://beta.solpg.io/).
2. **Connect Wallet**: Press "Connect" at the bottom left corner(red circle) of the page.
3. **Fund Your Account**:
   - Run `$solana airdrop 1` in the console to receive SOL tokens. If this doesn't work, use the [Solana Faucet](https://faucet.solana.com/) to manually send some tokens to your account.
4. **Deploy the Contract**:
   - Go to "build & deploy" tab. Click build and then deploy to compile and deploy the smart contract on the Solana devnet.

## Interacting with the Smart Contract

Once deployed, you can interact with the smart contract through the Solana Playground interface or using Solana's command-line tools. Ensure that you have the necessary keypairs for the initializer account and the system program.

### Adding a Review

- Use the `AddReview` instruction with parameters: title, rating, description, and location.

### Updating a Review

- Use the `UpdateReview` instruction with parameters: title, rating, description, and location.

## Important Notes

- Make sure that the title for each review is unique to successfully create a unique PDA.
- Ratings are restricted between 1 and 10.
- The contract checks for the initialization of accounts and valid PDAs to maintain data integrity.

## Conclusion

This smart contract exemplifies a basic yet functional use case of blockchain technology for content management. By leveraging Solana's capabilities, it offers a decentralized and secure way to handle restaurant reviews, providing transparency and immutability to user-generated data.

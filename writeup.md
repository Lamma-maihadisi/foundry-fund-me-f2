# FundMe Smart Contract — Project Writeup

## 🚀 Overview

This is a Solidity-based crowdfunding smart contract that allows users to contribute ETH, enforcing a minimum funding threshold based on real-time USD pricing via Chainlink Price Feeds. It is designed to help users understand on-chain value conversion, decentralized funding mechanics, and secure withdrawal logic.

## 🛠️ Tech Stack

- **Solidity** (Smart contract logic)
- **Foundry** (Development framework & testing)
- **Chainlink Price Feeds** (Oracle integration for ETH/USD)
- **Remix & Etherscan** (Contract deployment and verification)

## 🎯 Key Features

- Only accepts ETH contributions above a minimum USD threshold
- Automatically converts ETH value to USD using Chainlink oracles
- Tracks funders and their contributions
- Only the contract owner can withdraw funds

## 🧪 Testing Strategy

- Wrote unit tests using Foundry's built-in Forge framework
- Simulated real-world funding flows, including edge cases like:
  - Contributions below minimum threshold
  - Multiple funders
  - Withdrawals by non-owners
- Verified contract behavior using `--fork-url` to simulate live Chainlink data from Sepolia testnet

## 💡 What I Learned

- Deepened my knowledge of Foundry, particularly:
  - Writing fuzz tests and invariant checks
  - Using `vm.startPrank()` and cheatcodes for better test control
- Gained hands-on experience with Chainlink oracle integration
- Learned secure access control and best practices around fund withdrawal logic

## 📌 Challenges Faced

- Handling real-time ETH/USD conversions accurately in smart contracts
- Mocking external contract calls in Foundry (e.g., mocking oracles in local tests)
- Understanding ownership patterns and dealing with gas optimization in withdrawal functions

## 🧠 Why This Matters

Tokenized value transfer is core to DeFi, and understanding how to enforce pricing logic on-chain is a foundational skill. This project represents a building block for more complex systems like decentralized launchpads, DAOs, and tokenized real-world asset platforms.

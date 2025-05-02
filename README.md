# FundMe Smart Contract 💰

This is a decentralized crowdfunding smart contract built with **Solidity** and **Foundry**. It allows users to contribute ETH to the contract, and the contract owner can withdraw the funds. The contract utilizes **Chainlink Price Feeds** for real-time ETH to USD conversion, ensuring that the contribution meets a minimum threshold in USD.

---

## 📝 Features

- **Minimum Contribution**: Users must contribute at least **5 USD** worth of ETH, based on Chainlink price feeds.
- **Owner-Only Withdrawal**: Only the contract owner can withdraw the funds.
- **Gas-Optimized Withdrawals**: The `cheaperWithdraw()` function optimizes gas usage during withdrawals.
- **Fallback & Receive Functions**: Supports ETH transfers directly to the contract through fallback and receive functions.
- **Security**: Includes ownership checks and custom error handling to ensure secure interactions.

---

## 🛠️ Technologies Used

- **Solidity** `^0.8.18`
- **Foundry** – Fast and flexible framework for Solidity development
- **Chainlink Price Feeds** – For real-time ETH to USD conversion
- **OpenZeppelin Contracts** – Standard library for secure smart contract development

---

## 🚀 Installation & Deployment

### Prerequisites

- **Foundry**: A Solidity development toolchain. [Install Foundry](https://book.getfoundry.sh/)

### 1. Install Dependencies

Run the following command to install required dependencies:

```bash
forge install

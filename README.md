# VevoNFT

# NFT-Share: Blockchain-Based NFT Project

**NFT-Share** is a Solidity-based repository featuring **ERC-721** smart contracts designed for the creation, deployment, and sharing of NFTs. This project is optimized for the **Sepolia Ethereum Test Network** using **Remix IDE** and **MetaMask**. It serves as a comprehensive guide for users to understand the lifecycle of Non-Fungible Tokens, from minting unique digital assets to managing ownership transfers on a live test network.

## Features

* **ERC-721 NFT Implementation:** Standardized Solidity contracts for unique digital assets.
* **Minting & Sharing Logic:** Built-in functions to create new tokens and transfer them between users.
* **Remix-Ready Functions:** Interactive buttons within the IDE to trigger actions like `mint`, `approve`, and `transfer`.
* **Sepolia Testnet Integration:** Fully compatible with Ethereum's Sepolia network for risk-free testing.
* **MetaMask Support:** Real-time transaction signing and asset management via the MetaMask browser extension.

---

## Guide

### 1. Creation of MetaMask Wallet
* Navigate to the **Chrome Web Store** and download the **MetaMask** extension.
* Create your wallet and securely store your recovery phrase.
* Navigate to **Settings > Advanced** and enable **Show Test Networks**.
* Select **Sepolia** from the network dropdown menu.

### 2. Sepolia Ethereum Faucet
* Navigate to a Sepolia Faucet (such as the **Google Cloud Faucet** or **Alchemy**) to obtain test ETH.
* Enter your wallet address and complete the required steps to receive your funds.

### 3. Open Remix IDE
* Go to [https://remix.ethereum.org](https://remix.ethereum.org).
* Create a new workspace.
* **Create File 1:** Name it `NftShare.sol` and paste your NFT contract code (ensure the contract name matches your chosen file name).
* **Create File 2:** Name it `IERC721.sol` (or the relevant interface name) to support the NFT standard.

### 4. Compile the Contract
* Select the **Solidity Compiler** tab.
* Ensure the compiler version matches your code.
* Click **Compile NftShare.sol**.

### 5. Deploy the Contract
* Open the **Deploy & Run Transactions** tab.
* Set the **Environment** to **Injected Provider – MetaMask**.
* Confirm the connection request in the MetaMask popup.
* Ensure your network is set to **Sepolia Test Network**.
* Click **Deploy** and confirm the transaction fee in MetaMask.
* Once deployed, interact with your NFT functions (mint, transfer) directly in the Remix sidebar.

### 6. Confirming the Transaction
To verify that your NFT has been added to the blockchain:
* Go to [https://sepolia.etherscan.io](https://sepolia.etherscan.io).
* Copy and paste your **Deployed Contract Address** into the search bar.
* Review the "Tokens" and "Transactions" tabs to see your minted NFTs.

---

## Tech Stack

* **Solidity:** Smart contract language.
* **Remix IDE:** Web-based development environment.
* **Ethereum Sepolia:** Test blockchain network.
* **MetaMask Wallet:** Digital wallet for transaction signing.
* **ERC-721 Standard:** The protocol for Non-Fungible Tokens.
* **Sepolia Etherscan:** Blockchain explorer for verifying transactions.

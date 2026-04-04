# VevoNFT

**VevoNFT** is a Solidity-based repository featuring **ERC-721** smart contracts designed for the creation, deployment, and sharing of NFTs. This project integrates **Pinata** for decentralized storage, allowing users to link their NFTs to unique digital assets via **CID Hashes**. It is optimized for the **Sepolia Ethereum Test Network** using **Remix IDE** and **MetaMask**.

## Features

* **ERC-721 NFT Implementation:** Standardized Solidity contracts for unique digital assets.
* **IPFS Content Addressing:** Integration of Pinata CID hashes to link NFTs to media files (images, videos, etc.).
* **Minting & Sharing Logic:** Functions to create new tokens with specific metadata and transfer them between users.
* **Remix-Ready Functions:** Interactive buttons within the IDE to trigger actions like `mint` (with CID input), `approve`, and `transfer`.
* **Sepolia Testnet Integration:** Fully compatible with Ethereum's Sepolia network for risk-free testing.

---

## Guide

### 1. Creation of MetaMask Wallet
* Navigate to the **Chrome Web Store** and download the **MetaMask** extension.
* Create your wallet and securely store your recovery phrase.
* Navigate to **Settings > Advanced** and enable **Show Test Networks**.
* Select **Sepolia** from the network dropdown menu.

### 2. Upload Assets to Pinata
* Go to [Pinata.cloud](https://www.pinata.cloud/) and create an account.
* Upload your file (Image/Video/JSON) using the **Upload** button.
* Once uploaded, copy the **CID (Content Identifier)** hash. You will use this hash during the minting process to link your NFT to the file.

### 3. Sepolia Ethereum Faucet
* Navigate to a Sepolia Faucet (such as the **Google Cloud Faucet** or **Alchemy**) to obtain test ETH.
* Enter your wallet address and complete the required steps to receive your funds.

### 4. Open Remix IDE
* Go to [https://remix.ethereum.org](https://remix.ethereum.org).
* Create a new workspace.
* **Create File 1:** Name it `NftShare.sol` and paste your NFT contract code (ensure your `mint` function accepts a `string` for the CID).
* **Create File 2:** Name it `IERC721.sol` to support the NFT standard.

### 5. Compile and Deploy
* Select the **Solidity Compiler** tab and click **Compile NftShare.sol**.
* Open the **Deploy & Run Transactions** tab.
* Set the **Environment** to **Injected Provider – MetaMask**.
* Click **Deploy** and confirm the transaction fee in MetaMask.

### 6. Minting with CID Hash
* In the **Deployed Contracts** section, locate your `mint` or `createToken` function.
* Paste the **CID Hash** you copied from Pinata into the `tokenURI` or `metadata` field.
* Click **Transact** and confirm in MetaMask. Your NFT is now live and linked to your IPFS content!

### 7. Confirming the Transaction
* Go to [https://sepolia.etherscan.io](https://sepolia.etherscan.io).
* Paste your **Deployed Contract Address** to see your minted NFTs and verify the transaction history.

---

## Tech Stack

* **Solidity:** Smart contract language.
* **Pinata (IPFS):** Decentralized storage for NFT media and metadata.
* **Remix IDE:** Web-based development environment.
* **Ethereum Sepolia:** Test blockchain network.
* **MetaMask Wallet:** Digital wallet for transaction signing.
* **ERC-721 Standard:** Protocol for Non-Fungible Tokens.

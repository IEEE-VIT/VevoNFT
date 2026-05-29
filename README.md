# VevoNFT
**VevoNFT** is a Solidity-based repository featuring **ERC-721** smart contracts designed for the creation, deployment, and sharing of NFTs. This project integrates **Pinata** for decentralized storage, allowing users to link their NFTs to unique digital assets via **CID Hashes**. It is optimized for the **Sepolia Ethereum Test Network** using **Remix IDE** and **MetaMask**.

## Project Structure

```
VevoNFT/
├── contracts/
│   └── MediaToken.sol       # ERC-721 smart contract
├── metadata/
│   ├── image.json           # Standard NFT metadata for image assets
│   └── video.json           # Standard NFT metadata for video assets
└── README.md
```

---

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
* Upload your media file (Image/Video) using the **Upload** button and copy its **CID**.
* Open the appropriate metadata file from the `metadata/` folder (`image.json` or `video.json`).
* Replace the `image` or `animation_url` field value with your IPFS URI in the format `ipfs://<YOUR_CID>`.
* Fill in the `name`, `description`, and any `attributes` you'd like associated with your NFT.
* Upload the updated JSON file to Pinata and copy its **CID** — this will be your token URI.

### 3. Sepolia Ethereum Faucet
* Navigate to a Sepolia Faucet (such as the **Google Cloud Faucet** or **Alchemy**) to obtain test ETH.
* Enter your wallet address and complete the required steps to receive your funds.

### 4. Open Remix IDE
* Go to [https://remix.ethereum.org](https://remix.ethereum.org).
* Create a new workspace.
* **Create File 1:** Inside a `contracts/` folder, name it `MediaToken.sol` and paste the contents of `contracts/MediaToken.sol` from this repository.

### 5. Compile and Deploy
* Select the **Solidity Compiler** tab and click **Compile MediaToken.sol**.
* Open the **Deploy & Run Transactions** tab.
* Set the **Environment** to **Injected Provider – MetaMask**.
* Click **Deploy** and confirm the transaction fee in MetaMask.

### 6. Minting with CID Hash
* In the **Deployed Contracts** section, locate the `safeMint` function.
* Enter the recipient wallet address in the `to` field.
* Paste the **CID Hash** of your uploaded JSON metadata file (from `metadata/`) into the `uri` field, formatted as `ipfs://<YOUR_METADATA_CID>`.
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

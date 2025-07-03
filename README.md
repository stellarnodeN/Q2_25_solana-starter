````markdown name=README.md
# Solana Starter: SPL Token and NFT Minting with TypeScript

A comprehensive starter project for minting SPL tokens and Metaplex NFTs on Solana using TypeScript.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Usage](#usage)
  - [Minting SPL Tokens](#minting-spl-tokens)
  - [Transferring SPL Tokens](#transferring-spl-tokens)
  - [Minting NFTs](#minting-nfts)
  - [Vault Operations (Deposit & Withdraw)](#vault-operations-deposit--withdraw)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This repository provides a TypeScript codebase and practical scripts for:

- Creating and minting SPL tokens on the Solana blockchain
- Creating and minting NFTs using the Metaplex standard
- Managing tokens and NFTs with associated token accounts (ATAs)
- Vault operations for depositing and withdrawing tokens and NFTs

All scripts are written in TypeScript and use Solana, SPL Token, and Metaplex SDKs for secure and maintainable blockchain interactions.

---

## Features

- **SPL Token Minting**: Easily create and mint your own SPL tokens ([spl_init.ts](cluster1/spl_init.ts), [spl_mint.ts](cluster1/spl_mint.ts))
- **SPL Token Transfers**: Transfer SPL tokens between wallets ([spl_transfer.ts](cluster1/spl_transfer.ts))
- **NFT Minting (Metaplex Standard)**: Mint NFTs using Metaplex and manage their metadata ([spl_metadata.ts](cluster1/spl_metadata.ts))
- **Vault Operations**: Deposit and withdraw SPL tokens and NFTs using Anchor-based Solana programs ([vault_deposit_spl.ts](cluster1/vault_deposit_spl.ts), [vault_withdraw_spl.ts](cluster1/vault_withdraw_spl.ts))
- **TypeScript First**: All scripts use TypeScript for safer and more robust development

---

## Prerequisites

- [Node.js](https://nodejs.org/) (v16+ recommended)
- A funded Solana wallet (e.g. Phantom, Sollet) with devnet SOL
- Basic understanding of Solana, SPL tokens, and NFTs

---

## Getting Started

1. **Clone the Repository**
   ```bash
   git clone https://github.com/stellarnodeN/Q2_25_solana-starter.git
   cd Q2_25_solana-starter
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Wallet Setup**
   - Place your wallet JSON (exported from Solana CLI or Phantom) in the `cluster1/wallet/` directory.
   - Update wallet file imports in scripts if using a different file.

---

## Project Structure

```
cluster1/
  ├── spl_init.ts            # Create a new SPL token mint
  ├── spl_mint.ts            # Mint SPL tokens to an account
  ├── spl_transfer.ts        # Transfer SPL tokens
  ├── spl_metadata.ts        # Mint NFT metadata using Metaplex
  ├── vault_deposit_spl.ts   # Deposit SPL tokens into a vault
  ├── vault_withdraw_spl.ts  # Withdraw SPL tokens from a vault
  ├── programs/
  │     └── wba_vault.ts     # Anchor program definition for vault operations
  └── wallet/
        └── Turbin3-wallet.json # Example wallet file
```

---

## Usage

### Minting SPL Tokens

**1. Initialize a New SPL Token Mint**
```bash
ts-node cluster1/spl_init.ts
```
This will create a new mint address and display it in the console.

**2. Mint SPL Tokens to an Account**
- Update `mint` and wallet details in `spl_mint.ts` as needed.
```bash
ts-node cluster1/spl_mint.ts
```

### Transferring SPL Tokens

Update the recipient address and mint in `spl_transfer.ts` and run:
```bash
ts-node cluster1/spl_transfer.ts
```

### Minting NFTs

Use `spl_metadata.ts` to attach Metaplex metadata to an SPL token mint (turning it into an NFT).
- Update mint and metadata details in the script as needed.
```bash
ts-node cluster1/spl_metadata.ts
```

### Vault Operations (Deposit & Withdraw)

Deposit SPL tokens into a vault:
```bash
ts-node cluster1/vault_deposit_spl.ts
```

Withdraw SPL tokens from a vault:
```bash
ts-node cluster1/vault_withdraw_spl.ts
```

_See each script for inline comments on configuration and further steps._

---

## Contributing

Contributions are welcome! Please fork the repo, create a feature branch, and submit a pull request.

---
````



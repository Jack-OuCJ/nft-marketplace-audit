# Gas Bad NFT Marketplace 

<p align="center">
<img src="./img/gas-bad.png" width="400" alt="gas-bad">
<br/>


I am building a "gas bad" marketplace. An NFT marketplace, but I am going for a gas optimized version. 

To do this, I am writing 2 types of smart contracts:

1. Reference contracts in solidity 
2. Optimized contracts in solidity / assembly 

I will be deploying `GasBadNftMarketplace.sol` to the Ethereum mainnet, but are using `NftMarketplace.sol` as a reference point. 

# About

I am building a "gas bad" marketplace. An NFT marketplace, but I am going for a gas optimized version. 

To do this, I am writing 2 types of smart contracts:

1. Reference contracts in solidity 
2. Optimized contracts in solidity / assembly 

I will be deploying `GasBadNftMarketplace.sol` to the Ethereum mainnet, but are using `NftMarketplace.sol` as a reference point. 

# Getting Started

## Requirements

- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
  - You'll know you did it right if you can run `git --version` and you see a response like `git version x.x.x`
- [foundry](https://getfoundry.sh/)
  - You'll know you did it right if you can run `forge --version` and you see a response like `forge 0.2.0 (816e00b 2023-03-16T00:05:26.396218Z)`
- [certoraRun cli](https://docs.certora.com/en/latest/docs/user-guide/getting-started/install.html)
  - You'll know you did it right if you can run `certoraRun --version` and you see a response like `certora-cli 6.1.4`
  - You'll also need a certora environment variable named `CERTORAKEY`
  - You may need python and `pip` installed to install the certora cli

# Usage
## Certora

### Certora Setup

After installing the [Certora CLI](https://docs.certora.com/en/latest/docs/user-guide/getting-started/install.html), you'll need to set up your environment variables. The instructions here only work for linux/macOs/windows WSL.

```bash
export CERTORAKEY=<personal_access_key>
```
```

or, you can ruh:

```
source .env.example
```

You can check if the environment variable is set by running:

```bash
echo $CERTORAKEY
```

## Compatibilities

- Solc Version: 0.8.20
- Chain(s) to deploy contract to: 
  - Ethereum
- Tokens:
  - None

# Roles

- Buyer: Someone who buys an NFT from the marketplace
- Seller: Someone who sells and NFT on the marketplace

# Known Issues

- The seller can front-run a bought NFT and cancel the listing
- The seller can front-run a bought NFT and update the listing
- I should emit an event for withdrawing proceeds
- There are MEV/Front Running issues all over the place
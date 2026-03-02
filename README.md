# SunSwap 1.5 Contracts

This repository contains the core smart contracts for the **SunSwap 1.5 Protocol**, an AMM-based decentralized exchange deployed on TRON.

The goal of this README is to provide a clear, English-only overview of:

- The contracts shipped in this repository
- How to compile and deploy them
- The networks and addresses currently in use
- How to contribute or get in touch with the team

All of the original information (deployment addresses, commands, and setup instructions) is preserved and expanded below.

---

## Overview

SunSwap 1.5 provides the on-chain components required for:

- Creating and managing trading pairs
- Adding and removing liquidity
- Swapping tokens via an automated market maker (AMM)

This repository focuses on the **factory** and related core contracts. Frontend and off-chain services are maintained in separate repositories.

---

## Deployments

The following table lists known production or public test deployments of the contracts.

| Contract | Network | Address                            |
| :------- | :------ | :--------------------------------- |
| Factory  | TRON    | TB2LM4iegvhPJGWn9qizeefkPMm7bqqaMs |

> **Note**  
> Always verify contract addresses from official SunSwap / Sun.io announcements or documentation before interacting with them.

---

## Requirements

To work with this repository you will need:

- **Node.js 8.0+** – see the [official Node.js documentation](https://github.com/nodejs/node) for installation
- **npm** (bundled with most Node.js distributions)
- A compatible operating system:
  - Linux
  - macOS

---

## Getting Started

Clone the repository and install dependencies:

```bash
git clone https://github.com/sunswapteam/sunswap1.5-contracts.git
cd sunswap1.5-contracts
npm install
```

---

## Compile and Build

To compile the smart contracts:

```bash
npm run compile
```

This will:

- Run the Solidity compiler with the configured settings
- Output the compiled artifacts (bytecode and ABI) into the build directory configured in the project

If the command fails, ensure that:

- Your Node.js version is 8.0 or higher
- Dependencies have been installed successfully via `npm install`

---

## Deployment

### Deploying to Nile TestNet

You can deploy the SunSwap 1.5 **factory** and **value aggregator** contracts to the TRON Nile TestNet using the provided scripts.

First, export your private key for the Nile TestNet account (use a **test** account, never a production key):

```bash
export PRIVATE_KEY_NILE='Your private key'
```

Then run:

```bash
npm run migrate
```

This will:

- Use the `PRIVATE_KEY_NILE` environment variable to sign transactions
- Deploy the factory and related contracts to Nile
- Output the deployed addresses to the console or logs

> **Security Warning**  
> Do **not** commit or share your private key. Use environment variables or secure secrets management. For production deployment, use hardened operational security processes.

---

## Development Notes

- Review the contract source files to understand the exact AMM logic, fees, and token requirements.
- When modifying contracts, always:
  - Re-run `npm run compile`
  - Add or update tests where applicable
  - Perform manual verification on a test network before mainnet deployment

---

## Community & Support

If you have questions about this project, find bugs, or would like to contribute, you can reach the team and community via:

- [Telegram](https://t.me/SunIO_Defi)
- [Twitter](https://twitter.com/defi_sunio)

Please follow official announcements from these channels for the latest information on deployments, upgrades, and security notices.

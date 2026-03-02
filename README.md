# SunSwap1.5-contracts

This repository contains the core smart contracts for the SunSwap 1.5 Protocol.

## Description

SunSwap 1.5 Protocol id upgrade from sunswap 1.0 Protocol，we have discontinued support for BTT token（TRC10）and optimized parts of the codebase.

SunSwap 1.5 Protocol is TRX-TRC20 liquidity pool protocol，we  rely on  `X * Y = K` model for managing liquidity and performing exchange operations.

## Deployments

|contract|address|
|:---|:---|
|Factory |TB2LM4iegvhPJGWn9qizeefkPMm7bqqaMs|

## Compile and Deployment

To get started, first create and initialize a [NodeJS 8.0+ environment](https://github.com/nodejs/node). Next, clone the repo and install the developer dependencies:

### Setup

```bash
git clone https://github.com/sunswapteam/sunswap1.5-contracts.git
cd sunswap1.5-contracts
npm install
```

### OS requirement
 * Linux
 * Mac OS X

### Compile

```
npm run compile
```

### Deploy on Nile TestNet

Deploy the Sunswap 1.5 factory and value aggregator contract to the Nile TestNet.

```
export PRIVATE_KEY_NILE='Your private key'
npm run migrate
```

## Community

If you have any questions about this project, or wish to engage with us:

- [Telegram](https://t.me/SunIO_Defi)
- [Twitter](https://twitter.com/defi_sunio)

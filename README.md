# freeCodeCamp: Full Blockchain Solidity Course JavaScript - Lesson 12: Hardhat ERC20

# Contents

-   [Getting Started](#getting-started)
-   [Requirements](#requirements)
-   [Quickstart](#quickstart)
-   [Getting Started](#getting-started)
    -   [Requirements](#requirements)
    -   [Quickstart](#quickstart)
-   [Usage](#usage)
-   [Deployment to a testnet or mainnet](#deployment-to-a-testnet-or-mainnet)
    -   [Verify on etherscan](#verify-on-etherscan)

# Getting Started

## Requirements

-   [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
    -   You'll know you did it right if you can run `git --version` and you see a response like `git version x.x.x`
-   [Nodejs](https://nodejs.org/en/)
    -   You'll know you've installed nodejs right if you can run:
        -   `node --version` and get an ouput like `vx.x.x`
-   [Yarn](https://classic.yarnpkg.com/lang/en/docs/install/) instead of `npm`
    -   You'll know you've installed yarn right if you can run:
        -   `yarn --version` And get an output like `x.x.x`
        -   You might need to install it with npm

## Quickstart

```
git clone git@github.com:dariuszsetlak89/fcc-fbsc-js-lesson12-hardhat-erc20.git
cd fcc-fbsc-js-lesson12-hardhat-erc20
yarn
```

# Usage

Deploy:

```
yarn hardhat deploy
```

# Deployment to a testnet or mainnet

1. Setup environment variabltes

You'll want to set your `GOERLI_RPC_URL` and `PRIVATE_KEY` as environment variables. You can add them to a `.env` file.

-   `PRIVATE_KEY`: The private key of your account (like from [metamask](https://metamask.io/)). **NOTE:** FOR DEVELOPMENT, PLEASE USE A KEY THAT DOESN'T HAVE ANY REAL FUNDS ASSOCIATED WITH IT.
    -   You can [learn how to export it here](https://metamask.zendesk.com/hc/en-us/articles/360015289632-How-to-Export-an-Account-Private-Key).
-   `GOERLI_RPC_URL`: This is url of the kovan testnet node you're working with. You can get setup with one for free from [Alchemy](https://alchemy.com/?a=673c802981)

2. Get testnet ETH

Head over to [faucets.chain.link](https://faucets.chain.link/) and get some tesnet ETH. You should see the ETH show up in your metamask.

3. Deploy

```
yarn hardhat deploy --network goerli
```

## Verify on etherscan

If you deploy to a testnet or mainnet, you can verify it if you get an [API Key](https://etherscan.io/myapikey) from Etherscan and set it as an environemnt variable named `ETHERSCAN_API_KEY`. You can pop it into your `.env`.

In it's current state, if you have your api key set, it will auto verify kovan contracts!

However, you can manual verify with:

```
yarn hardhat verify --constructor-args arguments DEPLOYED_CONTRACT_ADDRESS
```

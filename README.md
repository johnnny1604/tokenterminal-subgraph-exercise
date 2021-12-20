<p align="center">
  <a href="https://tokenterminal.com">
    <img src="https://github.com/token-terminal/tt-analytics/raw/main/frontend/public/logo.png" height="128">
    <h2 align="center">Token Terminal</h2>
  </a>
</p>

# Welcome to the Token Terminal subgraph challenge!

If you are reading this, you are probably already familiar with [Token Terminal](https://www.tokenterminal.com/). We provide fundamental data on blockchains and [Web3](https://ethereum.org/en/developers/docs/web2-vs-web3/) applications.

One of the various tools that helps us achieve this is The Graph protocol. [The Graph](https://thegraph.com/) is a decentralized indexing protocol for querying data from blockchains like Ethereum. We use The Graph protocol extensively on Token Terminal to ensure we have control over the entire data pipeline (from querying [smart contract](https://ethereum.org/en/developers/docs/smart-contracts/) data to calculating high-level aggregate [business metrics](https://docs.tokenterminal.com/our-metrics)).

This repository contains a number of subgraph development tasks we use to assess candidates interested in joining our growing [team](https://docs.tokenterminal.com/careers). These tasks range from simply deploying existing subgraphs, modifying them, of developing subgraphs from scratch based on specifications we'll provide.

Our goal is to assess how efficiently you can get up to speed with a technology stack you may be unfamiliar with, so we will guide you through setting up your local environment for subgraph development. We will also try to fill you in with some background knowledge about the concepts related to these tasks, which may be especially useful if your are new to the crypto space.

## Pre-requisites

You will deploy subgraphs on The Graph’s [hosted service](https://thegraph.com/hosted-service/dashboard), which you can login into using your [GitHub](https://github.com/) account. To get you started quickly, here’s a summary of the steps to [install](https://thegraph.com/docs/developer/quick-start) The Graph CLI and initialize/deploy subgraphs (tested on Ubuntu 20.04.3 LTS).

### Install npm

#### Installing on Linux

One possibility to do this is using the Node Version Manager:

```bash
$ sudo apt update
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash # from https://github.com/nvm-sh/nvm#install--update-script
$ source ~/.bashrc
```

Now we can choose a specific version to install (you can use `nvm list-remote` to see available versions). Let's install `v17.2.0`:

```bash
$ nvm install v17.2.0

# Confirm installation worked
$ node --version
v17.2.0
$ npm --version
8.1.4
```

#### Installing on macOS

One possibility to do this is using Homebrew. To install Homebrew:

```bash
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# Confirm installation worked
$ brew -v

# Update
$ brew update
```

Now you can install Node via Homebrew:

```bash
$ brew install node

# Confirm installation worked
$ node -v
v17.2.0

$ npm -v
8.1.4
```

### Install The Graph CLI

```bash
$ npm install -g @graphprotocol/graph-cli

# Confirm installation worked
$ graph --version
0.25.1
```

## The tasks

You'll attempt 5 tasks which involve modifying and deploying existing subgraphs and creating and deploying your own subgraphs from scratch:

- [Task 1](./task-1/README.md): Introduction to subgraphs.
- [Task 2](./task-2/README.md): Add total reserves to a Compound subgraph.
- [Task 3](./task-3/README.md): Track [ENS](https://ens.domains/) token transfers.
- [Task 4](./task-4/README.md): Create a subgraph that tracks fees generated by the ENS protocol.
- [Task 5](./task-5/README.md): Create a subgraph that tracks premiums and settlement fees from ETH call options traded on Hegic.

Each of the directories linked above provide instructions specific for each task.

## General instructions

- Fork this repository, try to solve as many tasks as you can and push the solutions (source code) into your fork.
- Ensure you have a meaningful commit history and please adhere to the [`commitlint`](https://commitlint.js.org/) convention (to setup `commitlint` locally, run `npx husky install` from the root of this repository).
- The tasks are roughly in increasing order of difficulty so we suggest you tackle them in the order they are presented.
- We don't expect that solving these tasks will take more than 1 or 2 days.
- If you get stuck or find it difficult to finish any task on your own, reach out to us at `robert@tokenterminal.xyz`. We're happy to hop on a call and help out!
- We will discuss your solutions during a technical interview.

Good luck! 💪

# Introduction to Blockchain, Wallets, and Consensus Mechanisms

## Table of Contents

1. [Introduction](#introduction)
2. [What is Blockchain?](#what-is-blockchain)
3. [Blockchain Wallets](#blockchain-wallets)
4. [Consensus Mechanisms](#consensus-mechanisms)
   - [Proof of Work (PoW)](#proof-of-work-pow)
   - [Proof of Stake (PoS)](#proof-of-stake-pos)
   - [Other Consensus Mechanisms](#other-consensus-mechanisms)
5. [Applications of Blockchain Technology](#applications-of-blockchain-technology)
6. [Further Reading](#further-reading)

## Introduction

Welcome to the introductory guide on blockchain technology! This document aims to provide a comprehensive overview of key concepts such as blockchain, wallets, and consensus mechanisms.

## What is Blockchain?

- A blockchain is a distributed database or ledger shared among a computer network's nodes.
- Blockchain differs from a typical database in the way it stores information; blockchains store data in blocks linked together via cryptography.
- Blockchains are immutable, which means that the data entered is irreversible → transactions are permanently recorded and viewable to anyone.

### Key Features of Blockchain:

- **Decentralization**: No central authority controls the blockchain.
- **Transparency**: All transactions are visible to participants.
- **Immutability**: Once recorded, data cannot be easily altered.
- **Security**: Cryptographic techniques secure the data.

## Blockchain Wallets

- A blockchain wallet is a digital wallet that allows users to store, manage, and transact cryptocurrencies and other digital assets.
- Wallets come in various forms, including hot wallets (software wallets), cold wallets (hardware wallets).

### Types of Wallets:

- **Hot Wallets**: Connected to the internet, easy to use but potentially less secure (e.g., [metamask](https://metamask.io/)).
- **Cold Wallets**: Not connected to the internet, more secure but less convenient (e.g., [ledger](https://shop.ledger.com/)).

### Key Concepts:

- **Public Key**: An address that others use to send you cryptocurrency.
- **Private Key**: A secret key that you use to access and manage your funds.
- **Seed Phrase**: A recovery phrase or mnemonic phrase of 12 to 24 words generated by your wallet. It can be used to recover and restore access to your wallet.

  - Example of a 12-words Seed Phrase: "basket actual object roast balcony tourist brave session creek argue penalty amazing".

- <span style="color:red;">**IMPORTANT:**</span> Keep your **private key** and your **seed phrase** secure!!!

## Consensus Mechanisms

Consensus mechanisms are protocols used by blockchain networks to achieve agreement on the state of the blockchain among distributed nodes. They ensure the integrity and consistency of the data.

### Proof of Work (PoW)

- PoW is the original consensus mechanism used by Bitcoin.
- Miners solve complex mathematical puzzles to validate transactions and add them to the blockchain. This process requires significant computational power and energy.

### Proof of Stake (PoS)

- PoS is an alternative to PoW that requires validators to hold and lock up a certain amount of cryptocurrency as a stake.
- Validators are chosen to create new blocks and confirm transactions based on their stake and other factors, reducing energy consumption compared to PoW.

### Other Consensus Mechanisms

- **Delegated Proof of Stake (DPoS)**: Stakeholders vote for delegates to validate transactions.
- **Proof of Authority (PoA)**: Transactions are validated by a pre-approved group of nodes.
- **Practical Byzantine Fault Tolerance (PBFT)**: Designed to tolerate Byzantine faults, ensuring consensus despite malicious actors.

<!-- ## Applications of Blockchain Technology

Blockchain technology is used in various industries beyond cryptocurrencies, including:

- **Finance**: Cross-border payments, smart contracts, decentralized finance (DeFi).
- **Supply Chain**: Tracking the provenance of goods, improving transparency.
- **Healthcare**: Secure sharing of patient records, drug traceability.
- **Voting**: Secure and transparent election systems.
- **Real Estate**: Property records, automated transactions. -->

## Further Reading

- [Blockchain Basics](https://www.tutorialspoint.com/blockchain/index.htm)
- [Test dapp](https://metamask.github.io/test-dapp/)
- [Bitcoin Whitepaper by Satoshi Nakamoto](https://bitcoin.org/bitcoin.pdf)
- [Mastering Bitcoin by Andreas M. Antonopoulos](https://github.com/bitcoinbook/bitcoinbook)
- [Ethereum Whitepaper by Vitalik Buterin](https://ethereum.org/en/whitepaper/)

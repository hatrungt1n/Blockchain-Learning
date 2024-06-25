# Solidity Basics and Smart Contracts

## Table of Contents

1. [Introduction to Smart Contracts](#introduction-to-smart-contracts)
2. [Solidity Basic Concepts](#solidity-basic-concepts)
3. [Solidity Coding Conventions](#solidity-coding-conventions)
4. [Remix IDE](#remix-ide)
5. [ERC-20 Standard](#erc-20-standard)
6. [ERC-721 Standard](#erc-721-standard)
7. [ERC-1155 Standard](#erc-1155-standard)
8. [Useful documents](#useful-documents)

## Introduction to Smart Contracts

Smart contracts are self-executing contracts with the terms of the agreement directly written into code. They run on blockchain networks, such as Ethereum, and automatically enforce and execute the terms when predefined conditions are met.

## Solidity Basic Concepts

Solidity is a statically-typed programming language designed for developing smart contracts on the Ethereum blockchain. Below are some key concepts in Solidity:

- **Contract**: The fundamental building block of Solidity. It contains state variables, functions, and data types.
- **State Variables**: Variables that store data on the blockchain.
- **Functions**: Executable units of code within a contract.
- **Modifiers**: Used to change the behavior of functions.
- **Events**: Logging facility that allows you to write to the blockchain's log.
- **Inheritance**: Solidity supports multiple inheritance, enabling code reuse.

### Example of a Simple Solidity Contract

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleStorage {
    uint256 public storedData;

    function set(uint256 x) public {
        storedData = x;
    }

    function get() public view returns (uint256) {
        return storedData;
    }
}
```

## Solidity Coding Conventions

Adhering to coding conventions improves readability and maintainability. Here are some conventions:

- **File Naming**: Use CamelCase for Solidity file names.
- **Indentation**: Use 4 spaces for indentation.
- **Comments**: Use // for single-line comments and /\* \*/ for multi-line comments.
- **Function Naming**: Use mixedCase for function names.
- **Variable Naming**: Use mixedCase for variable names.
- **Constants**: Use ALL_CAPS for constants.

## Remix IDE

Remix IDE is an open-source web and desktop application that helps developers write, deploy, and test smart contracts in Solidity. It offers a range of features including:

- Syntax highlighting and auto-completion.
- Built-in compiler and debugger.
- Integration with Ethereum networks for deployment.

### Getting Started with Remix IDE

1. Open [Remix IDE](https://remix.ethereum.org/).
2. Create a new file with a .sol extension.
3. Write your Solidity code.
4. Compile the code using the Solidity compiler.
5. Deploy and test your contract using the Remix VM or connect to an Ethereum network.

## ERC-20 Standard

ERC-20 is a standard for fungible tokens on the Ethereum blockchain. It defines a common set of rules for tokens, making them interoperable with various platforms and services.

**Key function**

- **totalSupply()**: Returns the total supply of tokens.
- **balanceOf(address account)**: Returns the token balance of a specific account.
- **transfer(address to, uint256 amount)**: Transfers tokens to a specified address.
- **approve(address spender, uint256 amount)**: Approves another address to spend tokens on behalf of the token owner.
- **transferFrom(address from, address to, uint256 amount)**: Transfers tokens on behalf of the owner.

### Example

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MyToken is ERC20 {
    constructor(uint256 initialSupply) ERC20("MyToken", "MTK") {
        _mint(msg.sender, initialSupply);
    }
}
```

## ERC-721 Standard

ERC-721 is a standard for non-fungible tokens (NFTs) on the Ethereum blockchain. Each token is unique and can represent ownership of digital or physical assets.

**Key function**

- **ownerOf(uint256 tokenId)**: Returns the owner of a specific NFT.
- **transferFrom(address from, address to, uint256 tokenId)**: Transfers ownership of an NFT.
- **approve(address to, uint256 tokenId)**: Approves another address to transfer a specific NFT.
- **safeTransferFrom(address from, address to, uint256 tokenId)**: Safely transfers ownership of an NFT.

### Example

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC721/ERC721.sol";

contract MyNFT is ERC721 {
    uint256 public nextTokenId;
    address public admin;

    constructor() ERC721("MyNFT", "MNFT") {
        admin = msg.sender;
    }

    function mint(address to) external {
        require(msg.sender == admin, "only admin can mint");
        _safeMint(to, nextTokenId);
        nextTokenId++;
    }
}
```

## ERC-1155 Standard

ERC-1155 is a standard for multi-token contracts. It allows a single contract to manage multiple token types, including both fungible and non-fungible tokens.

**Key function**

- **balanceOf(address account, uint256 id)**: Returns the balance of a specific token type for an account.
- **balanceOfBatch(address[] accounts, uint256[] ids)**: Returns the balances of multiple token types for multiple accounts.
- **setApprovalForAll(address operator, bool approved)**: Approves or revokes approval for an operator to manage all of the caller's tokens.
- **safeTransferFrom(address from, address to, uint256 id, uint256 amount, bytes data)**: Safely transfers a specific token type.

### Example

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC1155/ERC1155.sol";

contract MyMultiToken is ERC1155 {
    uint256 public constant GOLD = 0;
    uint256 public constant SILVER = 1;
    uint256 public constant THORS_HAMMER = 2;

    constructor() ERC1155("https://api.example.com/metadata/{id}.json") {
        _mint(msg.sender, GOLD, 10**18, "");
        _mint(msg.sender, SILVER, 10**27, "");
        _mint(msg.sender, THORS_HAMMER, 1, "");
    }
}
```

## [Useful documents](SOLIDITY_USEFUL_DOCS.md)

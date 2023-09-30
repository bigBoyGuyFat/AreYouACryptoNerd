# AreYouACryptoNerd (MTK) 🚀

![License](https://img.shields.io/badge/license-MIT-blue.svg)

AreYouACryptoNerd is an Ethereum-based ERC-20 token with additional features. It incorporates OpenZeppelin contracts to provide functionalities such as burning, snapshotting, voting, and permit. This README provides an overview of the project and instructions for its usage.

## Table of Contents

- [About AreYouACryptoNerd](#about-areyouacryptonerd)
- [Features](#features)
- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Usage](#usage)
- [Snapshotting](#snapshotting)
- [Contributing](#contributing)
- [License](#license)

## About AreYouACryptoNerd 💡

AreYouACryptoNerd (MTK) is an ERC-20 token created for crypto enthusiasts. It extends the functionality of standard ERC-20 tokens with additional features such as burning, snapshotting, voting, and permit. This contract is written in Solidity and can be deployed on the Ethereum blockchain. ONLY CHADS CAN HOLD

## Features 🌟

- **Burning:** Token holders can burn (destroy) their tokens, reducing the total supply.
- **Snapshotting:** The contract supports snapshotting, allowing token holders to track historical balances and governance decisions.
- **Voting:** Token holders can participate in governance decisions using the ERC20Votes extension.
- **Permit:** Users can use the ERC20 permit function to approve token transfers without multiple transaction approvals.

## Getting Started 🚀

### Installation 🛠️

To use the AreYouACryptoNerd token contract in your Ethereum project, you can import it like this:

```solidity
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/token/ERC20/extensions/ERC20Burnable.sol";
import "@openzeppelin/contracts/token/ERC20/extensions/ERC20Snapshot.sol";
import "@openzeppelin/contracts/access/Ownable.sol";
import "@openzeppelin/contracts/token/ERC20/extensions/ERC20Permit.sol";
import "@openzeppelin/contracts/token/ERC20/extensions/ERC20Votes.sol";

contract YourContract is ERC20, ERC20Burnable, ERC20Snapshot, Ownable, ERC20Permit, ERC20Votes {
    constructor()
        ERC20("areYouACryptoNerd", "MTK")
        ERC20Permit("areYouACryptoNerd")
    {}
}
Usage 🚦
You can deploy this contract on the Ethereum blockchain and interact with it using a wallet or Ethereum development framework like Truffle or Hardhat. Ensure you have the necessary dependencies installed.

Snapshotting 📷
To create a snapshot of token balances, call the snapshot() function. This can be done only by the owner of the contract (as specified in the onlyOwner modifier). Snapshots are useful for tracking historical token balances and making governance decisions.

solidity
Copy code
function snapshot() public onlyOwner {
    _snapshot();
}
Contributing 🤝
Contributions to this project are welcome. Feel free to submit issues or pull requests. Please follow the project's code of conduct and licensing terms.

License 📝
This project is licensed under the MIT License - see the LICENSE file for details.

# Smart Contracts

A smart contract is a program that runs on a blockchain.

On Ethereum, smart contracts are executed by the Ethereum Virtual Machine (EVM).

## Ethereum Virtual Machine (EVM)

The EVM is the environment where smart contracts are executed.

Every node in the network runs the EVM to ensure the same results.

## Solidity

Solidity is the most popular programming language used to write Ethereum smart contracts.

It is similar to JavaScript in structure but designed for blockchain logic.

## Basic Solidity Example

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleStorage {
    uint256 public storedValue;

    function set(uint256 _value) public {
        storedValue = _value;
    }

    function get() public view returns (uint256) {
        return storedValue;
    }
}
```

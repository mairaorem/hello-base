# Advanced Smart Contract Example

This document introduces a slightly more advanced smart contract with events and state updates.

## Counter Contract with Event

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Counter {

    uint256 public count;

    event CountUpdated(uint256 newCount);

    function increment() public {
        count += 1;
        emit CountUpdated(count);
    }

    function decrement() public {
        require(count > 0, "Count cannot go below zero");
        count -= 1;
        emit CountUpdated(count);
    }
}
```
### State Variable

`uint256 public count;`

This variable is stored on-chain.  
Its value persists between transactions.

### Event

`event CountUpdated(uint256 newCount);`

Events allow the contract to emit logs that external applications can listen to.

They do not store data permanently on-chain but help with tracking activity.

### require()

The `require` statement prevents invalid state changes.

In this case, it ensures the counter cannot go below zero.

# On-Chain State

On-chain state refers to data that is permanently stored on the blockchain.

When a smart contract updates a state variable, the blockchain records that change.

## Why State Matters

State defines the current condition of a contract.

For example:
- Token balances
- Voting results
- Ownership records
- Counter values

State changes require gas because they modify blockchain storage.

## Example: Counter Contract

In the Counter contract, the variable `count` represents the contract's state.

Each time `increment()` or `decrement()` is called, the state changes and is permanently recorded.

## Gas Considerations

Each call to increment() or decrement() modifies storage and therefore consumes gas.

Efficient smart contract design aims to minimize unnecessary storage operations.

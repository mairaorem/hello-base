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

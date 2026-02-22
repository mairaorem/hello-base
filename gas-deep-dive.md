# Gas Deep Dive

Gas is the unit that measures computational work on Ethereum.

Every transaction consumes gas depending on the complexity of operations.

## Gas and State Changes

Operations that modify blockchain state cost more gas.

For example:
- Updating a storage variable
- Deploying a contract
- Writing new data to the blockchain

Reading data costs less than writing data.

## Gas in the Counter Contract

Calling `increment()` costs gas because it modifies the state variable `count`.

The blockchain must update storage permanently.

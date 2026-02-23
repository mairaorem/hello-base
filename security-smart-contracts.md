# Smart Contract Security Basics

Smart contracts are immutable once deployed.

Because they cannot be easily changed, security is critical.

## Reentrancy

Reentrancy occurs when a contract calls an external contract before updating its own state.

If not handled correctly, the external contract can call back repeatedly and exploit the logic.

## Checks-Effects-Interactions Pattern

A common defense against reentrancy is:

1. Check conditions
2. Update state
3. Interact with external contracts

Updating state before external calls reduces risk.

## Integer Overflow (Historical Issue)

Before Solidity 0.8.0, arithmetic operations could overflow.

Example:
If a uint256 exceeded its maximum value, it would wrap back to zero.

Since Solidity 0.8.0, overflow and underflow automatically revert transactions.

This significantly improved default safety.

## Security in the Counter Contract

The Counter contract uses:

- Solidity 0.8.0 (built-in overflow protection)
- require() to prevent invalid decrements

These are basic but important safety mechanisms.

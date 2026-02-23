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

# Smart Contract Security Basics

Smart contracts are immutable once deployed.

Because they cannot be easily changed, security is critical.

## Reentrancy

Reentrancy occurs when a contract calls an external contract before updating its own state.

If not handled correctly, the external contract can call back repeatedly and exploit the logic.

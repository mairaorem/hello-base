# Storage vs Memory

Solidity uses different data locations for variables.

The two most important are:

- Storage
- Memory

## Storage

Storage variables are permanently stored on-chain.

They are expensive to modify because they change blockchain state.

## Memory

Memory variables exist temporarily during function execution.

They are not stored permanently on-chain.

Memory is cheaper than storage.

## Example

```solidity
function example(uint256 _value) public pure returns (uint256) {
    uint256 temp = _value * 2; // stored in memory
    return temp;
}
```

This function does not modify storage.
It only uses memory and returns a value.

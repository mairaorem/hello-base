# Smart Contract Deployment

Deploying a smart contract means publishing its code to the blockchain.

Once deployed, the contract receives a unique blockchain address.

## Compilation

Before deployment, Solidity code is compiled into bytecode.

Bytecode is the low-level machine code understood by the Ethereum Virtual Machine (EVM).

## Bytecode

Bytecode is a sequence of instructions executed by the EVM.

When deploying a contract, the bytecode is included in a transaction sent to the network.

## ABI (Application Binary Interface)

The ABI defines how external applications interact with a smart contract.

It describes:
- Available functions
- Input parameters
- Return types
- Events

Frontends use the ABI to call contract functions.

## Deployment Process

1. Write the smart contract in Solidity
2. Compile it to generate bytecode and ABI
3. Send a deployment transaction containing the bytecode
4. The network assigns a contract address
5. The contract becomes part of the blockchain state

## Deployment and Gas

Deploying a contract costs more gas than calling a function.

This is because:
- Storage space is allocated
- The contract code is permanently stored on-chain

## Deployment on Base

Base is a Layer 2 network built on Ethereum.

Deploying on Base:
- Costs less gas compared to Ethereum mainnet
- Still inherits Ethereum security
- Uses the same EVM-compatible bytecode

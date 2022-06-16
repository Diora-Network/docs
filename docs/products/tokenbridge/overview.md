# Diora Token Bridge
The Bridge allows users to transfer assets between two chains in the Ethereum ecosystem. This is a customized version of [POA network Bridge](https://github.com/poanetwork/tokenbridge) 

![tokenbridge](/assets/bridge.png)

Diora's Token Bridge can be considered as a money-transferring system designed to solve the problem of users converting other cryptocurrency assets to Diora blockchain with a 1:1 ratio. At the same time, users can enjoy a faster and more liquid cross-chain crypto asset trading model.

## Bridge Elements
- The TokenBridge contained in the github repo.
- Solidity smart contracts. Used to manage bridge validators, collect signatures, and confirm asset relay and disposal.
- Bridge UI Application. A Dapp interface to transfer tokens and coins between chains.
- Bridge Monitor. A tool for checking balances and unprocessed events in bridged networks.
- Bridge Deployment. Manages configuration instructions for deployment.

## Network Definitions
Bridging occurs between two networks.

- Home - is a network with fast and inexpensive operations. All bridge operations to collect validator confirmations are performed on this side of the bridge.
- Foreign can be any chain; generally it refers to the Ethereum mainnet.

## Operational Modes
The TokenBridge provides next operational mode:
 ERC20-to-ERC20 ERC20-compatible tokens on the Foreign network are locked and minted as ERC20-compatible tokens (ERC677 tokens) on the Home network. When transferred from Home to Foreign, they are burnt on the Home side and unlocked in the Foreign network. This can be considered a form of atomic swap when a user swaps the token "X" in network "A" to the token "Y" in network "B".

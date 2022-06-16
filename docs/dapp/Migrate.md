# Migrate from Ethereum

!!! tip
    Every Dapp running on Ethereum can be easily ported to Diora!

## Overview

Because Diora emulates geth, our blockchain natively supports all EVM-compatible smart contracts and tools. This document describes the simple steps required to port your existing Ethereum Dapp to Diora.

## Connecting to our network


To connect to our network, see the RPC endpoints below. You can perform any RPC operation available in Ethereum on these URLs.

| Network RPC endpoint | Chain ID  |
| ----------- | ---------- |
| https://testnet.diora.network  | `:201` |

If you're using MetaMask, specify one of these URLs as a new, custom RPC.

If you're using Truffle, add the following section to your ```truffle.js``` file:

``` 
'use strict'

var HDWalletProvider = require("truffle-hdwallet-provider");

var mnemonic = '<PUT YOUR WALLET BACKUP KEY HERE>';

 module.exports = {
  networks: {
    development: {
      host: "127.0.0.1",
      port: 7545,
      gas: 4000000,
      network_id: "*"
    },
    defitestnet: {
      provider: function() {
        return new HDWalletProvider(mnemonic, 'https://testnet.diora.network');
      },
      gas: 1000000,
      network_id: 201
    }
  }
};
compilers: {
    solc: {
      settings: {
        evmVersion: "byzantium"
      }
    }
  }
};

```

## Yup, that's it

No need to rewrite your smart contracts or change any of your web3 code, you should be good to go! If you are having any problems, post in our Discord for direct access to, and immediate help from, some of our developers.
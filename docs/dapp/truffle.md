# Deploy with Truffle

## Compiling

To compile the source code, just type this command in the repository directory.

``` $ truffle compile ```

The following result should be shown.
```

Compiling ./contracts/Migrations.sol...
Compiling ./contracts/SimpleContract.sol...
Writing artifacts to ./build/contracts 

```

Now your smart contract has already been compiled. The compiled code are stored in the ```build``` directory. 

Setting up the Deployment Wallet

We need to specify the Diora wallet to deploy the smart contract first.  Here is the steps to Open ```truffle.js``` file. Here is the content inside.

```

'use strict'

var HDWalletProvider = require("truffle-hdwallet-provider");

var mnemonic = '<PUT YOUR WALLET BACKUP KEY HERE>'
	
	;module.exports = {
  networks: {
    development: {
      host: "127.0.0.1",
      port: 7545,
      gas: 4000000,
      network_id: "*"
    },
    tomotestnet: {
      provider: function() {
        return new HDWalletProvider(mnemonic, 'https://testnet.diora.network');
      },
      gas: 1000000,
      network_id: 201
    }
  }
}; 

```
Copy the backup key obtained from DeFiMask and paste it as a value of ```mnemonic``` variable.

``` var mnemonic = '<PUT YOUR WALLET BACKUP KEY HERE>'; ```

!!! tip 
Please note that the Diora testnet network will be used to deploy the smart contract we created. However, if you are familiar with Ganache, you could use the ```development``` network to do the local test as well if you want to.

## Deploying

Now it is time to deploy the smart contract to the Diora testnet! You can deploy the compiled smart contract using the following command.

``` $ truffle migrate --network dioratestnet ```

After a few seconds, the smart contract will be migrated successfully to Diora Testnet.



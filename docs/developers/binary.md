This guide shows how to run a Diora masternode in testnet and 
mainnet without the need of using Docker and `tmn`.


## Install Rust
  
```bash

```
    
## Prepare Diora client software
#### Build from source code
Create new directory for the project

- Download source code and build
```bash
git clone https://github.com/diora-network/diora.git
cd diora
```

- Checkout the latest version (e.g v1.4.1)
```
git pull origin --tags
git checkout v1.4.1
```

- Build the project
```
cargo build --release
```



## Start a node
    
#### Let's start a node
```bash

```

If you are a Dapp developer, you should open RPC and WS apis:
```bash

```

#### Some explanations on the flags
   
```
--verbosity: log level from 1 to 5. Here we're using 4 for debug messages
           
--datadir: path to your data directory created above.
           
--keystore: path to your account's keystore created above.
           
--identity: your full-node's name.
           
--password: your account's password.
           
--networkid: our network ID.
           
--port: your full-node's listening port (default to 30303)
           
--rpc, --rpccorsdomain, --rpcaddr, --rpcport, --rpcvhosts: your full-node will accept RPC requests at 8545 TCP.
           
--ws, --wsaddr, --wsport, --wsorigins: your full-node will accept Websocket requests at 8546 TCP.
           
           
--targetgaslimit: Target gas limit sets the artificial target gas floor for the blocks to mine (default: 4712388)
           
--bootnode: bootnode information to help to discover other nodes in the network
           
--gcmode: blockchain garbage collection mode ("full", "archive")
           
--dev: start in dev mode


```
To see all flags usage
   
```bash
 --help
```


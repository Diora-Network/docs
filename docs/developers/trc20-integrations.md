This tutorial is a guide for a developer who wants to know how to integrate ERC20 token to applications (e.g. wallet, exchange)

Smart Contract ABI:

ERC20 Contract Interface:
```javascript
function totalSupply() public view returns (uint);
function balanceOf(address tokenOwner) public view returns (uint balance);
function allowance(address tokenOwner, address spender) public view returns (uint remaining);
function transfer(address to, uint tokens) public returns (bool success);
function approve(address spender, uint tokens) public returns (bool success);
function transferFrom(address from, address to, uint tokens) public returns (bool success);

event Transfer(address indexed from, address indexed to, uint tokens);
event Approval(address indexed tokenOwner, address indexed spender, uint tokens);
```

Diora provides RPC APIs. So you can use Web3 library to directly call the functions in the smart contract.

You can follow the steps below to interact with the smart contract by using Web3 library and NodeJS.

## Init Web3 provider
At the first step, you need init Web3 provider by connecting Diora Fullnode RPC endpoint.

You can take a look to [Diora Networks](https://docs.Diora.com/general/networks/) page to get the details of Testnet/Mainnet network information.

```javascript
const Web3 = require('web3')
const web3 = new Web3('https://testnet.diora.network')
const chainId = 201
```

## Unlock wallet
To create a wallet, you can refer to Create wallet page

You need to unlock the wallet before interact ERC20 contract
#### Example
```javascript
// Unlock wallet by private key
const account = web3.eth.accounts.privateKeyToAccount(pkey)
const holder = account.address
web3.eth.accounts.wallet.add(account)
web.eth.defaultAccount = holder
```

## Init Web3 ERC20 Contract

```javascript
const erc20Abi = require('./TRC20.json')
const address = '[enter_your_contract_address]'
const erc20 = new web3.eth.Contract(trc20Abi,
        address, {gasPrice: 250000000, gas: 2000000 })
```


## Check balance
You need to call function `balanceOf()` from ERC20 contract to check your token balance for an address.

#### Example
```javascript
erc20.methods.balanceOf(holder).call()
.then((result) => {
    console.log(result)
}).catch(e => console.log(e))
```

## Estimate TX fee (gas)
Before sending tokens, you need to estimate fee to make sure you have enough DIR for sending.

You need to use this method:
```
myContract.methods.myMethod([param1[, param2[, ...]]]).estimateGas(options[, callback])
```

#### Example
```javascript
erc20.methods.transfer(to, '500000000000000000000').estimateGas({
    from: holder
})
.then((result) => {
    console.log(result)
}).catch(e => console.log(e))

```

## Transfer token
Token holder needs to call function `transfer` to send token to an address

#### Example
```javascript
// send 500000000000000000000 tokens to this address (e.g decimals 18)
const to = "0xf8ac9d5022853c5847ef75aea0104eed09e5f402"
erc20.methods.transfer(to, '500000000000000000000').send({
    from: holder,
    gas: 2000000,
    gasPrice: 250000000,
    chainId: chainId
})
.then((result) => {
    console.log(result)
}).catch(e => console.log(e))

```



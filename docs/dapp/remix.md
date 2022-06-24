## Getting started with Remix


* Head over to [Remix IDE](https://remix-project.org) official site to launch it.

* Create a workspace and a file in it named MyToken.Sol in root directory.

![overview](/assets/remix.png)

* Paste following code in MyToken.sol

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.2;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract MyToken is ERC20, Ownable {
    constructor() ERC20("MyToken", "MTK") {
        _mint(msg.sender, 1000 * 10 ** decimals());
    }

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }
}

```

!!! tip
    This is a mintable ERC20 contract based on openzeppelin. It creates MyToken with symbol ‘MTK’ and initially mints 1000 MTK to the owner of the contract. You can generate this code from OpenZeppelin contract wizard
   

* Navigate to the solidity compiler  from the left side navigation and then click on Compile MyToken.sol

![overview](/assets/remixa2.png)


Remix will download all the openzeppelin dependencies and compiles the contract

* Deploy the contract

1. Navigate to the deploy and run transaction tab from left side navigation

2. Change the environment to injected web3 from Environment dropdown. This will invoke the metamask extension in your browser. Make sure your metamask is configured to diora testnet.

3. Select the account from metamask and confirm the connection
From contracts dropdown select MyToken.sol and click on Deploy button

4. From contracts dropdown select MyToken.sol and click on Deploy button

![overview](/assets/remix1.png)

* You will be asked to confirm the transaction through metamak popup , confirm it and wait till it is deployed.

* The contract details will appear under deployed contracts in remix

![overview](/assets/remix3.png)

Hence we deployed ERC20 token using Remix on diora testnet node
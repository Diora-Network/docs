## Prerequisites

- Have a wallet connected to Diora (See [this tutorial](/get-started/wallet))

## Introduction

With a connected wallet, it's not time to try voting (staking) for some masternodes.

## Get some DIR

!!! info
    Testnet DeFi are only used for experimenting with the testnet.
    They have no value in the main blockchain and not market value.
	
	

### Using Web Wallet

DeFi Web Wallet provides a function named `Earn DIR to test`. It allows you to get 25 DIR on the Testnet.
Just click on it and you will see your balance go up.

!!! note
    You can use this function only once. You then have to use the faucet for any extra Testnet DeFi needed.

### Using Metamask and other wallets

We also have a service called "Faucet" which allows you to get 15 DIR at a time.

Access the faucet site at: [GET TOKENS HERE](https://diorafaucet.netlify.app)

Enter your wallet address in the field and tick the `I'm not a robot` box.

Click `REQUEST 25 DIR` and Wait for some seconds for the transaction to be confirmed.

You will receive a success confirmation message and the amount of DeFi in your wallet should be updated. You can check your DeFi balance by either looking at your wallet or using Diora explorer.

## How To Vote

Now you have some DIR. You can access our governance Dapp, "DeFiMaster" to start voting for masternodes.


DeFiMaster natively supports MetaMask, Polkadot.js & DeFiMask. You can also access your account page (the vertical three dots on the top right) to fill in your wallet Private Key or MNEMONIC.

Once configured, you can vote for masternodes by clicking on the `Vote` button.

At least 100 DeFi is required per vote. After clicking submit, your DIR will be sent to the voting smart contract and locked there.

## Reward
Every epoch (~30 minutes), you will automatically receive rewards for each masternode you voted for.

## How to Unvote

If you do not want to support a masternode you voted for, you can unvote it by clicking the `Unvote` button on the masternode's page and enter the amount of DIR you want to unvote.

After unvoting, your DIR is still locked in the smart contract for 48 hours before you are able to withdraw.

## How to Withdraw

For withdrawals after unvoting, you need to wait until your DeFi is unlocked from the smart contract. Then you can click the `withdraw` button in your account page (the vertical three dots on the top right) and choose which withdrawal you want to receive back your DIR.

Note that you might see multiple withdrawals on your account page if you made multiple unvotes previously.

If you withdraw before the unlock period expires, an error will be raised.

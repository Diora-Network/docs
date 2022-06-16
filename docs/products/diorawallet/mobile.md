
## MetaMask

!!! tip
    We have created DeFiMask a reskinned version of MetaMask that automaticly connects with Diora Networks and shows the correct values.
	
Get started! You first need to install [MetaMask Extension](https://metamask.io/).
Once you agree to the Metamask Terms of Use and create an account successfully, follow instructions:

**Step 1:** Click MetaMask logo on the browser to open the Extension -> select `Network` -> select `Custom RPC` as shown below:

![metamask1](/assets/metamask1.jpg)

**Step 2:** When Settings screen pops up, scroll down to `New Network` and click `Show Advanced Options`.
Enter the following information, then Save:

- New RPC URL: `https://testnet.diora.network`
- ChainID: `201`
- Symbol: `DIR`
- Nickname: `Diora Testnet`

![metamask2]()

Set `Privacy Mode` On, if you want to connect Metamask with your hardware wallet (Trezor, Ledger Nano S).

![metamask3](/assets/metamask3.jpg)

**Step 3:** You are successfully connected to Diora Testnet.

### Known issues with MetaMask
Since MetaMask was originally developed for Ethereum, certain info displayed in MetaMask can be somewhat misleading when you are using it for the Diora. Notably, there are multiple places in the UI that uses ETH (ether) as the unit, when they are really referring to DIR. By extension, the USD numbers are incorrect too, since they are computed using the price of ether. This is the main reason we built DeFiMask.

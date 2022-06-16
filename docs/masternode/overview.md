# PoSM Expained 

#### PoSM
!!! tip
    Diora masternode is a server which uses its computing power to contribute to the network, Its job is to create and sign blocks. For this contribution to the network, masternodes receive rewards in the form of DIR.

Diora Network proposes the Proof of Stake Masternode (PoSM) consensus, which is a PoS/PoW hybrid consensus protocol with a fair voting mechanism, rigorous security guarantees, and uniform probability eventually.

We apply PoSM with voting and Double Validation to create, verify and vote for blocks smoothly and efficiently. Whenever potentials of fork branches are detected, we employ the idea in PoW to select the longest branch with the most votes and discard the other branches. With this hybrid approach, PoSM does not only increase the performance and security of blockchain, but also reduce the fork situation in an efficient and practical manner. 

Masternodes contribute to the network and for this work they will receive a significant amount of block rewards, which will far exceed the cost for running the infrastructure. However, masternode owners need to invest in Diora by depositing at least 25,000 DIR, and stake them in the long term.

![overview](/assets/feat3.svg)

#### What criteria must be considered when Masternode? Which masternode candidate should I vote for?
The most important criteria to maximize voter’s profit, the main points you should consider when Masternode, are the following:

- **Top-150 most voted:** Your candidate must be one of the top-150 most-voted. If your candidate gets in the 151th most-voted place, it will not be promoted to masternode and you will earn zero rewards.
- **Hardware, Performance:** Powerful CPU, RAM, bandwidth, latency, etc so the node can work hard and receive high rewards
- **Number of signed blocks:** The more signed blocks per epoch, the higher rewards
- **Time of last signed block:** Verify that the masternode is active
- **Total Capacity:** Staking rewards are shared between all the masternode votes. Less voted masternodes are more profitable. 5K staked on a 50K-staked masternode will receive ten times more rewards than 5K staked on a 500K total staked masternode.
- **Social Proof, Reputation:** Masternodes managed by trusted companies that are for the long term, maintaining the masternode, updating hardware and software to last versions, fixing problems, etc.

#### Staking

Token holders can stake DIR and receive rewards.

To stake DIR you need to vote for masternode candidates by sending DIR to each candidates specific Masternode-address using the official governance dapp: DeFiMaster.`
The top-150 most voted candidates will become masternodes.
Token holders can also un-vote candidates, but the tokens will be locked for the next 96 epochs / 8,640 blocks (approx. 48 hours) after the un-Masternode.

Masternode token deposits, and all tokens used to vote for masternodes will enter the staking program, and earn block rewards in each epoch, plus any fees.
Tokens used to vote for candidates who do not become masternodes will not earn staking rewards.


#### What is 'Slashing'?

With Slashing v2.0, a masternode who doesn't create any block within an epoch and therefore delays the network by 10 seconds at each of their turns will be penalized (no rewards) for the next five epochs.
With Slashing  a masternode who doesn't create any block within an epoch and therefore delays the network by 10 seconds at each of their turns will be penalized (no rewards) for the next five epochs.

Note: a slashed Masternode can still sign transactions if he’s online but receive no rewards for doing so.

After being slashed for 5 epochs, the Masternode is analysed for re-entry.
If the slashed Masternode have signed any transaction during the last epoch (meaning that he's up and working again) it will come back to its Masternode status and receive rewards normally.
Otherwise it will be slashed for a new round of 5 epochs.
This can happen as long as the node isn't back up or kicked out of the top 150.

Some reasons for being Slashed might be that the masternode does not have the correct Diora software, lack of memory or masternode crashes due to the lack of e-maintenance and operation by the masternode owner.


#### How much reward from Masternodes will go to the Masternode infrastructure (node owner) and how much is for voters?
There is a reward sharing ratio among token holders and masternode who has been elected supported by the token holders.
The reward achieved by each Masternode will be divided into three portions:

- **Infrastructure Reward:** The first portion of 40% called Infrastructure Reward goes to the Masternode operator.
- **Staking Reward:** The second portion of 50% called Staking Reward goes to the pool of all voters for that Masternode which is shared proportionally based on the token stake.
The Masternode also gets proportional rewards for his 25K DIR initial deposit.
- **Treasury Reward:** The last portion of 10% called Tresuary Reward goes to a special treasury account which is controlled and run by the Diora commuinty through on-chain goverance. 


# Gas Rebates

Unlike existing smart contract platforms, Diora does not burn gas fees or distribute them entirely to the validators or miners. Instead, the collected gas fees are split between dApp developers, masternodes and our on-chain tresuary.

At network launch, gas fees are divided as follows. 


- 50% of all gas fees go to the dapp rewards pool for GAS Rebates

- 20% of all gas fees go to refill PoSM block rewards pool for after the 8 year period

- 30% of all gas fees go to treasury split 50/50 with DioraDAO & on-chain treasury

From the developer perspective, a contract receives a 50% rebate on all gas paid. From the masternode perspective, deferring a portion of rewards in the near term effectively drives transaction volumes, fees, and increases the value of the underlying network in the future.

It would not be profitable for an attacker to spam transactions on the network as gas rebates recoup only part of the fees paid (50%). As an additional safeguard against potential abuse and to prevent the deployment of spam contracts, gas fees are higher for uploading new contracts than for routine transactions. Gas fees are still sufficiently low to allow smaller projects to upload contracts.

Gas fee rebates are automatically paid out by the network on a per-block basis.


# Gas Tracking

to achieve the diora architecture desired properties, the gas tracking module follows this design:

Wrap the SputnikVM with a GasMeter to allow interception and tracking of information passed by the VM.

During launch, the recorded information is brought to memory and processed to determine rewards for each of the contracts executed in the last block.

Developers can choose to take the rewards or give the gas rebate to end users to subsidize transaction costs. 



![overview](/assets/feat.svg)

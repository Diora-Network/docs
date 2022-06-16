This tutorial shows you how to run a full node and meet the requirements 


## General hardware notice

The Diora team has extensively tested performances and 
come up with those minimal requirements for any Diora masternode host.

**Testnet**

- Must be facing internet directly (no NAT, public IP)
- Must have at least 2 cores
- Must have at least 8GB of RAM
- Must use an IaaS ("cloud") provider of your choice (AWS, Digital Ocean, Google Cloud, etc.).
- Storage must be SSD

**Mainnet**

- Must be facing internet directly (no NAT, public IP)
- Must have at least 16 cores
- Must have at least 32GB of RAM
- Must use an IaaS ("cloud") provider of your choice (AWS, Digital Ocean, Google Cloud, etc.)
- Storage must be SSD


We recommend using popular cloud providers as there reliability and uptime are close to 100%.
Those servers would be a good starting point:

- **DigitalOcean**: CPU optimized droplet 32GB/16CPU
- **Amazon EC2**: C5 instance
- **Google Cloud Engine**: n1-highcpu-16

Setting up a masternode candidate on a weaker machine might result in poor performances.
Significantly impacting owner's rewards and the chain performance.

If you have other production grade environment than cloud provider at your disposal, please come chat with us on our [Discord]().

!!! info Performances
    A masternode has a certain amount of tasks to process (validations, block creations, etc.) over time.
    You masternode should be able to process all the tasks that are attributed to him or the rewards will be negatively impacted.
    However, over sizing your masternode will not get you more rewards.


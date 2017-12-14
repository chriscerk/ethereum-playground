# My Ethereum Playbook

## Parity

The simple route: parity.io

## Geth

From experience, installing & running `geth` (go-ethereum) through Ubuntu Subsystem on Windows 10 wasn't worth the hassle. These are some steps to get up and running relatively quickly.

### Install
`https://ethereum.github.io/go-ethereum/downloads/`

### External Drive Use - Windows
Requirements: SSD drive with at least 30GB (64 GB USB stick works well)
1. Create symbolic link to external drive `mklink /D "C:\Users\Christopher\AppData\Roaming\Ethereum" "D:\ethereum" `
2.  Downloading the chain data (can take up to 3-6 hours, recommend `--cache 4096` if you have 16GB RAM) `geth --datadir "D:\ethereum" --cache 2048` 

### Get Syncing Status
1. Run `geth attach`
3. `100 * eth.syncing.currentBlock / eth.syncing.highestBlock` for percent complete
2. `eth.syncing` for full details

### Develop

1. Install `solidity` from Visual Studio Code marketplace
2. Use the test-net `geth --testnet console`

### Install Wallet
Now that you have the full chain, download the wallet
1. `https://github.com/ethereum/mist/releases`


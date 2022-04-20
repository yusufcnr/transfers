# Near Protocol Whitelist dApp
Welcome!
This small project is written in Assemblyscript using Near Protocol Sample project. 
The purpose of the project is to whitelist the users who have interacted with our decentelized application on NEAR protocol for their early support.
Anyone can interact with the project by attaching 0.1 NEAR. 
Maximum number of the whitelisted wallets is limited to 10.
Everyone interacted with dapp will receive 0.2 when whitelist period is over.
User need to wait 30 days after the before they can call getRewards method to get their rewards.

### Getting started
Before getting started we need to get a testnet account from Near Protocol in order to interact smart contracts.

### Get Near Protocol Testnet Account from:

https://wallet.testnet.near.org/

## install dependencies from packacge.json file like this: (Reuire yarn installed)

Install yarn (package manager) from terminal like this: 

`sudo apt install yarn`

Then istall dependencies and node modules using yarn package manager :

`yarn`

### Install `NEAR CLI` in order to interact with Smart Contract like this:

`npm i -g near-cli`

### Check if NEAR CLI is installed properly like this:

`near --version`

1. clone this repo to a local folder:  

3. `git clone https://github.com/yusufcnr/transfers.git`

4. run `yarn build:release`

5. run `near dev-delpoy ./build/release/simple.wasm`


or basically run 1.dev-deploy.sh script like this:

`./scripts/1.dev-deploy.sh`

6. run `./scripts/2.use-contract.sh`

7. run `./scripts/2.use-contract.sh` (run it to see changes)

## Usage

## Interacting with smart contract

Interacting with smart contract requires user to attach 0.1 NEAR in order to get in the whitelist.
Run this command to interact with smart contract:

`near call $CONTRACT interact --amount 0.1 --accountId <YOUR_ACCOUNT.testnet>`

## Check whether you are whitelisted or not:

`near call $CONTRACT checkWhitelistStatus --accountId <YOUR_ACCOUNT.testnet>`

## Check number of whitelisted addresses:

`near call $CONTRACT checkWhitelistStatus --accountId <YOUR_ACCOUNT.testnet>`
## Retrieve the list of whitelisted addresses:

`near view $CONTRACT getListOfWhitelistedAddresses --accountId <YOUR_ACCOUNT.testnet>`

## Send rewards to whitelisted wallets after the whitelisting process is over:

`near call $CONTRACT sendRewards --accountId ycfinans.testnet`

## Retrieve name of the contract by calling getContractName

`near call $CONTRACT getContractName --accountId <YOUR_ACCOUNT.testnet>`
# Ethereum Dapp for Tracking Items through Supply Chain

## UML
### Activity
![activity_diagram.png](images%2Factivity_diagram.png)
### Sequence
![sequence_diagram.png](images%2Fsequence_diagram.png)
### State
![state_diagram.png](images%2Fstate_diagram.png)
### Classes
![classes_diagram.png](images%2Fclasses_diagram.png)

## Libraries
- truffle-hdwallet-provider: ^1.0.17
- web3: ^1.8.1

## Deploy smart contract on a public test network
- Transaction ID: 0x35e2cb557b4c8aafaa44d2592a992ca22da4c8eb77d544bb12aab6dd6267ff2b
- Contract address: 0x0237e0bdfff12b7ea83a5aa3b77edbd1d31d5271
```
daisuke@Daisukes-MacBook-Air project-6 % truffle migrate --reset --network goerli
Using network 'goerli'.

Running migration: 1_initial_migration.js
  Deploying Migrations...
  ... 0x510fe2d3dd19dc42658080c8690ad62219e5c1163a2dbd26c659247223e209d2
  Migrations: 0x176ba5243d294d6d884763e993184db19fca6e83
Saving successful migration to network...
  ... 0xdc3fc7b1a66c14ea37da1ef9b0a0b8ee83810bbf2ec1f8c858d2493b8132e498
Saving artifacts...
Running migration: 2_deploy_contracts.js
  Deploying FarmerRole...
  ... 0x5bc5806d8f7f34adf93635acdac344409f210fbfeb029aa5db75b616f4c348be
  FarmerRole: 0xfe33dc820f3f01cd984a08dca1d2ac1b1f962204
  Deploying DistributorRole...
  ... 0x1951fdcb946eefc0d284bca298b35a40387fbec5b8711bf81b62e33c9fc62938
  DistributorRole: 0xb552dbbc8b8838d76f389f3eea857ea3c5de688d
  Deploying RetailerRole...
  ... 0x5e9054a85c29b16dd3355460d38a1b0a021fe98efbd5a02f0c7ef8447aa9a03b
  RetailerRole: 0x30de613662dbce4ab349a06a2e9578905084f46c
  Deploying ConsumerRole...
  ... 0x4033c6f81c8fa41895d748aa0690eabb35afd1293d98c5ee6e39a9b33ba65beb
  ConsumerRole: 0x2db3669a4c61d7dbfd6dea5795698429cec3a9da
  Deploying SupplyChain...
  ... 0x35e2cb557b4c8aafaa44d2592a992ca22da4c8eb77d544bb12aab6dd6267ff2b
  SupplyChain: 0x0237e0bdfff12b7ea83a5aa3b77edbd1d31d5271
Saving successful migration to network...
  ... 0xdfccba85612e621592b5e197e04b9eff37eb35800c2e39f94122e9f6281e02ab
Saving artifacts...
daisuke@Daisukes-MacBook-Air project-6 % 
```
![deploy.png](images%2Fdeploy.png)

# Supply chain & data auditing

This repository containts an Ethereum DApp that demonstrates a Supply Chain flow between a Seller and Buyer. The user story is similar to any commonly used supply chain process. A Seller can add items to the inventory system stored in the blockchain. A Buyer can purchase such items from the inventory system. Additionally a Seller can mark an item as Shipped, and similarly a Buyer can mark an item as Received.

The DApp User Interface when running should look like...

![truffle test](images/ftc_product_overview.png)

![truffle test](images/ftc_farm_details.png)

![truffle test](images/ftc_product_details.png)

![truffle test](images/ftc_transaction_history.png)


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Please make sure you've already installed ganache-cli, Truffle and enabled MetaMask extension in your browser.

ganache and Truffle (ganache-cli has been changed to ganache.)
```
npm i -g ganache
npm i -g truffle@4.1.14
```

Metamask extension
```
1. Open a browser such as Google Chrome and search for the MetaMask extension.
2. Access the extension page and click "Add to Chrome".
3. The extension will be installed and an icon will appear on the top right corner of the browser. Click on the icon to open the settings.
4. Create or import an account and set a password.
5. MetaMask is now enabled and ready to use.
```

### Installing

> The starter code is written for **Solidity v0.4.24**. At the time of writing, the current Truffle v5 comes with Solidity v0.5 that requires function *mutability* and *visibility* to be specified (please refer to Solidity [documentation](https://docs.soliditylang.org/en/v0.5.0/050-breaking-changes.html) for more details). To use this starter code, please run `npm i -g truffle@4.1.14` to install Truffle v4 with Solidity v0.4.24. 

A step by step series of examples that tell you have to get a development env running

Clone this repository:

```
git clone https://github.com/dai175/nd1309-Project-6b.git
```

Change directory to ```project-6``` folder and install all requisite npm packages (as listed in ```package.json```):

```
cd project-6
npm install
```

Launch Ganache:

```
ganache -m "spirit supply whale amount human item harsh scare congress discover talent hamster"
```

Your terminal should look something like this:

![truffle test](images/ganache-cli.png)

In a separate terminal window, Compile smart contracts:

```
truffle compile
```

Your terminal should look something like this:

![truffle test](images/truffle_compile.png)

This will create the smart contract artifacts in folder ```build\contracts```.

Migrate smart contracts to the locally running blockchain, ganache-cli:

```
truffle migrate
```

Your terminal should look something like this:

![truffle test](images/truffle_migrate.png)

Test smart contracts:

```
truffle test
```

All 10 tests should pass.

![truffle test](images/truffle_test.png)

In a separate terminal window, launch the DApp:

```
npm run dev
```

## Built With

* [Ethereum](https://www.ethereum.org/) - Ethereum is a decentralized platform that runs smart contracts
* [IPFS](https://ipfs.io/) - IPFS is the Distributed Web | A peer-to-peer hypermedia protocol
to make the web faster, safer, and more open.
* [Truffle Framework](http://truffleframework.com/) - Truffle is the most popular development framework for Ethereum with a mission to make your life a whole lot easier.


## Authors

See also the list of [contributors](https://github.com/your/project/contributors.md) who participated in this project.

## Acknowledgments

* Solidity
* Ganache-cli
* Truffle
* IPFS

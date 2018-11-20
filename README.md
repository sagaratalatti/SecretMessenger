# Secret Messenger - Ethereum Smart Contract

Working towards setting up your **blockchain** to connect with a front end application. Using an HTML file, then switch to serving this live on our local host and [Rinkeby](https://www.rinkeby.io/). We will be deploying smart contract to local ethereum blockchain by [Ganache](https://truffleframework.com/ganache)


# Prerequisites

- [Metamask](https://metamask.io/) - Brings **Ethereum** to your browser.
- [Ganache](https://truffleframework.com/ganache) - One click **BLOCKCHAIN**
- [Visual Studio Code](https://code.visualstudio.com/download) - is a source code **editor** developed by Microsoft

Download and install Metamask as Chrome browser extension. 

 1. Create your new wallet by generating mnemonic passphrase. Do not forget to backup your passphrase key.
 2. Choose Rinkeby test network as we will be working with Test Ethers which don't cost any money.  
 ![Rinkeby Test Network](https://i.imgur.com/LsaEdLT.png)
 3. To receive free ethers please request from Rinkeby [faucet](https://www.rinkeby.io/#faucet). Follow the instructions there.
 4. Install Ganache and Run the application for one click ethereum blockchain deployment on localhost.
 ![Ganache Application](https://i.imgur.com/7rvG8hc.png)
 You will find the blockchain has been deployed to ``http://127.0.0.1:7545``. The ganache will also create Ethereum wallet addresses for you, all addresses are loaded with 100.00 Ethers and Mnemonic passphrase.

## Project Setup

**Dependencies Used**

 1. [Web3](https://www.npmjs.com/package/web3) -  Ethereum API

**Dependencies Installation**

 2. Download and open project in Visual Studio Code or any other code editors.
 3. Open terminal and install all dependencies by running command ``npm install``

**Working with Project**

 1. Open ``index.html`` file in your Chrome browser.
 2. Any changes made to code you will need to refresh the page on browser to update changes.
 3. Copy code from ``messenger.sol`` and paste the code to [Remix](https://remix.ethereum.org/) solidity EVM. Remix will help you interact with your Ganache Local Blockchain and Metamask wallet.

## Using Ganache - Local Ethereum Blockchain

Once you have deployed the Ganache Local Ethereum Blockchain on localhost you need to make the following steps to this project.

1. Go to [Remix](https://remix.ethereum.org/) EVM and click start to compile.
2. In Remix go to Run tab and select Web3 Provider to connect to Ganache. After selecting web3 provider you need to enter the RPC address where the Ganache blockchain has been deployed. You will find the RPC address in your Ganache Application. 
![RPC Server Address](https://i.imgur.com/hid7zL1.png)
3. Once you have successfully connected to Ganache blockchain you should see your Ganache Ethereum addresses with 100 Ethers in Remix. 
![enter image description here](https://i.imgur.com/XL1Vgyc.png)

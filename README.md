# Secret Messenger - Ethereum Smart Contract

Working towards setting up your **blockchain** to connect with a front end application. Using an HTML file, then switch to serving this live on our local host.. We will be deploying smart contract to local ethereum blockchain by [Ganache](https://truffleframework.com/ganache)


# Prerequisites

- [Ganache](https://truffleframework.com/ganache) - One click **BLOCKCHAIN**
- [Visual Studio Code](https://code.visualstudio.com/download) - is a source code **editor** developed by Microsoft

 1. Install Ganache and Run the application for one click ethereum blockchain deployment on localhost.
 
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

![Remix connected with Ganache](https://i.imgur.com/XL1Vgyc.png)

4. Deploy the message contract by clicking Deploy button in Remix.
5. In Remix console you will find the new section below as Deployed Contracts will show your contract there. Click on the message contract and copy the deployed contract address.

![Copy deployed contract address](https://i.imgur.com/tXzCgvO.png)

6. Open ``index.html`` in Visual Studio Code editor and find this code:
 ``var myMessage = RemixContract.at('Enter Your Contract Address');``
 paste your contract address there.
7. We also need to copy + paste the ABI code for our contract from Remix. You will find the ABI code to copy in compile section from remix console.

![Copy ABI code](https://i.imgur.com/6mhrchB.png)

8. Paste ABI code in your ``index.html`` within this code: 
``var RemixContract =  web3.eth.contract('Enter your ABI code here');``
9. Now we need to connect Ganache with your ``index.html`` copy the RPC Server address from Ganache Application within this code: 
``web3 =  new  Web3(new  Web3.providers.HttpProvider("Enter RPC Server"));``
10. Refresh your ``index.html`` in chrome browser to updated all the changes we have made so far.

**Testing the Project**

1. Open console in Google Chrome to see logs from the project. Options>More Tools>Developer Tools> Console.
2. Type any secret message you want and click Set Secret Message.
3. You should see the output in console log. 

![Chrome console log](https://i.imgur.com/nZ5FDsY.png)
and you will also find the transaction in your Ganache application in the Transaction section.

![Ganache Transaction](https://i.imgur.com/eXNKMcy.png)

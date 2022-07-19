<h1 align="center">
  <img alt="cgapp logo" src="https://github.com/Divijkatyal0406/MediBuddy/blob/master/images/readme_header1.png" width="224px"/><br/>
  A Revolutionary e-Health Platform
</h1>

<div align="center">
<h3 align="center">
  Table of Contents
  </h3>
</div>


<div align="center">

**PROJECT PHILOSOPHY • 
INSTALLATION • 
TECH STACK • 
CONFIGURATION • 
ARCHITECTURE DIAGRAM • 
DEMO**

</div>

<br />

[YouTube walk-through link](https://youtu.be/QLiTN3KWro8)

## 🧐 Project Philosophy

> The aim of this framework is firstly to implement blockchain technology for EHR (Electronic Health Records_ and secondly to provide secure storage of electronic records by defining granular access rules for the users (both patients and doctors) of the proposed framework. Moreover, this framework also discusses the scalability problem faced by the blockchain technology in general via use of off-chain storage of the records. This framework provides the EHR system with the benefits of having a scalable, secure and integral blockchain-based solution.

## 📒 Installation
The projects requires NodeJS and npm to work. Instructions to install all other dependencies are given below.
### Node modules

1. Move to the project directory and open it in your terminal.
2. Run `npm install` to install project dependenccties.

### Ganache

1. Go to [Ganache homepage](https://truffleframework.com/ganache) and download. 
2. If you are on Linux, you must have received an _.appimage_ file. Follow installation instructions available [here.](https://itsfoss.com/use-appimage-linux/)

### IPFS

1. Go to the [github page](https://github.com/ipfs/ipfs-desktop) of IPFS and install IPFS Desktop

### Local server

1. Install Node lite-server by running the following command on your terminal `npm install -g lite-server`

### Metamask

1. Metamask is a browser extension available for Google Chrome, Mozilla Firefox and Brave Browser.
2. Go to the this [link](http://metamask.io/) and add Metamask to your browser.

## 👨‍💻 Tech stack

Here's a brief high-level overview of the tech stack the app uses:

- This project uses the Ethereum Blockchain. Ethereum is a decentralized, open-source blockchain with smart contract functionality.
- HTML, CSS and Bootstrap is used for the UI (User Interface).
- Web3.js is used for the frontend to interact with local ethereum node.
- Solidity is used to code smart contracts. Solidity is an object-oriented programming language for implementing smart contracts on various blockchain platforms, most notably, Ethereum.


## 📒 Configuration
#### 1. Ganache
  - Open Ganache and click on settings in the top right corner.
  - Under **Server** tab:
    - Set Hostname to 127.0.0.1 -lo
    - Set Port Number to 8545
    - Enable Automine
  - Under **Accounts & Keys** tab:
    - Enable Autogenerate HD Mnemonic

#### 2. IPFS
  - Fire up your terminal and run `ipfs init`
  - Then run 
    ```
    ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin "['*']"
    ipfs config --json API.HTTPHeaders.Access-Control-Allow-Credentials "['true']"
    ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods "['PUT', 'POST', 'GET']"
    ```

    > Note: If you face any issues with the above command on windows, try using command prompt and escape sequences or git bash.
#### 3. Metamask
  - After installing Metamask, click on the metamask icon on your browser.
  - Click on __TRY IT NOW__, if there is an announcement saying a new version of Metamask is available.
  - Click on continue and accept all the terms and conditions after reading them.
  - Stop when Metamask asks you to create a new password. We will come back to this after deploying the contract in the next section.
  
### Smart Contract

1. Install Truffle using `npm install truffle -g`
2. Compile Contracts using `truffle compile`

#### 1. Starting your local development blockchain
  - Open Ganache.
  - Make sure to configure it the way mentioned above.
  
1. Open new Terminal and deploy contracts using `truffle migrate`
2. Copy deployed contract address to src/app.js 
![alt text](https://github.com/Divijkatyal0406/MediBuddy/blob/master/images/ganace-contracct.png)

```js
// app/src/app.js  line number 11
var agentContractAddress = '0x75E115394aacC7c6063E593B9292CB9417E4cbeC';
```

3. If you change contents of any contract , replace existing deployment using `truffle migrate --reset`
> Note :  reset of the contract will change the contract Address which needs to be updated in src/app.js

### Running the dApp

#### 1. Connecting Metamask to our local blockchain
  - Connect metamask to localhost:8485
  - Click on import account
  ![alt text](https://github.com/Divijkatyal0406/MediBuddy/blob/master/images/meta-1.png)
  - Select any account from ganache and copy the private key to import account into metaMask
  ![alt text](https://github.com/Divijkatyal0406/MediBuddy/blob/master/images/con-g1.png)

#### 2. Starting IPFS 
  - Start the IPFS Desktop Application
  
#### 3. Start a local server
  - Open a new terminal window and navigate to `/YOUR_PROJECT_DIRECTORY/app/`.
  - Run `npm start`.
  - Open `localhost:3000` on your browser.
  - That's it! The dApp is up and running locally.


## ✍️ Architecture Diagrams
![alt text](https://github.com/Divijkatyal0406/MediBuddy/blob/master/images/dia1.png)
![alt text](https://github.com/Divijkatyal0406/MediBuddy/blob/master/images/dia2.png)

## 🚨 Demo
![alt text](https://github.com/Divijkatyal0406/MediBuddy/blob/master/Demo_ss_MediBuddy/Screenshot%202022-07-08%20122525%20-%20Copy.png)
![alt text](https://github.com/Divijkatyal0406/MediBuddy/blob/master/Demo_ss_MediBuddy/Screenshot%202022-07-08%20122525.png)
![alt text](https://github.com/Divijkatyal0406/MediBuddy/blob/master/Demo_ss_MediBuddy/Screenshot%202022-07-08%20122622.png)
![alt text](https://github.com/Divijkatyal0406/MediBuddy/blob/master/Demo_ss_MediBuddy/Screenshot%202022-07-08%20122703.png)
![alt text](https://github.com/Divijkatyal0406/MediBuddy/blob/master/Demo_ss_MediBuddy/Screenshot%202022-07-08%20122802.png)
![alt text](https://github.com/Divijkatyal0406/MediBuddy/blob/master/Demo_ss_MediBuddy/Screenshot%202022-07-08%20122828.png)
![alt text](https://github.com/Divijkatyal0406/MediBuddy/blob/master/Demo_ss_MediBuddy/Screenshot%202022-07-08%20122851.png)

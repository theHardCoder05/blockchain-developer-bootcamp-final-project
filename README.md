# Final project - Decentralised Cars Renting Platform (D-Rent)

## Deployed version url:

https://thehardcoder05.github.io/blockchain-developer-bootcamp-final-project/

## Steps to run the project:

### Prerequisites

- Node.js 
- Truffle and Ganache
- NPM
- `git checkout master`

### Contracts

- Run `npm install` in project root to install Truffle build and smart contract dependencies
- Run local testnet in port `8545` with an Ethereum client, e.g. Ganache
- `truffle compile` - To build Smart Contracts artifacts
- `truffle migrate --network development`
- `truffle console --network development`
- Run tests in Truffle console: `truffle test`
- `development` network id is 1337, remember to change it in Metamask as well!
- Your local Ganache should be configured as the setting below
 - endpoint: http://127.0.0.1 or http://localhost
 - port: 8545
 - networkid: 1337

### Frontend

- `cd client`
- To install the dependecies - `npm install`
- To build artifacts - `npm run build`
- To run the app - `npm run dev`
- Open `http://localhost:8080`


## Recording

https://drive.google.com/file/d/1B-mevsCnvhG61-DBYzhjdMNEkPvgtbBW/view?usp=sharing


## Public Ethereum wallet for certification:

`0xA7D88AB5987b7837d9C6aE2A07f5df4575a502EB` - For the NFT

## Description

D-Rent is a De-centralised,Low-Cost,Transparent,Trustworthy, and Efficient marketing place to allow drivers to rent a car for their trips. The current version of D-Rent is rather quick and dirty on the UI frontend part, reason was I wanted to focus to make the Smart Contracts(Solidity) right in the first place. The key idea to leverage the beauty of Smart Contracts - "Turing Complete" to act as an Escrow to manage the the booking process. Driver to visits the Dapp website to pick the desired car follow-by filling up the Personal Driving Identify such as the Driving License Id; The renting rate is go by per day basis, as low as 0.001 ether. If you days * 0.001 = total amount. 
The Withdraw will happen when the driver returns back the car to the depot. Agent to perform a thourough check to ensure no traffic rules violation or any car damaage, agent shall re-fund back the 70% of the deposit to the driver. The 30% it will remain in the Smart Contract for the operation costs. 
Certainly, this is definately not the ideal version. There are more services and components to be built for the MVP version such as KYC, ChainLink Intergration, Data Security Compliance features, Cloud Security features, and etc. 


## Workflow
### Booking workflow
1. Navigate to the Application URL
2. MetaMask prompts to user for login
3. Ensure your MetaMask's address(0x0) showing in the Driver's address field approriately.
4. Entering your Personal Information such as Full name and Driving License Id - The Driving Identify Id will be stored as hash value for GDPR compliance. (In the LIVE production version this information should handle by legitimate KYC process).
5. Enter the desire days to rent with the exact deposit amount.
6. Hit "Book Me" button in a few minutes later you shall receive SMS or email regarding the booking confirmation(In phase 3). To inform about collecting the car key.
7. Enjoy your ride!!!!

### Withdraw workflow
1. Agent to withdraw or refund back the Driver if and only if the Driver didn't violate traffic rules or met any accident.
2. The Withdraw amount should be the 70% of the total amount of the deposit; 30% is the renting fee charge. 
3. Greets to the Driver and see you soon!!


## Implementation Plan and Roadmap

1. KYC Process
2. Improve UI Frontend and User experience
3. Oracelisation platform - ChainLink
4. Upgradeble Smart Contracts
5. Multisig function on the Withdraw - Ideally, the withdraw function could potentially have multi-party to sign and withdraw. The scenario would be the car agent, authoritise(Police department), and Insurance company.
6. User Consent
7. Migrate the React for better User experience

## Directory structure

- `client`: Project's React frontend.
- `contracts`: Smart contracts that are deployed in the Ropsten testnet.
- `migrations`: Migration files for deploying contracts in `contracts` directory.
- `test`: Tests for smart contracts.

## Sensitive Information

- .key file - Infura Gateway - Project Id
- .secret - MetaMask Mnemonic key
-  You do not need the key and secret to test on your local!!!

## Sidenotes
- Agent(Owner) is not allowed to book a car.
- No double booking on the same driver. 
- Only the Agent(Owner) can withdraw back the fund to driver.



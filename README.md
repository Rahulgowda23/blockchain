# Ethereum Blockchain-Powered Land Registration Application


![](https://github.com/1209simran/Land-Registry-Application/blob/master/src/images/home.png?raw=true)

## Abstract

Created a revolutionary decentralized application leveraging Blockchain technology to revolutionize the conventional land registry procedures. This innovative solution addresses the inherent limitations of the existing system by introducing a transparent, efficient, and secure way of monitoring property transfers.

Through the power of Blockchain, the intricate process of transferring land ownership becomes seamless, eliminating the need for intermediaries. Buyers, sellers, and government registrars benefit from this streamlined approach, enabling swift and hassle-free property ownership transfers.

What sets this solution apart is its incorporation of essential features such as immutability, auditability, traceability, and anonymity. These cutting-edge attributes captivate individuals worldwide, making them eager to embrace decentralization in the realm of land registry.

Not only does this technology accelerate the registration process, but it also shines a light on transparency within the system, ensuring a brighter, more efficient future for land registry management.

## Technologies Used

- ReactJS
- NodeJS
- MongoDB
- Solidity
- IPFS

## Prerequisites

#### Install Node JS
Refer to https://nodejs.org/en/ to install nodejs.

#### Install Ganache
Refer to https://www.trufflesuite.com/ganache to install Ganache.

#### Install Truffle
Install truffle npm package globally. Use the following command to install truffle
`$ npm install -g truffle`

#### Install Metamask Chrome Extension
Refer to https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=en to download the extension.

#### Make an account on MongoDB Altas
https://www.mongodb.com/cloud/atlas

#### Create an account on Vonage (Previously Nexmo)
https://dashboard.nexmo.com/sign-up

## Getting Started
To set up the project, go along with the following steps:-
- Go to the directory with the repository. <br/>
`$ cd folder_name`
- Run **npm install** (or **yarn install** if you use yarn) to download the npm packages. <br/>
`$ npm install`
- Open Ganache.
- Run **truffle compile** to compile the truffle project. <br/>
`$ truffle compile`
- Run **truffle migrate** to deploy the contracts. <br/>
`$ truffle migrate`
- Run **npm start** to start the project. <br/>
`$ npm start`
- Open another terminal and navigate to the **Server** folder. <br/>
`$ cd Server`
- Run **npm install** (or **yarn install** if you use yarn) to download the npm packages. <br/>
`$ npm install`
- Navigate to the **backend** folder then to the **Config** folder. <br/>
`$ cd backend/Config`
- Change the credentials of **db_config.js** .
- Run the server using this command:- <br/>
`$ npm start`
- Open another terminal and execute the following command to add the government registrar detail to the database. <br/>
`$ curl -X POST http://localhost:3001/register_govt`
- Credentials for government login:- <br/>
Username:- Delhi Government <br/>
Password:- Delhi
- You're all done. Enjoy!

## Workflow
User and Property Registration:

Begin by registering on the platform at http://localhost:3000/signup. Upon clicking the submit button, users will be directed to the login page.
To log in, users must provide their private key.
For property registration, access the "Register Land" tab on the dashboard and complete all property and owner details. After form submission, the government authority verifies the application.

Government Authority Validation:

During the land registration process, users must upload legal land documents for verification by the government and potential buyers. If the application is rejected, users must submit a new one, preventing it from being available to other users. If approved, landowners have the option to list their land for sale.
An exciting feature: Notifications are sent to users via email and SMS as the government approves or rejects requests. NEXMO API and Nodemailer API are utilized for this purpose. This keeps users informed of their application status without needing to repeatedly check their accounts.

Transaction Between Parties:

This step involves multiple stages with no intermediaries or central authority involved in transaction verification. Landowners can only sell their land as a whole; partial transactions are not permitted. The following steps are involved:

Making the Land Available: After government approval, landowners can list their land for sale to other users.
Sending Purchase Requests: Buyers can browse available properties and send purchase requests to landowners.
Viewing Requests: Landowners review purchase requests and decide whether to accept or decline them.
Processing Requests: If the landowner verifies the requester's address, they can approve the request.
Property Purchase: Once approved, buyers can complete the purchase. The property's cost is deducted from the buyer's account and transferred to the landowner's account. Transaction details can be viewed in the user's profile. After a successful transaction, the property is removed from the previous owner's asset list.
The entire process is executed through a smart contract, ensuring immutability, security, and digitization. Data cannot be tampered with, and authenticity is maintained. This eliminates human errors, reduces paperwork, and enhances transparency, minimizing the potential for fraud. The public ledger can be used to resolve disputes over land ownership claims, as digitally signed documents facilitate the transfer of land titles upon cryptocurrency payment.

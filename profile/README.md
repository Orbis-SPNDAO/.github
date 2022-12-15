

# Welcome to SPN DAO


## Problem Statement

Our credit card transaction data reveal a lot about our behaviors. Aggregated together, they tell even more powerful stories about the economy. Is there a spike in Netflix subscriptions? Is there a dip in spending at hardware stores? Credit card transaction data is the highest-grossing data source in the “alternative data” market. The global alternative data market is anticipated to reach 143.31 billion USD by 2030 and is expected to grow at a 54.4% CAGR. North America alone accounted for a revenue share of more than 67.0% in 2021. 

There are more than 400 alternative data providers. Among them are credit card issuers like MasterCard and Visa, institutions like Bloomberg and Goldman Sachs, and numerous analytics firms. These businesses have been monetizing from selling purportedly anonymized and aggregated credit card transaction data and analytics services. The emergence of machine learning and AI have accelerated the growth of these services.

Despite mixed outcomes, hedge funds have spent billions of dollars acquiring such data with the hope to forecast stock performance more accurately. Google spent millions of dollars purchasing data from MasterCard, trying to link online ads to store purchases. 

However, consumers have little control over how and when their personal data, including credit card transaction data, is used. Consumers’ personal data fuels a multi-billion dollar industry while we receive almost no financial rewards. In practice, data from a single person is of little value. And there is no platform where consumers could coordinate and pool their data together. 


## Our Solution

This is exactly why we have created SPN DAO! Our first product release is a dApp that facilitates the creation and operation of a data DAO.

### For consumers/end-users: 

If someone opts in to become a DAO member and to contribute to the data economy, they will be able to upload anonymized credit card transaction data as a .csv file, have it encrypted immediately and store the encrypted data on decentralized storage provided by IPFS.

The user will proceed to mint a soul-bound token (SBT). The token is non-transferable and represents provable membership of the DAO. More importantly, the IPFS CID of the encrypted data is referenced in the metadata of the SBT.

Only a wallet containing the “admin NFT” can decrypt the data. Any existing DAO members have the option to burn their SBTs if they wish to exit the DAO and stop sharing their data. 

### For the admin of the DAO:

The “admin NFT” will be held in a multi-sig wallet. The multi-sig will be jointly managed by delegates elected by DAO members.

When the admin multi-sig connects to the dApp and authenticates ownership of the “admin NFT”, they could unlock the token-gated admin portal. The admin is able to view all the wallet addresses that own the SPN DAO SBT, and initiate decryption of the credit card transaction data tied to a given SBT.

Whenever a decryption is initiated, a payment will be triggered to send rewards to the holder of a given SBT.


## How It's Made

###### Architecture

###### Technologies

- Smart Contracts - Solidity
- Backend - TypeScript
- Testnet - Polygon Mumbai/ FEVM
- Tools - Hardhat, Remix, Metamask
- UX & UI Design - Figma

## Related source code repo

* dApp - https://github.com/SPNDAO/frontend
* Smart Contracts - https://github.com/SPNDAO/core

## Demo URL


##  Future Road Maps

- Integration of Plaid API to source data directly from DAO members. It serves the purpose of KYC as well. 
- We are currently building on-chain voting and decentralized discussion forums that DAO members could access directly from the end user dashboard. 
- Make the metadata of the SBT upgradeable. 
- Time-based NFT passes as subscription, as a revenue stream from third-party clients. 


## Team

* Brian Grosso: Developer
* Jonathan Conn: Developer
* Ram Vittal Kumar: Developer
* Tobias Leinss: Developer
* Karen Sheng: Product Manager
* Yifeng Wang: UX & UI Designer

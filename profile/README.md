
# Welcome to SPN DAO

## Problem Statement

Web 3.0 technologies have enabled a paradigm shift in how we perceive and enforce data privacy and ownership. Data privacy is not equivalent to having everyone’s personal data kept within walled gardens. Instead, consumers should have governance rights and direct control over the use and monetization of their data.

After lots of debates and iterations, our team decided to build a data DAO that incentivizes members to contribute their credit card transaction data and govern how their data is used.

Why credit card transaction data? Platforms such as Instagram heavily influence the formation of consumers’ tastes, preferences, and what we purchase. In return, our credit card transactions reveal a lot about our behaviors. Aggregated together, the data tell even more insightful stories about the economy. For instance, is there a spike in Netflix subscriptions? Or is there a dip in spending at hardware stores?

Credit card transaction data is the highest-grossing data source in the “alternative data” market. The global alternative data market is anticipated to reach 143.31 billion USD by 2030 and is expected to grow at a 54.4% CAGR. North America alone accounted for a revenue share of more than 67.0% in 2021.

There are more than 400 alternative data providers. These businesses have been monetizing from selling purportedly anonymized and aggregated credit card transaction data and analytics services. The emergence of machine learning and AI has accelerated the growth of these services.

Despite mixed outcomes, hedge funds have spent billions of dollars acquiring such data with the hope to forecast stock performance more accurately. Google spent millions of dollars purchasing data from MasterCard, trying to link online ads to store purchases.

However, consumers have little control over how and when our personal data, including credit card transaction data, is used. Consumers’ personal data fuels a multi-billion dollar industry while we receive almost no financial rewards. In practice, data from a single person is of little value. And there is no platform where consumers could coordinate and pool their data together.

## Our Solution

This is why we are inspired to create SPN DAO. We built our POC on the Wallaby testnet of Filecoin’s EVM (FEVM) chain over two days at Hack FEVM in mid-November. Encryption/access control mechanism such as Lit protocols is not supported on FEVM. Therefore, we used Pinata Submarine as a workaround to implement access control for the previous hackathon. The Web3 Social Hackathon gave us an opportunity to rebuild the dApp and build core features from the ground up.

We have built a decentralization application (dApp) that facilitates the creation and operation of a data DAO. The dApp consists of portals for three types of users:

**For end users (prospective and existing DAO members):**

- If someone opts in to become a DAO member and to contribute to the data economy, they will be able to upload anonymized credit card transaction data as a .csv file, have it encrypted immediately and store the encrypted data on decentralized storage provided by IPFS. The IPFS CID is encrypted immediately as well. 

- The user will proceed to mint a soul-bound token (SBT). The token is non-transferable and represents provable membership of the DAO. More importantly, the encrypted IPFS CID is referenced in the metadata of the SBT.

- Only a wallet containing the “admin NFT” can decrypt the CID and the data. Any existing DAO members have the option to burn their SBTs if they wish to exit the DAO and stop sharing their data.

- In the end-user dashboard, DAO members have access to a discussion forum. DAO members could also view and cast votes on any proposals that are active. 

**For the admin of the DAO:**

- The admin could be a core contributor or a delegate that has been approved by community members of the DAO.

- The admin wallet stores the “admin NFT”, which is authorized to unlock the token-gated admin portal and decrypt data. 

- In the “Data Management” dashboard, the admin is able to view all the wallet addresses that own the DAO membership SBT and initiate decryption of the data tied to one or multiple SBTs.

- Whenever a decryption is completed, payment will be sent over to the holder of a given SBT as a reward. The payment transactions can be easily verified on PolygonScan. For example [here](https://mumbai.polygonscan.com/address/0xb66763558e38b596c151954e9b070c46e115c56e#internaltx "here").

- In the “Proposal Management” dashboard, the admin is able to create proposals and set up elections for the proposal. 

**For Subscribers (third-party clients):**

- Subscribers could purchase a 30-day NFT pass as a subscription.

- The NFT unlocks the subscriber’s portal, where the subscriber could view aggregated data or analytics reports that the DAO creates. 

- The subscriber could be an institutional fund, an e-commerce site, an investment club, or even a DAO member who wishes to leverage the data and insights that the community-owned data economy has created.


## Challenges & Future Iterations:

- In general, as we tried to build use cases for multiple bounties, we experienced some difficulties working with tools still in development without a lot of documentation and informal documentation of StackOverflow threads and the like.

- One of the biggest challenges is the reliability of data encryption. We had to deal with the conundrum of the transparency of blockchain and being an open-source project. We realized that there were risks in embedding the decryption key in the membership SBT smart contract. The solution we came up with was to map the key in the admin NFT smart contract.

- Future iterations to enhance the solution include storing the decryption key (“admin NFT”) in a Gnosis multi-sig and enforcing collecting a certain number of approval signatures for decryption; exploring and incorporating a privacy layer such as Aztec.

- Another challenge is to maintain secure storage and retrieval of data while also storing the data in a trustless decentralized manner. For the MVP, the CSV file that a DAO member contributes is automatically downloaded to the admin’s local machine once a member’s SBT is decrypted. This is clearly not appropriate for real-world practice. Future iterations include routing the individual datasets to secure cloud storage; setting up infrastructure for confidential computing; exploring possibilities for compute-over-data.

- Manual data uploads vs. integration of Plaid API in the future. For the MVP, the onboarding process of any prospective DAO members starts with uploading a csv file to IPFS. The data from each user is stored temporarily in a cloud server. After the data is uploaded and encrypted, the data stored on the cloud server is deleted. This manual process requires the end user to remove sensitive PII (personal identifiable information) manually and we have to assume that the data from each user has a standardized schema. The next step post-hackathon is to explore and implement integration with Plaid API. This serves two purposes:
	- Standardizing and automating the funnel of data. 
	- Zero-knowledge KYC and mitigation of Sybil attacks. 


## How It's Made

The tech stack that we’ve used for building the dApp consists of

- NextJS
- Tailwinds
- Vocdoni
- Orbis
- RainbowKit
- Wagmi 
- Lit 
- Figma for design

For the core development, we used:

- Hardhat
- Polygon (Mumbai)
- Pinata as a gateway for IPFS (Submarine)
- IPFS for decentralized storage


## Related source code repo

* dApp - https://github.com/SPNDAO/frontend
* Smart Contracts - https://github.com/SPNDAO/core

## Demo URL

* https://spn-dao.vercel.app/

## Team

* Brian Grosso: Developer
* Jonathan Conn: Developer
* Karen Sheng: Product Lead
* Yifeng Wang: UX & UI Designer
* Tobias Leinss: Developer

# Ethign
Ethign is a multi-party file signature platform built on Ethereum.

## Background
Signature is to authorize. While e-signature has been widely used in our daily life, the e-signature service provider seems fail to proof the certainty and make it easy to verify for the third party. E-signature service providers like [DocuSign](https://www.docusign.net/) and [Esign](https://www.esign.cn/) use centralized trust source, which is fail to provide transparency. <br />
**Transparency is the source of trust.**<br />
We choose to utilize Ethereum smartcontract to provide trust, each contract will be verified by thousands of nodes and we can easily compute the cost to reverse the contract to provide transparency.<br />

## Muldules
* **Website**, platform for this service, interface between users and blockchain, browser to the file.
* **Wallet**, Ethereum identity provider and gas fee payer. *Metamusk(Chrome extension) could be a good choice.*
* **Smartcontract**, multi-party signature data storage and operation. Note there is a privacy issue in this part, users should be able to choose whether the signature beheviour is private and public which means those data store in the smartcontract is encoded or not.  
* **IPFS**(TBD), storage for the contract file itself, if appiled, the contract file alone with the hash of this file are both store in IPFS  and ethereum.
* **ENS**(TBD), UX improvement, to allow people sign files with .eth address.

## 

## Basic operation process
### Sign
1. User sign in, user uses Ethereum wallet like Metamusk and Dapper extension to sign in.
2. Upload file, including image, documents, and set the preview screen.
3. Initiate the smartcontract, define the number of signer and their address.
4. Sign the data and store in the contract.
### Verify
1. User sign in.
2. Search the smartcontract by file hash and display related smartcontract. 
3. Display basic information of the contract, such as time, counter-party, block height, cost to reverse it.

## Related examples
* [Decentraland](https://decentraland.org/)

## Assignment
* Smartcontract
* Wallet interaction, research on wallet functions
* Website front-end
* Storage in IPFS

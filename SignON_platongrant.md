# SignON

## Project Description
SignON is a multi-party privacy-preserving file signature platform powered by Private Contract VM on PlatON.  
**Signature is to authorize.** While e-signature has been widely used in our daily life, the e-signature service provider seems fail to proof the certainty and make it easy to verify for the third party. E-signature service providers like DocuSign and Esign use centralized trust source, which is fail to provide transparency.  
**Transparency is the source of trust, cryptography helps in providing transparency.** More specifically we will create:
- A website platform for users to sign file in the PlatON smart-contract and store in IPFS
- A website platform for the third-party verifier to explor the contract and verify the signature
- A private contract deployed on PlatON which provide data-preserving feature to users and easy to verify by a third-party

### Why PlatON

PlatON offers flexible privacy computation functionality in smart contract, which is essential for SignON, since the data stored in the signature contract need to be relatively confidential for signer's privacy and verifier's accessibility.
As the high users base and volume in financial activity expectation in PlatON, SignON can show the advantages compared to centralized application, such as easily providing services in B2B, B2C and C2C scenario without CA verify and centralized institution cost, providing better UX in signature verification with transparency, instantaneity and no-cost.

### Muldules
- **Website**, platform for service, interface between users, blockchain and IPFS, browser to the file.
- **Wallet**, PlatON identity information provider and gas fee payer, since PlatON has no chrome extension wallet yet, the account authrization action will excute in Samurai.
- **Smartcontract**, multi-party signature data storage and operation. Note there is a privacy issue in this part, users should be able to choose whether the signature beheviour is private and public which means those data store in the smartcontract is encoded or not. Using MPC features in the PCVM, we shall add more sensitive information as input in the compution.
- **IPFS**, storage for the contract file itself, if appiled, the contract file alone with the hash(file address) of this file are both store in IPFS and PlatON.

### Open Source
This is an open source project under GNU LGPL v3. All the defined milestones will be available to the open source community.

## Team members
* Potter Li: Project Manager, president of Blockchain@USC
* Boyuan X.: Tech Lead, TA (Blockchain) at USC Viterbi School of Engineering
* Adam Hamden: Developer, co-president of Blockchain@USC
* Can Toraman: Developer, computer vision engineer of AUV
* Xin: Developer, former blockchain engineer at Strata

## Development Roadmap
- M1 - 1 week: Release the Architecture draft
![Image text](https://github.com/devrevyanx/Ethign/blob/master/Architecture%20draft.jpg)
- M2 - 3 weeks: A Minimum Viable Product on PlatON testnet
  - Two-party file signature smart contract design
  - Identity interact via wallet and explorar
  - Store file on IPFS from NodeJS website
  - Documentations:
    - Guide: How to sign file in SignON
    - Design Doc: Privacy explaination in private contract
- M3 - 4 weeks: Functionality
  - Documentations:
    - Guide: How to sign file in SignON between multi-party
    - Guide: How to verify signature and check the origin file
  - Users should be able to follow the guide to test full functionality of this application.
    - Design model for signature reversion cost.
- M4 - 3 weeks: UX improvement
  - nodeJS website optimization in logo, buttons, and digits display
  - Fully working signature interact with smart contract
      - Different data privacy-preserving strategy support
  - Fully working storage in IPFS
  - Fully working signature verification via blockchain browser
  - Finalize the design docs in M1 & M2
All the deliveriables for each milestone will be published in the open source repositories.

# Contract Signing Protocol Using Rejectable Soulbound Tokens

This repository contains the corresponding smart contracts implementation and the corresponding tests for the Two-step Contract Signing Protocol. The protocol paper with a detailed explanation of the protocol approach is available in: 

The Two-step Contract Signing Protocol paper presents an innovative contract signing protocol for two signers that reduces tthe number of steps needed for a fair contract signature to just two: the proposal of the signature and its acceptance. The presented protocol approach is made possible by the use of a special type of token, a rejectable non-fungible token, named RejSBT. 

The current implementation available in this repository is based in the usage of RejSBT smart contracts, which are deffined using the inheritance structure presented in the following graph.

--> Add inheritance graph 


# Cost analysis 
--> Add Cost trends over the past year of the RejSBT smart contract functions and Cost trends over the past year of the RejSBT smart contract deployment graphs.

## Install dependencies and deployment

### Preparations

* Set ``MNEMONIC`` to obtain the deployers private key, in ``.env``
* Set ``COINMARKETCAP_API_KEY`` to a CoinMarketCap API key in ``.env``, to get complete hardhat gas reporter report.
* Set ``POLYGONSCAN_API_KEY``to the Polygonscan API key in ``.env``, to get complete hardhat gas reporter report.
* Set ``INFURA_API_KEY`` to the Infura API key in ``.env``.

### Install dependencies

Run:
``yarn install`` or ``npm install``

Compile contracts:
``yarn compile`` or ``npm run compile``

Run protocol unit tests:
``yarn test:contractSigningRejSBT`` or ``npm run test:contractSigningRejSBT``

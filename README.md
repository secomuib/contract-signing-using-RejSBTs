# Contract Signing Protocol Using Rejectable Soulbound Tokens

This repository contains the corresponding smart contracts implementation for the contract signing protocol using rejectable soulbound tokens.

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

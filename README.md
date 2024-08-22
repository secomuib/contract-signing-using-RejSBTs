# Contract Signing Protocol Using Rejectable Soulbound Tokens

This repository contains the corresponding smart contracts implementation and the corresponding tests for the Two-step Contract Signing Protocol. The protocol paper with a detailed explanation of the protocol approach is available in:

The Two-step Contract Signing Protocol paper presents an innovative contract signing protocol for two signers that reduces tthe number of steps needed for a fair contract signature to just two: the proposal of the signature and its acceptance. The presented protocol approach is made possible by the use of a special type of token, a rejectable non-fungible token, named RejSBT.

The current implementation available in this repository is based in the usage of RejSBT smart contracts, which are deffined using the inheritance structure presented in the following graph.

![image](./img/contract%20signing%20inheritance.png)

At the core is the SBT interface, which defines the main functionalities of the SBTs. The RejSBT interface extends from SBT, introducing features for rejection and acceptance. Specifically, incorporating an intermediate stage in the minting process, where ownership is only assigned upon acceptance.

Then the RejectableSBTDeadline extends the functionality by introducing a $deadline$ feature that allows the proposed owner to accept or reject the token before the $deadline$. Finally, the ContractSigningRejSBT implements the requirements for the minting stage of the present protocol. Defining a function to check the current state of a contract signature, considering the defined deadlines and the executed actions.

# Cost analysis

Following are presented two graphs of the cost trends from the past year, illustrating the US Dollar costs associated with the smart contract deployment (first graph), and the costs of executing the various functions of the protocol (second graph).

This representation of the past year's trends provides a general visualization of the protocol's cost efficiency. The two graphs clearly show that the main deployment of the smart contracts generally incurs a cost of less than 0.5 US Dollars. As for the functions that constitute the smart contract, the minting of tokens is known to be the most expensive transaction. However, as depicted in the Smart contract functions costs graph, this cost is generally below 0.05 US Dollars, with all other functions having lower costs.

![image](./img/deployment%20costs%20gas.png)

![image](./img/functions%20costs%20gas.png)

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

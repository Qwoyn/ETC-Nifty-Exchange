![Project Wyvern Logo](https://qwoyn.io/wp-content/uploads/2018/04/qwoyn-512-e1535149864317.png "Project Wyvern Logo")

## ETC Nifty Exchange Ethereum Classic Smart Contracts

[![https://badges.frapsoft.com/os/mit/mit.svg?v=102](https://badges.frapsoft.com/os/mit/mit.svg?v=102)](https://opensource.org/licenses/MIT) [![Build Status](https://travis-ci.org/ProjectWyvern/wyvern-ethereum.svg?branch=master)](https://travis-ci.org/ProjectWyvern/wyvern-ethereum) [![Coverage Status](https://coveralls.io/repos/github/ProjectWyvern/wyvern-ethereum/badge.svg?branch=master)](https://coveralls.io/github/ProjectWyvern/wyvern-ethereum?branch=master)


### Synopsis

*Autonomously governed decentralized digital asset exchange.*

These are the Ethereum smart contracts for the Wyvern Protocol, the Wyvern ERC20 token (WYV), and the Wyvern DAO. For general information on the Wyvern project, please see [the website](https://projectwyvern.com).

### Deployed Contracts

*Please note: correct deployed contract addresses will always be in config.json. If you wish to import this repository directly, please use that file. The addresses in Truffle build output are not necessarily accurate.*

#### Mainnet

##### Latest, by Qwoyn

### Development Information

#### Setup

[Node >= v8](https://nodejs.org/en/) and [Yarn](https://yarnpkg.com/en/) required.

Before any development, install the required NPM dependencies:

```bash
yarn
```

#### Testing

Start Ethereum's testrpc tool to provide a Web3 interface (leave this running):

```bash
yarn testrpc
```

Compile the latest smart contracts:

```bash
yarn compile
```

Run the testsuite against the simulated network:

```bash
yarn test
```

Make sure to lint the Solidity files once you're done:

```bash
yarn lint
```

#### Generating Documentation

Install the dependencies:

```bash
cd doxity
yarn
cd ..
```

Autogenerate documentation from Ethereum Natspec using [Doxity](https://github.com/DigixGlobal/doxity):

```bash
yarn doc
```

Final output will be written to [docs](docs), which will be automatically published on push to GitHub Pages at [docs.projectwyvern.com](https://docs.projectwyvern.com).

#### Misc

Run automated smart contract analysis (requires [Oyente](https://github.com/melonproject/oyente) and [Mythril](https://github.com/ConsenSys/mythril)):

```bash
yarn analyze
```

Flatten contract source (for e.g. Etherscan verification, requires [solidity-flattener](https://github.com/BlockCatIO/solidity-flattener) to be installed):
```bash
yarn flatten
```

#### Contributing

Contributions welcome! Please use GitHub issues for suggestions/concerns - if you prefer to express your intentions in code, feel free to submit a pull request.
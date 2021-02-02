![Project Wyvern Logo](https://media.githubusercontent.com/media/ProjectWyvern/wyvern-branding/master/logo/logo-square-red-transparent-200x200.png?raw=true "Project Wyvern Logo")

## Wyvern Protocol Javascript SDK

[![https://badges.frapsoft.com/os/mit/mit.svg?v=102](https://badges.frapsoft.com/os/mit/mit.svg?v=102)](https://opensource.org/licenses/MIT) [![npm](https://img.shields.io/npm/v/wyvern-js.svg)](https://www.npmjs.com/package/wyvern-js) [![npm](https://img.shields.io/npm/dt/wyvern-js.svg)](https://www.npmjs.com/package/wyvern-js)

### Synopsis

This is the standard Javascript SDK for the Wyvern Protocol. Modeled in part after the excellent [0x.js](https://github.com/0xProject/0x.js).

### Versioning

This project uses [semantic versioning](https://semver.org/).

The major version of this library will always correspond with the major version of the Wyvern Protocol, but there is not necessarily an equivalence between the minor version of this library and the minor version of the Wyvern Protocol.

Currently, the latest version of this library supports Wyvern Protocol v2. v2.1 support will be added as soon as v2.1 is deployed to the Ethereum mainnet.

### Development Information

#### Setup

[Node >= v6.9.1, < 10](https://nodejs.org/en/) and [Yarn](https://yarnpkg.com/en/) required.

Before any development, install the required NPM dependencies:

```bash
nvm install v8.17.0
nvm use v8.17.0
yarn install
yarn run build
```

### Contract Deployment using Remix
1. Go to https://remix.ethereum.org/
2. Create new files on Remix
    - WyvernProxyRegistry.sol
    - WyvernTokenTransferProxy.sol
    - WyvernExchange.sol
3. Copy/Paste contents from this repo to newly created files respectively
3. Select compiler version v0.4.23+commit.124ca40d , Enable 'Auto compile', Enable optimization 200
4. Select the network ( Main Ethereum / Rinkeby ) on Metamask and Select 'Injected Web3' in Remix
5. Provide constructor parameters and click Transact
6. Call grantInitialAuthentication function on WyvernProxyRegistry and pass WyvernExchange address as parameter
7. Add contract address in src/wyvern-ethereum/config.json file
8. Run 'yarn run build'
9. Commit changed files

#### Contributing

Contributions welcome! Please use GitHub issues for suggestions/concerns - if you prefer to express your intentions in code, feel free to submit a pull request.

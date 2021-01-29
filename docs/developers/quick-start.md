## Using SDK

### Adding realdao-js

- npm: `npm install realdao-js`
- yarn: `yarn add realdao-js`
- pure js: [dist/realdao.min.js](https://github.com/realdao-finance/realdao-protocol/tree/main/sdk/dist/realdao.min.js)

### Create RealDAO instance

```js
// In Node.js
// const Web3 = require('web3')
// const RealDAO = require('realdao')

// Create with web3 option.
// You should get Web3 independently and transfer it to RealDAO constuctor as an option.
// RealDAO will use the mainnet provider by default.
const realdao = new RealDAO({ web3: Web3 })

// Create with env option.
const realdao = new RealDAO({
  web3: Web3,
  env: 'mainnet',
})

// Adding a provider option.
const realdao = new RealDAO({
  web3: Web3,
  env: 'testnet',
  provider: '<some provider>',
})
```

### Load

You must call initialize method before using it

```js
// Load  contracts
await realdao.loadRDS()
await realdao.loadController()
await hodes.loadRTokens()
```

### Change provider

```js
realdao.setProvider('<some provider>')
```

### Using

```js
const rds = realdao.rds()
await rds.totalSupply().call()

await realdao
  .rEther()
  .mint()
  .send({ from: '<some account>', value: '<some amount>' })

await realdao.rDOL().borrow('<some amount>')

await realdao.rToken('rDOL').borrow('<some amount>')

await realdao.controller().getAccountLiquidity('<some account>').call()

// get raw web3 contract
const orchestrator = realdao.orchestrator(true)
const events = await orchestrator.getPastEvents({ fromBlock: 'latest' })
console.log(orchestrator.options.address)
```

## Using CLI

### Install

```
npm install -g realdao-cli
```

### Using

```
realdao-cli call --instance RDS --signature totalSupply

realdao-cli send --instance rEther --signature mint --value <some value> --wallet <your private key or mnemonic>

realdao-cli send --target <target contract address> --signature borrow --parameters p1,p2,p3
```

### Using with config

```
realdao-cli --env mainnet call --instance RDS --signature totalSupply

realdao-cli --provider <some provider> call --instance RDS --signature totalSupply

realdao-cli --config <path/to/config> call --instance RDS --signature totalSupply
```

<!-- prettier-ignore -->
!!! note
	If there is a `.realdaorc` file in current directory or root directory, `realdao-cli` will use it as the default config file unless you provide other command line arguments.

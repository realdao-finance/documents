# Orchestrator

Orchestrator contract

## getAddress(string)

Get registered contract address

### Params

|||
|---|---|
|key|The key of the contract|

## getContractConfig(string)

Get registered contract config

### Params

|||
|---|---|
|key|The key of the contract|

## initialize(address[])

Initialize and setup most of the contract in realdao protocol

### Params

|||
|---|---|
|_contracts|Addresses of the main contracts in realdao protocol<br/>       Array layout:<br/>       0. MarketControllerLibrary<br/>       1. MarketController<br/>       2. Distributor<br/>       3. InterestRateModel<br/>       4. PriceOracle<br/>       5. RDS<br/>       6. DOL<br/>       7. Council<br/>       8. ProtocolReporter<br/>|

## registerContract(string,address,uint8,uint8)

Register a contract

### Params

|||
|---|---|
|addr|The address of the contract|
|key|The key of the contract|
|permission|The permission of the contract|
|variability|The variability of the contract|

## registerProxy(string,address,bytes,uint8)

Register a proxied contract

### Params

|||
|---|---|
|impl|The address of the contract implementation|
|initialCall|Initialization calldata|
|key|The key of the contract to be updated|
|permission|The permission to upgrade to the proxy|

### Returns

- proxy address*

---
## upgradeProxy(string,address)

Upgrade contract implementation

### Params

|||
|---|---|
|key|The address of the new Distributor contract|


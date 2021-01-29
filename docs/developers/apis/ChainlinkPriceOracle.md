# ChainlinkPriceOracle

Price oracle implementation based on chainlink

## getUnderlyingPrice(address)

Get the underlying price of a rToken asset

### Params

|||
|---|---|
|rTokenAddr|The rToken to get the underlying price of|

### Returns

- The underlying asset price mantissa (scaled by 1e18)

---
## initialize(address)

Initialize the price oracle

### Params

|||
|---|---|
|_orchestrator|The address of the orchestrator contract|

## setPriceFeedAddress(string,address)

Set the address of the price feed contract

### Params

|||
|---|---|
|addr|The contract address|
|symbol|The anchor asset symbol, e.g. ETH, BTC|


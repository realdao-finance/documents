# ProtocolReporter

ProtocolReporter contract

## getAllRTokenBalances(address)

Query balance info of all the markets for a user

### Params

|||
|---|---|
|account|Address of the queried user|

### Returns

- Array of RTokenBalances object

---
## getMarketInfo(address)

Query the market info by a specific token address

### Params

|||
|---|---|
|rTokenAddr|Address of the money market to query|

### Returns

- MarketInfo object

---
## getRTokenBalances(address,address)

Query balance info for a user

### Params

|||
|---|---|
|account|Address of the queried user|
|rTokenAddr|Address of the money market to query|

### Returns

- RTokenBalances object

---
## getUnderlyingPrice(address)

Get the underlying price of a rToken asset

### Params

|||
|---|---|
|rTokenAddr|The rToken to get the underlying price of|

### Returns

- RTokenUnderlyingPrice object

---
## initialize(address)

Initialize ProtocolReporter contract

### Params

|||
|---|---|
|_orchestrator|The address of the orchestrator contract|


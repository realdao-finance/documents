# Distributor

Distributor contract

!!!note
	Implement the distribution algorithms for the incentive token

## claim(uint32)

Claim rewards from pool

### Params

|||
|---|---|
|id|Id of the pool to claim|

## closeLendingPool(address)

Close a lending pool

### Params

|||
|---|---|
|rToken|The lending market address bound with the pool that will be closed|

## closePool(uint32)

Close a pool by `id`

### Params

|||
|---|---|
|id|Id of the pool to close|

## createExchangingPool(address,uint32,uint256)

Create a new exchanging pool for a LP token with a specific delay before launching

### Params

|||
|---|---|
|delay|The pool can be launched after some delay blocks|
|lpToken|Address of the LP token bound with the new created pool|
|weight|The distribution weight of the pool|

## createLendingPool(address,uint32,uint256)

Create a new lending pool for a money market with a specific delay before launching

### Params

|||
|---|---|
|delay|The pool can be launched after some delay blocks|
|rToken|Address of the money market bound with the new created pool|
|weight|The distribution weight of the pool|

## exitExchangingPool(uint32)

Exit from the exchanging pool

### Params

|||
|---|---|
|id|Id of the pool to exit|

## getAccountRecord(address,uint32)

Get account record of a specific pool for a user

### Params

|||
|---|---|
|account|Address of the account|
|id|Id of the pool to query account record|

### Returns

- AccountRecord object of the user in the specific pool

---
## getAccountRecords(address)

Get account record of all pools for a user

### Params

|||
|---|---|
|account|Address of the user|

### Returns

- Array of AccountRecord of the user

---
## getPool(uint32)

Query a pool by `id`

### Params

|||
|---|---|
|id|Id of the pool to query|

### Returns

- The pool object queried

---
## initialize(address)

Initialize the distributor

### Params

|||
|---|---|
|_orchestrator|The address of the orchestrator contract|

## isPoolActive(address)

Query if a pool is in active state

### Params

|||
|---|---|
|token|The market address of LP token address bound with the pool|

### Returns

- Whether or not the pool active

---
## mintExchangingPool(uint32,uint256)

Lock LP tokens to mint RDS in the exchanging pool

### Params

|||
|---|---|
|amount|The amount of the LP tokens to lock|
|id|Id of the pool to mint|

## openPool(uint32)

Open a pool by `id`

### Params

|||
|---|---|
|id|Id of the pool to open|

## updateLendingPower(address,uint256)

Update the latest lending `power` for the`account`

### Params

|||
|---|---|
|account|Address of the account to be updated|
|power|The new power of the account|


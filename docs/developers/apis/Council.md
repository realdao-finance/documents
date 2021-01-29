# Council

Council governance contract

## cancel(uint256)

Cancel a proposal by `id`

### Params

|||
|---|---|
|id|Id of the proposal to cancel|

## execute(uint256)

Execute a proposal

### Params

|||
|---|---|
|id|Id of the proposal to execute|

## getProposal(uint256)

Query a proposal by `id`

### Params

|||
|---|---|
|id|The id of the proposal to query|

### Returns

- The queried proposal object

---
## initialize(address)

Initialize the council

### Params

|||
|---|---|
|_orchestrator|The address of the orchestrator contract|

## propose(address,uint256,string,bytes,uint256,uint256,string)

Lanuch a proposal

### Params

|||
|---|---|
|delay|Delay of the voting time|
|desc|The description of the proposal|
|params|The params of the transaction|
|signature|The signature of the method that is to be called in the proposal|
|target|The target contract address of the proposal|
|value|Ethers that the proposal will transfer|
|votingPeriod|Duration of the voting stage|

## setExecutionDelay(uint256)

Set executionDelay

### Params

|||
|---|---|
|val|The new value of the executionDelay|

## setMaxMembers(uint256)

Set maxMembers

### Params

|||
|---|---|
|val|The new value of the maxMember|

## startNewTerm(address[])

Start a new term for the council

### Params

|||
|---|---|
|newMembers|Array of address of the new members|

## vote(uint256)

Vote a proposal

### Params

|||
|---|---|
|id|Id of the proposal to vote|


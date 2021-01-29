# RDS

RDS contract (EIP-20 compatible)

!!!note
	Governance and incentive token in realdao protocol

## allowance(address,address)

Get the number of tokens `spender` is approved to spend on behalf of `account`

### Params

|||
|---|---|
|account|The address of the account holding the funds|
|spender|The address of the account spending the funds|

### Returns

- The number of tokens approved

---
## approve(address,uint256)

Approve `spender` to transfer up to `amount` from `src`

!!!note
	This will overwrite the approval amount for `spender` and is subject to issues noted [here](https://eips.ethereum.org/EIPS/eip-20#approve)

### Params

|||
|---|---|
|amount|The number of tokens that are approved (2^256-1 means infinite)|
|spender|The address of the account which may transfer tokens|

### Returns

- Whether or not the approval succeeded

---
## balanceOf(address)

Get the number of tokens held by the `account`

### Params

|||
|---|---|
|account|The address of the account to get the balance of|

### Returns

- The number of tokens held

---
## burn(address,uint256)

Burn `amount` tokens for 'src'

### Params

|||
|---|---|
|amount|The number of tokens to burn|
|src|The address to burn tokens|

## delegate(address)

Delegate votes from `msg.sender` to `delegatee`

### Params

|||
|---|---|
|delegatee|The address to delegate votes to|

## delegateBySig(address,uint256,uint256,uint8,bytes32,bytes32)

Delegates votes from signatory to `delegatee`

### Params

|||
|---|---|
|delegatee|The address to delegate votes to|
|expiry|The time at which to expire the signature|
|nonce|The contract state required to match the signature|
|r|Half of the ECDSA signature pair|
|s|Half of the ECDSA signature pair|
|v|The recovery byte of the signature|

## getCurrentVotes(address)

Gets the current votes balance for `account`

### Params

|||
|---|---|
|account|The address to get votes balance|

### Returns

- The number of current votes for `account`

---
## getPriorVotes(address,uint256)

Determine the prior number of votes for an account as of a block number

!!!note
	Block number must be a finalized block or else this function will revert to prevent misinformation.

### Params

|||
|---|---|
|account|The address of the account to check|
|blockNumber|The block number to get the vote balance at|

### Returns

- The number of votes the account had as of the given block

---
## initialize(address)

Initialize the DOL contract

### Params

|||
|---|---|
|_orchestrator|The address of the orchestrator contract|

## mint(address,uint256)

Mint `amount` tokens for 'src'

### Params

|||
|---|---|
|amount|The number of tokens to mint|
|src|The address to receive the mint tokens|

## setSuperior(address)

Set superior address

### Params

|||
|---|---|
|_superior|The address of the superior contract|

## transfer(address,uint256)

Transfer `amount` tokens from `msg.sender` to `dst`

### Params

|||
|---|---|
|amount|The number of tokens to transfer|
|dst|The address of the destination account|

### Returns

- Whether or not the transfer succeeded

---
## transferFrom(address,address,uint256)

Transfer `amount` tokens from `src` to `dst`

### Params

|||
|---|---|
|amount|The number of tokens to transfer|
|dst|The address of the destination account|
|src|The address of the source account|

### Returns

- Whether or not the transfer succeeded

---

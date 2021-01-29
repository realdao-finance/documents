# DOL

DOL stablecoin contract (EIP-20 compatible)

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

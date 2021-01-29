# REther

## allowance(address,address)

Get the current allowance from `owner` for `spender`

### Params

|||
|---|---|
|owner|The address of the account which owns the tokens to be spent|
|spender|The address of the account which may transfer tokens|

### Returns

- The number of tokens allowed to be spent (-1 means infinite)

---
## approve(address,uint256)

Approve `spender` to transfer up to `amount` from `src`

!!!note
	This will overwrite the approval amount for `spender` and is subject to issues noted [here](https://eips.ethereum.org/EIPS/eip-20#approve)

### Params

|||
|---|---|
|amount|The number of tokens that are approved (-1 means infinite)|
|spender|The address of the account which may transfer tokens|

### Returns

- Whether or not the approval succeeded

---
## balanceOf(address)

Get the token balance of the `owner`

### Params

|||
|---|---|
|owner|The address of the account to query|

### Returns

- The number of tokens owned by `owner`

---
## balanceOfUnderlying(address)

Get the underlying balance of the `owner`

### Params

|||
|---|---|
|owner|The address of the account to query|

### Returns

- The amount of underlying owned by `owner`

---
## borrow(uint256)

Sender borrows assets from the protocol to their own address

### Params

|||
|---|---|
|borrowAmount|The amount of the underlying asset to borrow|

## getAccountSnapshot(address)

Get a snapshot of the account's balances, and the cached exchange rate

!!!note
	This is used by controller to more efficiently perform liquidity checks.

### Params

|||
|---|---|
|account|Address of the account to snapshot|

### Returns

- (token balance, borrow balance, exchange rate mantissa)

---
## initialize(address,string,string,string,address[])

Initialize the money market

### Params

|||
|---|---|
|_anchor|Anchor symbol of this token|
|_name|EIP-20 name of this token|
|_orchestrator|The address of the MarketController|
|_parts|Code fragments of  RToken|
|_symbol|EIP-20 symbol of this token|

## liquidateBorrow(address,address)

The sender liquidates the borrowers collateral. The collateral seized is transferred to the liquidator.

!!!note
	Reverts upon any failure

### Params

|||
|---|---|
|borrower|The borrower of this rToken to be liquidated|
|rTokenCollateral|The market in which to seize collateral from the borrower|

## mint()

Sender supplies assets into the market and receives rTokens in exchange

!!!note
	Reverts upon any failure

## redeem(uint256)

Sender redeems rTokens in exchange for the underlying asset

!!!note
	Accrues interest whether or not the operation succeeds, unless reverted

### Params

|||
|---|---|
|redeemTokens|The number of rTokens to redeem into underlying|

## repayBorrow()

Sender repays their own borrow

!!!note
	Reverts upon any failure

## repayBorrowBehalf(address)

Sender repays a borrow belonging to borrower

!!!note
	Reverts upon any failure

### Params

|||
|---|---|
|borrower|the account with the debt being payed off|

## seize(address,address,uint256)

Transfers collateral tokens (this market) to the liquidator.

!!!note
	Will fail unless called by another rToken during the process of liquidation. Its absolutely critical to use msg.sender as the borrowed rToken and not a parameter.

### Params

|||
|---|---|
|borrower|The account having collateral seized|
|liquidator|The account receiving seized collateral|
|seizeTokens|The number of rTokens to seize|

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

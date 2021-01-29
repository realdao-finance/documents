# MarketController

RealDAO' MarketController Contract

## borrowAllowed(address,address,uint256)

Checks if the account should be allowed to borrow the underlying asset of the given market

### Params

|||
|---|---|
|borrowAmount|The amount of underlying the account would borrow|
|borrower|The account which would borrow the asset|
|rToken|The market to verify the borrow against|

### Returns

- 0 if the borrow is allowed, otherwise a semi-opaque error code

---
## getAssetsIn(address)

Returns the assets an account has entered

### Params

|||
|---|---|
|account|The address of the account to pull assets for|

### Returns

- A dynamic list with the assets the account has entered

---
## liquidateBorrowAllowed(address,address,address,address,uint256)

Checks if the liquidation should be allowed to occur

### Params

|||
|---|---|
|borrower|The address of the borrower|
|liquidator|The address repaying the borrow and seizing the collateral|
|rTokenBorrowed|Asset which was borrowed by the borrower|
|rTokenCollateral|Asset which was used as collateral and will be seized|
|repayAmount|The amount of underlying being repaid|

## liquidateCalculateSeizeTokens(address,address,uint256)

Calculate number of tokens of collateral asset to seize given an underlying amount

!!!note
	Used in liquidation (called in rToken.liquidateBorrowFresh)

### Params

|||
|---|---|
|actualRepayAmount|The amount of rTokenBorrowed underlying to convert into rTokenCollateral tokens|
|rTokenBorrowed|The address of the borrowed rToken|
|rTokenCollateral|The address of the collateral rToken|

### Returns

- ( number of rTokenCollateral tokens to be seized in a liquidation)

---
## mintAllowed(address,address,uint256)

Checks if the account should be allowed to mint tokens in the given market

### Params

|||
|---|---|
|mintAmount|The amount of underlying being supplied to the market in exchange for tokens|
|minter|The account which would get the minted tokens|
|rToken|The market to verify the mint against|

### Returns

- 0 if the mint is allowed, otherwise a semi-opaque error code

---
## redeemAllowed(address,address,uint256)

Checks if the account should be allowed to redeem tokens in the given market

### Params

|||
|---|---|
|rToken|The market to verify the redeem against|
|redeemTokens|The number of rTokens to exchange for the underlying asset in the market|
|redeemer|The account which would redeem the tokens|

### Returns

- 0 if the redeem is allowed, otherwise a semi-opaque error code

---
## repayBorrowAllowed(address,address,address,uint256)

Checks if the account should be allowed to repay a borrow in the given market

### Params

|||
|---|---|
|borrower|The account which would borrowed the asset|
|payer|The account which would repay the asset|
|rToken|The market to verify the repay against|
|repayAmount|The amount of the underlying asset the account would repay|

### Returns

- 0 if the repay is allowed, otherwise a semi-opaque error code

---
## seizeAllowed(address,address,address,address,uint256)

Checks if the seizing of assets should be allowed to occur

### Params

|||
|---|---|
|borrower|The address of the borrower|
|liquidator|The address repaying the borrow and seizing the collateral|
|rTokenBorrowed|Asset which was borrowed by the borrower|
|rTokenCollateral|Asset which was used as collateral and will be seized|
|seizeTokens|The number of collateral tokens to seize|

## setCloseFactor(uint256)

Sets the closeFactor used when liquidating borrows

!!!note
	Admin function to set closeFactor

### Params

|||
|---|---|
|newCloseFactorMantissa|New close factor, scaled by 1e18|

## setCollateralFactor(address,uint256)

Sets the collateralFactor for a market

!!!note
	Admin function to set per-market collateralFactor

### Params

|||
|---|---|
|newCollateralFactorMantissa|The new collateral factor, scaled by 1e18|
|rToken|The market to set the factor on|

## setLiquidationIncentive(uint256)

Sets liquidationIncentive

!!!note
	Admin function to set liquidationIncentive

### Params

|||
|---|---|
|newLiquidationIncentiveMantissa|New liquidationIncentive scaled by 1e18|

## setMaxAssets(uint256)

Sets maxAssets which controls how many markets can be entered

!!!note
	Admin function to set maxAssets

### Params

|||
|---|---|
|newMaxAssets|New max assets|

## supportMarket(address)

Add the market to the markets mapping and set it as listed

!!!note
	Admin function to set Listed and add support for the market

### Params

|||
|---|---|
|rToken|The address of the market (token) to list|

## transferAllowed(address,address,address,uint256)

Checks if the account should be allowed to transfer tokens in the given market

### Params

|||
|---|---|
|dst|The account which receives the tokens|
|rToken|The market to verify the transfer against|
|src|The account which sources the tokens|
|transferTokens|The number of rTokens to transfer|

### Returns

- 0 if the transfer is allowed, otherwise a semi-opaque error code

---

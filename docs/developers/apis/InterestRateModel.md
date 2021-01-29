# InterestRateModel

RealDAO' InterestRateModel

!!!note
	Enabling updateable parameters.

## getBorrowRate(uint256,uint256,uint256)

Calculates the current borrow rate per block, with the error code expected by the market

### Params

|||
|---|---|
|borrows|The amount of borrows in the market|
|cash|The amount of cash in the market|
|reserves|The amount of reserves in the market|

### Returns

- The borrow rate percentage per block as a mantissa (scaled by 1e18)

---
## getSupplyRate(uint256,uint256,uint256,uint256)

Calculates the current supply rate per block

### Params

|||
|---|---|
|borrows|The amount of borrows in the market|
|cash|The amount of cash in the market|
|reserveFactorMantissa|The current reserve factor for the market|
|reserves|The amount of reserves in the market|

### Returns

- The supply rate percentage per block as a mantissa (scaled by 1e18)

---
## initialize(address)

Construct an interest rate model

### Params

|||
|---|---|
|_orchestrator|The address of the Orchestrator|

## updateModel(uint256,uint256,uint256,uint256)

Update the parameters of the interest rate model (only callable by admin, i.e. Timelock)

### Params

|||
|---|---|
|_kink|The utilization point at which the jump multiplier is applied|
|baseRatePerYear|The approximate target base APR, as a mantissa (scaled by 1e18)|
|jumpMultiplierPerYear|The multiplierPerBlock after hitting a specified utilization point|
|multiplierPerYear|The rate of increase in interest rate wrt utilization (scaled by 1e18)|

## utilizationRate(uint256,uint256,uint256)

Calculates the utilization rate of the market: `borrows / (cash + borrows - reserves)`

### Params

|||
|---|---|
|borrows|The amount of borrows in the market|
|cash|The amount of cash in the market|
|reserves|The amount of reserves in the market (currently unused)|

### Returns

- The utilization rate as a mantissa between [0, 1e18]

---

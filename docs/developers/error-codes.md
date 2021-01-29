## Structure

Example:

<font color=red>13</font><font color=green>04</font>020

- The left two digits (red color) represent the function domain the error occured
- THe middle digits represent the error type
- The right three digits represent the error detail

## Error domains

| Code | Domain            |
| ---- | ----------------- |
| 10   | Unknow            |
| 11   | RToken            |
| 12   | MarketController  |
| 13   | Distributor       |
| 14   | Oracle            |
| 15   | InterestRateModel |
| 16   | Council           |
| 17   | Democracy         |
| 18   | Orchestrator      |

## Error Type

| Code | Type                   |
| ---- | ---------------------- |
| 1    | Parameter Error        |
| 2    | Math Error             |
| 3    | Auth Error             |
| 4    | Business Error         |
| 5    | Unexpected Error       |
| 6    | Environment Error      |
| 7    | External Service Error |

## Error Detail

### RToken

|     | Code                                                    | Message |
| --- | ------------------------------------------------------- | ------- |
| 1   | Invalid length of RToken contract parts                 |
| 2   | Math error while querying account snapshot              |
| 3   | Math error while calculating borrower principal         |
| 4   | Math error while calculating borrowed amount            |
| 5   | Borrow rate is absurdly high                            |
| 6   | Could not calculate block delta                         |
| 8   | Math error while calculating accure interest            |
| 9   | Math error while calculating exchanging rate            |
| 10  | Math error while calculating total cash                 |
| 11  | Ether sender mismatch                                   |
| 12  | Ether value mismatch                                    |
| 13  | Failed to transfer in Erc20 token                       |
| 14  | Calculation overflowed while transfering in Erc20 token |
| 15  | Failed to transfer out Erc20 token                      |
| 16  | Controller rejected while seizing collateral assets     |
| 17  | Failed to check accrual block number                    |
| 18  | Math error in minting calculation                       |
| 19  | Invalid redeem parameters                               |
| 20  | Math error in redeeming calculation                     |
| 21  | Insufficient cash                                       |
| 22  | Math error in borrowing calculation                     |
| 23  | Transfer source address equals to the target            |
| 24  | Math error in transferring calculation                  |
| 25  | Only controller is allowed                              |
| 26  | Math error in system supplying calculation              |
| 27  | Math error in system reducing calculation               |
| 28  | Math error while adding reserves                        |
| 29  | Math error while reducing reserves                      |
| 30  | Insufficient reserves                                   |
| 31  | Math error while seizing collateral assets              |
| 32  | Liquidator is borrower                                  |
| 33  | Math error while repaying                               |
| 34  | Liquidating too much                                    |
| 35  | Liquidating amount is max uint                          |
| 36  | Liquidating amount is zero                              |
| 37  | Math error while calculating balance of underlying      |
| 38  | Allowance is insufficient while transferring            |
| 39  | Balance is insufficient while transferring              |
| 40  | Addition overflow while transferring                    |
| 41  | Redeem too much                                         |
| 42  | Substraction underflow while redeeming                  |
| 43  | Seize too much                                          |
| 44  | Substraction underflow while seizing                    |
| 45  | Repay too much                                          |
| 46  | Substraction underflow while repaying                   |
| 47  | Reduce too much DOL                                     |
| 48  | Substraction underflow while reducing DOL               |

### MarketController

|     | Code                                                            | Message |
| --- | --------------------------------------------------------------- | ------- |
| 1   | Market is not listed                                            |
| 2   | Too many assets                                                 |
| 3   | Insufficient account liquidity while moving asset               |
| 4   | Invalid length of contract implementation parts                 |
| 5   | Market is suspended                                             |
| 6   | Invalid liquidation incentive                                   |
| 7   | Token is already supported                                      |
| 8   | Invalid close factor                                            |
| 9   | Invalid collateral factor                                       |
| 10  | Price queried from oracle is zero                               |
| 11  | Math error in liquidation calculating                           |
| 12  | Math error in account liquidity calculating                     |
| 13  | Account shortfall of borrower is insufficient while liquidating |
| 14  | Math error while calculating max close amount of liquidation    |
| 15  | Repay too much while liquidating                                |
| 16  | Contract implementation parts are already bound                 |
| 17  | Market not found or exist                                       |
| 18  | Market is not in closing state                                  |
| 19  | Market is not in liquidating state                              |
| 20  | Market state is none                                            |

### Distributor

|     | Code                                                    | Message |
| --- | ------------------------------------------------------- | ------- |
| 1   | Market is not listed                                    |
| 2   | Pool id out of range                                    |
| 3   | Pool not created                                        |
| 4   | Unexpected pool id                                      |
| 5   | Pool is closed                                          |
| 6   | Mint amount is zero                                     |
| 7   | Pool not started                                        |
| 8   | StartBlock too small                                    |
| 9   | Pool for the market already created                     |
| 10  | Pool already started                                    |
| 11  | Failed to transfer in Erc20 tokens                      |
| 12  | Calculation overflowed while transfering in Erc20 token |
| 13  | Failed to transfer out Erc20 tokens                     |
| 14  | Pool launching time is not up                           |
| 15  | Math error while calculating total power                |
| 16  | Math error while calculating accmulated power           |
| 17  | New power is overflow while updating power              |
| 18  | Pool is not active while closing it                     |
| 19  | Only market controller is allowed                       |
| 20  | Permission denied to close the pool directly            |

### ChainlinkPricePracle

|     | Code                          | Message |
| --- | ----------------------------- | ------- |
| 1   | Underlying decimals too big   |
| 2   | Only supported in dev network |

### InterestRateModel

|     | Code | Message |
| --- | ---- | ------- |

### Council

|     | Code                                         | Message |
| --- | -------------------------------------------- | ------- |
| 1   | Permission only for council member           |
| 2   | Invalid voting delay                         |
| 3   | Invalid voting period                        |
| 4   | Proposal not exist                           |
| 5   | Voting time not up                           |
| 6   | Proposal already voted                       |
| 7   | Invalid member count while starting new term |
| 8   | Failed to execute proposal                   |
| 9   | The executing proposal is not queued         |
| 10  | Proposal hasn't surpassed time lock          |
| 11  | Proposal is stale                            |
| 12  | Invalid max member set                       |
| 13  | Invalid execution delay set                  |
| 14  | Proposal is not in voting state              |

### Democracy

|     | Code | Message |
| --- | ---- | ------- |

### Orcestrator

|     | Code                                                            | Message |
| --- | --------------------------------------------------------------- | ------- |
| 1   | Invalid contract number while initializing                      |
| 2   | Only guardian is allowed                                        |
| 3   | Only council is allowed to set democracy address                |
| 4   | Only democracy is allowed to change democracy address           |
| 5   | Proxy contract already created                                  |
| 6   | Proxy not created while updating implementation                 |
| 7   | Democracy is not set while abdicating guardian                  |
| 8   | Distributor is final while upgrading distributor implementation |

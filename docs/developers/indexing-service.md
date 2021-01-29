## Run

```
git clone https://github.com/realdao-finance/realdao-protocol

cd realdao-protocols/tools/liquidating-assistant

npm install

# modify orchestrator field of  .env.js in the root dir

node index.js
```

## API

### GET /potential_liquidations

Get the accounts which are likely to be liquidated

#### Query

| Field  | Type   | Description                                      | Required | Default |
| ------ | ------ | ------------------------------------------------ | -------- | ------- |
| offset | Number | How many records will be skipped in the response | false    | 0       |
| limit  | Number | Number of records to include in the response     | false    | 25      |

Example:

```
curl https://api.realdao.finance/potential_liquidations?offset=50&limit=25
```

#### Response

| Field       | Type   | Description                                       |
| ----------- | ------ | ------------------------------------------------- |
| account     | String | Address of the account                            |
| liquidity   | Number | Normalized literal value of the account liquidity |
| collaterals | Object | Collateral assets of the account                  |
| borrows     | Object | Borrowed assets of the account                    |

Example:

```js
{
  "account": "0xB4bb59B8cE6DDcd7cCCBCc6134E58Aaf4fF2213A",
  "liquidity": 1150,
  "collaterals": {
      "rEther": 10.5,
      "rDOL": 0,
  },
  "borrows": {
      "rEther": 0,
      "rDOL": 2000,
  }
}
```

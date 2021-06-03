# Vesper API documentation

## Endpoints

[`[GET] /dashboard`](https://api.vesper.finance/dashboard)

Gets additional information such as contracts, strategies and pool rewards from all pools.
Returns an array with the requested data:
- `name`(`string`): the name of the pool
- `contract` (`object`): pool contract information.
  - `address` (`string`): pool contract address.
  - `tokens`: (`object[]`): list of tokens from the contract.
  - `holders` (`number`): number of holders from the pool.
- `strategies` (`object[]`): list of pool strategies information such as address, tokens, pool rewards, status and stage.
  - `address` (`string`): pool strategy address.
  - `tokens`: (`object[]`): list of tokens information from strategy.
  - `makerVaultInfo` (`object | undefined`): information on the MakerDAO Vault as applicable.
- `strategy` (`object`): [Deprecated] pool strategy information such as address, tokens, pool rewards, status and stage.
  - `address` (`string`): pool strategy address.
  - `tokens`: (`object[]`): list of tokens information from strategy.
  - `makerVaultInfo` (`object | undefined`): information on the MakerDAO Vault as applicable.
- `poolRewards` (`object`): pool rewards information.
  - `address` (`string`): pool rewards address.
  - `tokens` (`object[]`) list of pool tokens
- `status` (`string`): pool status. It can be "operative", "paused".
- `stage` (`string`): stage the pool is currently on. It can be "alpha", "beta", "prod" or "retired".

Example:
```js
[{
    name: "vLINK",
    contract: {
        address: "0x0a27E910Aee974D05000e05eab8a4b8Ebd93D40C",
        tokens: [
            {
                address: "0x514910771af9ca656af840dff83e8264ecf986ca",
                balance: "3563537237796219000000000",
                decimals: "18",
                symbol: "LINK"
            }
        ],
        holders: 239
    },
    strategies: [
      {
        address: "0x59543A595B69897b295F12964d3C7C37B3AD29C0",
        tokens: [
          {
            address: "0x6b175474e89094c44da98b954eedeac495271d0f",
            balance: "10141625",
            decimals: "18",
            symbol: "DAI"
          },
          {
            address: "0xca0c34a3f35520b9490c1d58b35a19ab64014d80",
            balance: "825661980228538300000",
            decimals: "18",
            symbol: "vDAI"
          }
        ],
        makerVaultInfo: {
          collateralRatio: "0",
          daiDebt: "0",
          highWater: "3000000000000000000",
          isUnderwater: false,
          lowWater: "2750000000000000000",
          vaultNum: "23254"
        }
      }
    ],
    strategy: {
        address: "0x59543A595B69897b295F12964d3C7C37B3AD29C0",
        tokens: [
            {
                address: "0x6b175474e89094c44da98b954eedeac495271d0f",
                balance: "10141625",
                decimals: "18",
                symbol: "DAI"
            },
            {
                address: "0xca0c34a3f35520b9490c1d58b35a19ab64014d80",
                balance: "825661980228538300000",
                decimals: "18",
                symbol: "vDAI"
            }
        ],
        makerVaultInfo: {
            collateralRatio: "0",
            daiDebt: "0",
            highWater: "3000000000000000000",
            isUnderwater: false,
            lowWater: "2750000000000000000",
            vaultNum: "23254"
        }
    },
    poolRewards: {
        address: "0xcA9AEeB14ff396F8661F7DF3128f88c31D2fDEC5",
        tokens: [
            {
                address: "0x1b40183efb4dd766f11bda7a7c3ad8982e998421",
                balance: "4643799953696691000000",
                decimals: "18",
                symbol: "VSP"
            }
        ]
    },
    status: "operative",
    stage: "prod"
}]
```

[`[GET] /loan-rates`](https://api.vesper.finance/loan-rates)

Gets the APY, APR and token symbol from all pools.
Returns an object with the key `lendRates` that contains an array with the requested data from each pool.
- `apy` (`number`): annual percentage yield calculated over the last 24h.
- `apr` (`number`): annual percentage rate calculated over the last 24h.
- `tokenSymbol` (`string`): token symbol.

Example:
```js
{
    lendRates: [
        {
            apy: 0.0415,
            apr: 0.0407,
            tokenSymbol: "DAI"
        },
        {
            apy: 0.0057,
            apr: 0.0057,
            tokenSymbol: "ETH"
        },
        {
            apy: 0.0024,
            apr: 0.0024,
            tokenSymbol: "LINK"
        },
        {
            apy: 0.0196,
            apr: 0.0194,
            tokenSymbol: "USDC"
        },
        {
            apy: 12.9642,
            apr: 2.646,
            tokenSymbol: "VSP"
        },
        {
            apy: 0.0143,
            apr: 0.0142,
            tokenSymbol: "WBTC"
        }
    ]
}
```

[`[GET] /pools`](https://api.vesper.finance/pools)

Gets detailed information from all pools.
Returns an array with the requested data.
- `name` (`string`): name of the pool.
- `address` (`string`): address of the pool.
- `asset` (`object`): asset compounding the pool.
  - `address` (`string`): asset address.
  - `decimals` (`string`): pool asset decimals quantity.
  - `symbol` (`string`): asset symbol.
  - `currency` (`string`): asset currency.
  - `price` (`number`): asset price.
- `birthblock` (`number`): the block at which the pool contract was created.
- `chainId` (`number`): the id of the chain where the contract was deployed.
- `riskLevel` (`number`): shows the risk level of the pool. More than 3 is considered aggressive, 3 or less is conservative.
- `stage` (`string`): stage the pool is currently on. It can be "alpha", "beta", "prod" or "retired".
- `collRewardsRate` (`string`): collateral rewards rate.
- `decimals` (`string`): pool decimals quantity.
- `interestEarned` (`string`): interest earned from the pool.
- `interestFee` (`number`): interest fee that it is charged. It is set to 15% for every pool except vVSP which is 0.
- `lockPeriod` (`number`): time (expresed in seconds) where the user can't do a withdraw. It is set to 0 for every pool except for vVSP which is 24 hours (86400 seconds).
- `status` (`string`): pool status. It can be "operative", "paused".
- `tokenValue` (`string`): pool token value.
- `totalSupply` (`string`): pool total supply.
- `totalValue` (`string`): pool total value.
- `vspRewards` (`boolean`): flag used to know if pool gives rewards.
- `vspRewardsRate` (`string`): VSP rewards rate.
- `withdrawFee` (`number`): withdraw fee charged. It is set to 0.60% for every pool except vVSP which is 0.
- `color` (`string`): color (in hex) used to represent a pool, for example in a chart.
- `holders` (`number`): number of holders from a pool.
- `isRetiring` (`boolean`): flag used to know if a pool is in the process of retiring.
- `actualRates` (`object`): pool actual rates from 1, 2, 7 and 30 days.
- `earningRates` (`object`): pool earning rates from 1, 2, 7 and 30 days.
- `vspDeltaRates` (`object`): VSP delta rates from 1, 2, 7 and 30 days.

Example:
```js
[{
    name: "vDAI",
    address: "0xcA0c34A3F35520B9490C1d58b35A19AB64014D80",
    asset: {
        address: "0x6B175474E89094C44Da98b954EedeAC495271d0F",
        decimals: "18",
        symbol: "DAI",
        currency: "USD",
        price: 1.0006
    },
    birthblock: 11594191,
    chainId: 1,
    riskLevel: 3,
    stage: "prod",
    collRewardsRate: "0",
    decimals: "18",
    interestEarned: "0",
    interestFee: 0.15,
    lockPeriod: 0,
    status: "operative",
    tokenValue: "1031290356976276280",
    totalSupply: "257324418187703220979612",
    totalValue: "265376191091509055419337",
    vspRewards: false,
    vspRewardsRate: "0",
    withdrawFee: 0.006,
    color: "#c7c3e8",
    holders: 90,
    isRetiring: false,
    actualRates: {
        1: 4.15,
        2: 4.46,
        7: 4.62,
        30: 6.88
    },
    earningRates: {
        1: 4.15,
        2: 4.46,
        7: 4.62,
        30: 6.88
    },
    vspDeltaRates: {
        1: 0,
        2: 0,
        7: 0,
        30: 0
    }
}]
```

`[GET] /pools/:address/data-points`

Gets data points such as values, supplies, interest and interest fee from the specified pool within the last week.
Returns an array with the requested data.
- `number` (`number`): the block number where the values were taking from.
- `interest` (`string`): interest given from the specified pool.
- `interestFee` (`number`): interest fee that it's charged. It is set to 15% for every pool except vVSP which is 0.
- `supply` (`string`): pool supply from which the data point is from.
- `timestamp` (`number`): date and time (in seconds) from which the data point is from.
- `value` (`string`): pool value from which the data point is from.

Example:
```js
[{
    number: 12477605,
    interest: "503509373321162311",
    interestFee: 0.15,
    supply: "126482280705011577917580",
    timestamp: 1621599093,
    value: "1003979119015679467"
}]
```

[`[GET] /values-locked`](https://api.vesper.finance/values-locked)

Gets deposits asset values from all pools within the last month.
Returns an array with the requested data.
- `_id` (`string`): random ID.
- `number` (`number`): the block number where the values were taking from.
- `timestamp` (`number`): date and time (in seconds) in which the data comes from.
- `valuesLocked` (`object`): list of pools by address
  - `{{poolAddress}}` (`string`): total value locked from the pool within the `timestamp`

Example:
```js
[{
    _id: "60897a1d03dc1669cf6beec6",
    number: 12329593,
    timestamp: 1619621673,
    valuesLocked: {
        0x0a27E910Aee974D05000e05eab8a4b8Ebd93D40C: "145249765884",
        0xbA4cFE5741b357FA371b506e5db0774aBFeCf8Fc: "76310599903590",
        0xcA0c34A3F35520B9490C1d58b35A19AB64014D80: "340903766941",
        0x0C49066C0808Ee8c673553B7cbd99BCC9ABf113d: "236672858664861",
        0x4B2e76EbBc9f2923d83F5FBDe695D8733db1a17B: "405713119147682",
        0x103cc17C2B1586e5Cd9BaD308690bCd0BBe54D5e: "554270079439720"
    }
}]
```

[`[GET] /vsp-stats`](https://api.vesper.finance/vsp-stats)

Gets information related to the VSP token, such as price, total and circulating supply, market cap and more.
Returns an `object` with the requested data.
- `price` (`number`): last VSP token price.
- `priceChange1h` (`number`): VSP token price change within the last hour.
- `priceDelta1h` (`number`): VSP token price delta change within the last hour.
- `totalSupply` (`string`): VSP token total supply.
- `circulatingSupply` (`string`): VSP token circulating supply.
- `marketCap` (`number`): VSP token market cap.
- `vspDistributed` (`string`): VSP tokens distributed.
- `vspDistributed30d` (`string`): VSP tokens distributed within 30 days.

Example:
```js
{
    price: 17.530217,
    priceChange1h: 0,
    priceDelta1h: -0.136685,
    totalSupply: "10000000000000000000000000",
    circulatingSupply: "3513992153784838601048611",
    marketCap: 61601044.99,
    vspDistributed: "16986395824456057293201", 
    vspDistributed30d: "184549654243772215145896"
}
```

# VIP-17 Emissions Overhaul
Status: Pending

## Summary
Introduce a better scaling Emissions framework and align incentives with long-term minded vVSP holders.

## Abstract
Many more Vesper Pools are launching, and with the rise of Vesper Orbit and expanding multi-chain ambitions, the rate of new pools will likely increase for the foreseeable future. Our current emissions framework assigns weight to all pools, which isn’t a sustainable approach.

VSP boosting serves several purposes:

- Boosting APY
- Attracting (and retaining) TVL
- Incentivizing collaborations

Initially, VSP emissions were a means of broadly distributing the governance token for the ecosystem, but as VSP is now largely circulated, our intentions for emissions should no longer reflect “diversity of holders” and instead emphasize the most efficient and effective usage of our weight.

Additionally, there is opportunity to leverage vVSP ownership as weight in emissions, similarly to how projects like Curve and FRAX offer “gauges” directed by voter signal.

## Expectations
This proposal suggests an emissions restructure that:

1. Provides VSP emissions to the top performing subset of pools
2. Cements a predictable, future-proof budget as more pools and chains are incorporated
3. Encourages participation in new pools

Per VIP-10 there our emissions look like 40,000 for December-January, 35,000 for January-February, then 30,000 VSP for following months for Vesper pools.

Instead of boosting every pool, boost the pools as follows:

#### Ethereum mainnet

- 12,500 split between the top 8 performing pools
-- Scoring determined as highest revenue generating pools (30-day average APY * spot TVL)
-- 2,500 VSP each for top pool (1)
-- 2,000 VSP each for the next 2 pools (2-3)
-- 1,200 VSP each for the next 5 pools (4-8)

#### Other Chains (Polygon, Avalanche, etc.)
Up-to 5,000 VSP budgeted per month to boost top pools on non-Ethereum chains.

#### New Pools and Partners
Up-to 10,000 VSP budgeted per month to boost new pools and partners.
Communities looking to co-boost Vesper pools can receive additional emissions through VSP replenish and partnership earmarks outlined in the new treasury split.

#### Specifications
- VIP-10 Overridden
- VSP emissions assigned from DAO holdings monthly, by performance of pool
- New pools to adopt standardized emissions framework
- Assigned emission targets for other chains

# VIP-18: Fee Structure Overhaul

Summary
-------

Replace the existing fee structure with a single, universal fee. This prevents users from ever earning negative returns.

Abstract
--------

The Vesper revenue framework was built using market data from competitors at the time and analyzing the user psychology of different fee models. As the market has changed substantially since inception, our fee model is now outdated, and seen as inferior to others.

This proposal sunsets the existing model (0.6% withdrawal fee, 20% performance fee) and introduces a universal fee.

The universal fee is straightforward: Vesper will charge a 2% fee on principal, collected from realized earnings on the pool at each rebalance. If that 2% reflects more than 50% of yield earned, Vesper will only take 50% of yield.

In other words, we charge 50% under 4% APY, and 2% of principal at-or-above 4%.

This model was determined by analyzing competitors and modeling APY and revenue to both protocol and end user. 

Expectations
------------

This fee model is also unique from other options in its ease of implementation. The universal fee, while assigned based on principle, does not touch the deposits of user funds, only the yield earned.

The management fee is added to the rebalance logic module, and looks like an additive, dynamic fee on yield earned versus deposits. It works as follows:

Yield Earned is assigned at rebalance. Then...\

Fee = 2% * ( blocks since last rebalance / blocks per year ) * TVL

If (fee > Yield Earned * 50%)

*  Fee = Yield Earned * 50%

User APY = Yield Earned - Fee

Protocol Revenue = Fee

Examples:

| Base APY | End User APY (Vesper) | End User APY (Yearn) |
|-------: |-------: | --------|
| 1% | 0.5% | 0% |
| 2% | 1% | 0% |
| 3% | 1.5% | 0.4% |
| 5% | 3% | 2% |
| 8% | 6% | 4.4% |
| 13% | 11% | 8.4% |
| 21% | 19% | 14.8% |

Specification
-------------

All pools' withdrawal/deposit fees are set to 0%. Rebalance logic modified to account for a universal fee. This fee is set at 2% of management or 50% of performance, whichever is lower.

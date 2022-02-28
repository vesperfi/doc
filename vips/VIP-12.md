# VIP-12: Change Fee Structure, Treasury Management, and Revenue Allocation
Status: Passed

## Summary
Change the withdrawal fee, performance fee, treasury management strategy, and structure for how protocol revenue is allocated. Optimize the fee structure and revenue allocation to improve long term growth in users and TVL. In its current state, the Vesper treasury is just holding VSP, which entails unnecessary risk through lack of diversification.

## Abstract
Raising the yield fees and lowering the cost to transfer between pools incentivizes growing the total returns for Vesper pool users, while still staying in line with competitors’ fees. Implementing an algo-trading strategy for the treasury mitigates risk. Diverting protocol revenue from vVSP rewards lowers short-run returns to stakers, but enables long-run growth.

## Expectations
Currently, withdrawal fees make up 93% of protocol revenue, but are acting as a disincentive for users to move to higher APY pools. Raising the yield fees and lowering the cost to transfer incentivizes growing the total returns for Vesper pool users.

Yield fee: increase from 15% to 20%
Withdrawal fee:
If transferring directly to another Vesper pool: decrease fee from 0.6% to 0.3%. (Starting with transfers of the same token between conservative and aggressive pools).
If withdrawing without transferring to another pool: keep fee at 0.6%
Proposed changes to how fee revenue is allocated:

Operations and Marketing: 25%
Developer: 5%
Partner Program: 5%
Replenishing VSP Reserves: 10%→25% (gradual transition)
Rewards: 55%→40% (gradual transition)

New Initiatives:
Operations and Marketing: this allocation is set to cover a projected $4 million budget that will allow for expanded operations and marketing initiatives to accelerate Vesper’s growth
Partner Program: these funds will go towards incentives for pools created for partner protocols, which bring in deposits from their treasury and community, driving an increase in fee revenue for Vesper
Replenishing VSP Reserves: these funds will go towards buying VSP to extend the VSP pool incentives past their current expected expiration in August/September 2022. This allocation will be gradually increased over the course of a year in order to make the decrease in vVSP rewards more gradual

## Specification
Some fee revenue will be diverted from VSP buybacks and vVSP reward payouts to wallets for each new initiative.
The algo-trading strategy for the treasury will determine if assets should be allocated to stablecoins or a specific allocation of other tokens (ETH, UNI, LINK, and VSP) to minimize the drawdown of treasury funds. This strategy will only impact the allocation of new funds and will not touch existing VSP holdings to avoid excessive sell pressure.

##Test Cases
Economics Design examined historical data on Vesper’s fees and devised recommendations for Vesper’s new fee structure, fee revenue allocation, and treasury management. Their team also conducted financial analysis of the projected impact to balance a short-term revenue drop with a goal of improving long-term growth.

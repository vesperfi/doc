# VIP: Emissions Upgrade

Status: Pending

## Summary

Adopted from [VIP-9](https://github.com/vesperfi/doc/blob/main/vips/VIP-9.md), this proposal outlines just the emissions upgrades as part of the broader "Treasury V2" overhaul.

## Abstract

VIP-10 is intended to correct the VSP over-subsidization of pools and create a global emissions budget that can scale as new pools arrive. It also incorporates a future-proof mechanism for LP rewards once the current schedule expires and as VSP is ported to other networks.


## Expectations

**Emissions**

 The global VSP fund reflects the outstanding proposed emissions schedule in an earlier VIP:
* Month 7 (starts August 17): 120,000 VSP
* Month 8: 90,000 VSP
* Month 9: 67,500 VSP
* Month 10: 52,500 VSP
* Month 11: 40,000 VSP
* Month 12: 35,000 VSP
* Month 13+: 30,000 VSP
 Point allocation will rebalance each month based on TVL, with greater TVL awarding higher weight.
* #1 highest TVL pool: 5 points
* 2-3: 4 points
* 4-5: 3 points
* 6-8: 2 points
* 9+: 1 point
New pools will automatically be allocated 3 points for the first month after launch and 2 points for the second month, and are absorbed into the above methodology starting their third month.

LP rewards will have separate emissions, reflective of the existing schedule. (Uniswap LP program is prefunded through Month 12 and will be integrated on Month 13, hence the emissions increase).
* Month 7-12: 34,500 VSP
* Month 13+: 45,000 VSP
Point allocation (based on trading volume)
* SushiSwap: 5 points
* #1 highest volume (excluding SushiSwap on ETH Layer 1): 3 points
* 2-3: 2 points
* 4+: 1 point
New markets start with 2 point allocation in their two months, and are absorbed into the above methodology starting their third month.

## Specification

VSP administrators to make proposed upgrades and pertinent treasury accounts to be handed over to DAO governance.

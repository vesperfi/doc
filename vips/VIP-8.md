# VIP: Shift VSP Emissions for Pool Rewards

Status: Draft

## Summary

Shift the allocated VSP emissions for the remaining months in order to create a more gradual "sunset" of rewards.

## Background

VSP rewards for pool participants work to attract TVL to Vesper Grow pools and fairly distribute VSP to participants in the ecosystem. This shifting of VSP rewards seeks to minimize friction as rewards ultimately decrease over time until they are "sunset" altogether.

## Expectations

There is 8 months of VSP rewards remaining for participants in vETH, vUSDC, and vWBTC pools (month 5-month 12). The existing per month breakdown is as follows:

|       |  TOTAL | Month 4 | Month 5 | Month 6 | Month 7 | Month 8 | Month 9 | Month 10 | Month 11 | Month 12 |
|:-----:|:------:|:-------:|:-------:|:-------:|:-------:|:-------:|:-------:|:--------:|:--------:|:--------:|
| vETH  | 740000 | 100,000 |  45,000 |  35,000 |  35,000 |  30,000 |  30,000 |   30,000 |   30,000 |   30,000 |
| vUSDC | 690000 |  50,000 |  45,000 |  35,000 |  35,000 |  30,000 |  30,000 |   30,000 |   30,000 |   30,000 |
| vWBTC | 740000 | 100,000 |  45,000 |  35,000 |  35,000 |  30,000 |  30,000 |   30,000 |   30,000 |   30,000 |

This proposal seeks to shift rewards to diminish more gradually. There is no net change in the total distributed throughout the duration.

|       |  TOTAL | Month 4 | Month 5 | Month 6 | Month 7 | Month 8 | Month 9 | Month 10 | Month 11 | Month 12 |
|:-----:|:------:|---------|---------|---------|---------|---------|---------|----------|----------|----------|
| vETH  | 740000 | 100,000 |  75,000 |  55,000 |  40,000 |  30,000 |  22,500 |   17,500 |   13,333 |   11,667 |
| vUSDC | 690000 |  50,000 |  75,000 |  55,000 |  40,000 |  30,000 |  22,500 |   17,500 |   13,333 |   11,667 |
| vWBTC | 740000 | 100,000 |  75,000 |  55,000 |  40,000 |  30,000 |  22,500 |   17,500 |   13,333 |   11,667 |

## Specification

VSP reserve signers will follow the revised emissions schedule outlined in this proposal for each coming month's rewards.



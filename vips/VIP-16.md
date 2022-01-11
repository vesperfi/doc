# Zero Fee like-Token intra-Vesper Transfers
Status: Passed

## Summary
Zero withdrawal fee, for pool-to-pool transfers within Vesper.

This proposal rests on top of , and depends on, proposal #32.

## Specification
Do not charge a fee when moving tokens from one Vesper pool into another Vesper pool. e.g. Moving ETH from a conservative Grow pool to an ETH-DAI Earn pool. This may only be applied

In cases where the withdraw token from the old pool (e.g. ETH) and the deposit token into the new pool (e.g. ETH, again) are the same.
In cases where the withdraw pool and the deposit pool are both Vesper Grow or Earn pools. This does not apply to lending or other products.

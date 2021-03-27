
# VIP-draft: Add LINK pool

## Summary

Whitelist the LINK token, and promote the LINK pool to tier-1 production.

## Abstract

Research the LINK token (Ethereum ERC20), and whitelist if the technical
qualifications are met.  Deploy a LINK pool to public beta testing, and
auditors.  Finally, promote the LINK pool from beta to production.

## Expectations

Research the LINK token to ensure it is compatible with the Vesper
system, and compiles with relevant standards (e.g. ERC20).

The LINK Grow pool behavior will mimic existing Vesper Grow pools:
"Deposit-X, Earn-X", compounding the LINK token without risk of
impermanent loss or other common balance-goes-down scenarios.

Underlying algorithmic strategies employed will include Direct-to-X
(deposit 90+% into Compound, Aave or another lending platform) and Maker
strategies.  Strategies will be maintained and upgraded as directed by
the Vesper community and Vesper Pool Ops.

Liquidity will be bootstrapped by assigning VSP from community treasury,
at a level recommended by OpComm.

## Specification

* Whitelist LINK token.
* Create LINK pool (sub-class of pool base);
* Create LINK-Maker strategy (sub-class of Maker strategy) and LINK-Direct-to-X strategy (sub-class of Direct-to-X).
* Deploy pool to beta, for live mainnet testing.
* Send to auditors.
* Deploy to pool production.
* Assign VSP to production pool.


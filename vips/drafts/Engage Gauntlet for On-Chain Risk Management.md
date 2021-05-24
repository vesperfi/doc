# VIP: Engage Gauntlet for On-Chain Risk Management

Status: Draft 

## Summary

Vesper will partner with Gauntlet to build out and implement a risk management system to assess Vesper pools and better optimize strategies.

## Background

Gauntlet is a simulation platform for market risk management and protocol optimization. Gauntlet uses battle-tested techniques from the algorithmic trading industry to inform on-chain protocol management. We use agent-based simulation to help protocols manage risk, capital efficiency, fees, and rewards.
Recent work, relevant to Vesper Grow Pools, includes assessments for [Compound](https://gauntlet.network/reports/compound), [Aave](https://gauntlet.network/reports/aave), and [MakerDAO](https://maker-report.gauntlet.network/). Gauntlet’s continuous optimization work, similar to what we would like to do for Vesper, includes [Balancer](https://medium.com/balancer-protocol/balancer-partners-with-gauntlet-to-make-dynamic-fee-pools-a-reality-97b3fb1760df), [SushiSwap](https://medium.com/gauntlet-networks/optimizing-token-emissions-for-sushiswap-23dfe5bf9962), and [Acala](https://medium.com/gauntlet-networks/gauntlet-to-provide-automated-financial-risk-management-for-acala-and-karura-3f912adfe3a7). 

## Abstract 

The work outlined in this proposal reflects a risk management system for Vesper pools. Following Gauntlet's initial due diligence on the Vesper protocol and Grow Pools, our two main concerns were static risk management and arbitrary collateralization benchmarks. Volatility, liquidity, and other variables like network congestion make continuous risk management necessary to improve capital efficiency and maximize yields. The second issue is the low-water and high-water collateralization benchmarks. The initial strategy benchmarks will benefit from greater precision and monitoring to properly balance risk and reward (yield). Gauntlet will build a financial model focusing on managing risk, improving capital efficiency, and increasing total value locked on the Vesper protocol.

## Expectations

Gauntlet will ingest numerous live data feeds from Ethereum, centralized and decentralized exchanges, and the Vesper contracts to ensure our models can remain in lockstep with changing market conditions. The data is then ingested into numerous specialized models. For Vesper, Gauntlet will deploy the following models: 

- Market Liquidity Model: Slippage and price impact
- Agent Models: Borrower and liquidator behavior
- [MultiGBM](https://en.wikipedia.org/wiki/Geometric_Brownian_motion) model: Covariance matrix and price trajectories
- Transaction Delay Model: Gas prices and confirmation delay

The above models coalesce into the Lending Risk Model, which will have the primary function of outputting collateralization benchmarks. Gauntlet's models may identify other risks and optimization opportunities. For example, Vesper's rebalancing mechanism may require upgrades as more strategies and assets enter the Grow Pools. When identified, Gauntlet will proactively make governance proposals, similar to how we do for [Compound Governance](https://compound.finance/governance/address/0x6626593c237f530d15ae9980a95ef938ac15c35c), to ensure the protocol is functioning optimally.

Gauntlet will develop a Vesper Risk Management Dashboard to provide easy-to-digest metrics across assets, strategies, and risk levels. For any simulation output or suggested protocol upgrade, Vespernauts can expect to find Gauntlet active in the community (e.g., Discord) to provide clarifications and follow-ups from our analysis. 

This proposal is intended to buildout the proper tools to automate risk management, increase capital efficiency, and improve the user experience. The top-line goal is higher TVL and revenue to Vesper, which is expected to follow with the improvements listed. 

In return, strategies that are managed by Gauntlet’s simulation platform will draw 1.5% of revenue back to Gauntlet. These pools would instead reflect a 93.5/1.5/5 % split rather than 95/5.

## Specification

* Modify revenue splitter contract so vToken shares on pools leveraging Gauntlet split funds 93.5/1.5/5 with 1.5% to Gauntlet wallet (`0xD20c9667bf0047F313228F9fE11F8b9F8Dc29bBa`)


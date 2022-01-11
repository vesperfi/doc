# Token Whitelisting Frenzy

VIP-14
Status: Passed

## Summary

Vesper is uniquely positioned to service a huge and growing demand for risk-on DeFi degens to maximize the efficiency of their capital. Market participants have shown a willingness to pay huge premiums for the privilege of collateralizing aggressive assets to take out loans as well as deploying those assets to generate additional yield beyond whatever metrics the underlying token possesses.

With a more proactive approach to supporting new and high revenue tokens, Vesper can benefit from higher TVL, stronger revenue, and better exposure to the DeFi communities who need products like Vesper.

## Background Research

Rari Fuse’s rapid rise to over $1 billion TVL, seemingly overnight, sans incentives, can be linked to the engagement of the Olympus DAO community, who benefit from a product that enables them to take out loans for additional leverage on their staked OHM tokens (which generate 8,000% APY already). Over Rari’s $1.3 billion TVL, over half of that is attributed to sOHM deposits in Pool #6 and Pool #18.

These assets are used primarily as collateral to take out stablecoin loans. For sOHM holders taking out these loans, this gives them the opportunity to generate more profit beyond their existing 8,000% APY:
- They can use stablecoins to buy more sOHM and redeposit for a leveraged position (at a somewhat-conservative 40% loan-to-value, they can boost their APY well over 10,000%)
- They can use those stablecoins to farm at other aggressive destinations, taking advantage of yield arbitrage between borrow interest and deposit rates.
- They can ape into projects incubated in the OHM ecosystem via Olympus Pro, further invigorating the Olympus protocol and with a strong conviction of significant ROI.

This risk-on nature translates to huge premiums on loans. Borrowers using sOHM in these pools routinely borrow at rates of 20-100% APR. (Our aggressive DAI pool is a major supplier on these loans, and benefits from the premium rates).

The Rari community and RGT, as the sole providers of “do more” for the Olympus community, have benefited immensely from their endorsement of OHM, as each community has heavily tapped into one another and been able to multiply their growth through the comradery. 

Centralized platforms are taking advantage of this market dynamic as well. SHIB shorters recently were paying 400% APR on FTX for the privilege of selling dog token at market price.

## Abstract

I see three distinct opportunities, substantiated by market trends, that Vesper is wholly prepared to take advantage of:
- Support risk-on assets to create exciting products that generate premium yield (and premium revenue for VSP holders).
- Tap-in to “buzzing” DeFi 2.0 tokens/communities as a means to grow TVL and market Vesper to new groups
- “Incubate” upcoming, aggressive, or controversial tokens (similarly to what Rari has done for OHM) by creating yield sources and hooking those tokens up to them via our Vesper pools.

However, this needs to be done in such a way that does not compromise the overall security of Vesper or diminish our carefully crafted reputation as the responsible, secure yield source. 

Some tokens exist on my radar that hit the checkboxes of:
- capable of good, sustainable yield at high TVL
- ready-for-integration in our bluechip strategies
- more-or-less responsible tokenomics regarding an interesting product that reasonably exists well into the future

This proposal outlines tokens that meet these criteria. Those who do not will be handled separately in the "Vesper Orbit" VIP.

Whitelisted tokens are greenlit for Vesper Lend, Vesperdev app, [Orbit, and Orbit Lend (pending VIP)]. All tokens must graduate from Vesperdev before hitting the main app.

Whitelist:

Abracadabra
- MIM
- SPELL
- sSPELL

SushiSwap
- SUSHI
- xSUSHI

Olympus
- OHM
- sOHM
- wsOHM

Frax Finance
- FRAX
- FXS

Gelato Network
- G-UNI(DAI-USDC)

Unit Protocol
- USDP

Aave
- AAVE
- stkAAVE

Compound
- COMP
 
Yearn
- YFI
- yvUSDC
- yvUSDT
- yvETH
- yvWBTC

Fei Protocol
- FEI
- TRIBE

Alchemix
- ALCX
- alUSD
- alETH

Curve & Convex
- CRV
- CVX
- crvCVX

Metronome
- MET

Terra
- LUNA
- UST

Brave
- BAT

Synthetix
- sUSD
- SNX

Binance
- BNB
- BUSD

Index Coop
- MVI

NOTE that whitelisting does not require that a product is built out on top of the whitelisted asset. Many of these integrations are low burden (forking frontend, strategies, pools). Some however require extra care, and those with “elevated” engineering burdens will be scheduled against other Vesper engineering needs. 

Elevation from whitelist to integration (particularly on lending markets) also requires safety assessment on vulnerability of token to be leveraged for exploits.

## Specification

- Whitelist the following tokens Vesper-wide: MIM, SPELL, sSPELL, SUSHI, xSUSHI, OHM, sOHM, wsOHM, FRAX, FXS, G-UNI(DAI-USDC), USDP, AAVE, stkAAVE, COMP, YFI, yvUSDC, yvUSDT, yvDAI, yvETH, yvWBTC, FEI, TRIBE, ALCX, alUSD, alETH, CRV, CVX, crvCVX, MET, LUNA, UST, BNB, BUSD, MVI, SNX, SUSD
- Vesper to build products and integrate tokens following whitelisting as seen most apt.

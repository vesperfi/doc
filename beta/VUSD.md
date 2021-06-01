# VUSD Beta Information

## Summary

VUSD is a collateral-backed, Ethereum-native, USD-pegged stablecoin.

## Status

VUSD is in public beta, with a 50M mint limit.

Users should exercise additional caution during this phase.  Risk-averse users should wait until after the beta test period is complete.

## Game theory

VUSD may be minted from, and redeemed for, DAI, USDC or USDT on a 1:1 basis (less minting fee or redeem fee).

If the VUSD price rises above US$1.00, it is cheaper to mint VUSD using the Minter module, rather than swapping on the spot market.

If the VUSD price falls below US$1.00, it is cheaper to redeem VUSD for collateral using the Redeemer module, rather than swapping on the spot market.

## Contracts

* VUSD token: 0x677ddbd918637E5F2c79e164D402454dE7dA8619
* Minter (DAI/USDC/USDT -> VUSD): 0x7C148217c7f99504AbEB4582334c9189e5F11397
* Redeemer (VUSD -> DAI/USDC/USDT): 0x7915CE4F43E1378f0C3720351A973A023F7fB3e8
* Treasury (holds c-tokens): 0x813E891e2Bb6729beF4185663624bd09F4902bD8

## Minting VUSD

Minting fee is zero (0.00%) during this phase.

1. Approve the Minter contract spending your DAI, USDC or USDT tokens at https://pure.finance/token-approvals   Enter the token ticker symbol under Token Address, and enter the Minter contract address - 0x7C148217c7f99504AbEB4582334c9189e5F11397 - as the Spender Address.
2. Decide on the amount of DAI (or USDC or USDT) to mint.
3. Convert this amount to integer.  For DAI, with 18 decimals, use this calculator: https://eth-converter.com/   For USDC or USDT, add six zeros after the dollars.  e.g. $1000.12 becomes 1000120000.
4. Visit https://etherscan.io/address/0x7c148217c7f99504abeb4582334c9189e5f11397#writeContract and connect your web3 wallet such as MetaMask.
5. To mint VUSD, call the #2 Mint function.  The `_token (address)` is the address of the deposit token (e.g. 0x6b175474e89094c44da98b954eedeac495271d0f for DAI). The `_amount (uint256)` is the amount calculated in step 3.
6. Click the **Write** button to submit an Ethereum transaction minting VUSD.

When the transaction confirms, VUSD will have been credited to your wallet, and DAI, USDC or USDT will have been deducted from your wallet.

## Redeeming VUSD

Redemption fee is 0.3% during this phase.

1. Approve the Redeemer contract spending your VUSD tokens at https://pure.finance/token-approvals   Enter the VUSD contract address - 0x677ddbd918637E5F2c79e164D402454dE7dA8619 - under Token Address, and enter the Redeemer contract address - 0x7915CE4F43E1378f0C3720351A973A023F7fB3e8 - as the Spender Address.
2. Decide on the amount of VUSD to redeem.
3. Convert this amount to integer.  Use this calculator: https://eth-converter.com/ 
4. Visit https://etherscan.io/address/0x7915ce4f43e1378f0c3720351a973a023f7fb3e8#writeContract and connect your web3 wallet such as MetaMask.
5. To redeem VUSD, call the #2 Redeem function.  The `_token (address)` is the address of the token to be received (e.g. 0x6b175474e89094c44da98b954eedeac495271d0f for DAI). The `_vusdAmount (uint256)` is the amount calculated in step 3.  And `_tokenReceiver (address)` is the address receiving the collateral tokens (your wallet address).
6. Click the **Write** button to submit an Ethereum transaction redeeming VUSD.

When the transaction confirms, VUSD will have been debited from your wallet, and DAI, USDC or USDT will have been sent to your wallet.

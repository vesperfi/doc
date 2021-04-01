# Vesper Finance - Products and Pools FAQ

*A Vesper Community FAQ Powered by COIN$TAR*

**Q. Where can I buy VSP?**

Uniswap, Sushiswap, and Loopring currently. You can also use DEX aggregators like 1inchexchange or matchaXYZ.

**Q. Any plans on getting listed on a CEX? When Binance?**

Of course they are working on this behind the scenes. Liquidity is vital for every project. CEXs have NDAs so even if the team knew when Binance, if they told us Binance would cancel the deal. 

**Q. Why is Deposit/Withdraw button grayed out?**

First make sure there is ETH in your wallet. Vesper is a DEFI platform on top of Ethereum, thus gas is needed for transactions. Also make sure you are either entering an amount to Deposit/Withdraw or hitting the preset % buttons.

**Q. Why is the 100% deposit button not working for the ETH pool?**

If you deposited 100% of your ETH balance you would have no ETH left to pay the gas fees. 

**Q. How many transactions are needed to deposit? Do all transactions have gas fees?**

For all pools but the ETH pool, 2. For the ETH pool, 1. This is because for a smart contract to take ERC20 tokens from your wallet you have to first "approve" of its ability to do so. So the ERC20 pools such as wBTC, VSP, USDC, or DAI you have to do this first approval transaction. Then in the second transaction it swaps your asset for the corresponding amount of vAsset tokens. As this is all done on ETH mainnet, each transaction will need you to have ETH for the gas fees. 

**Q. Are deposits locked?**

Deposits are never locked for any pools except for the VSP pool. The VSP pool locks you out of withdrawing for 24 hours after your last deposit. This is to prevent whales/bots from gaming the buyback/rewards system. Ie. Dumping a ton of VSP into the pool right before rewards are distributed, then immediately taking it all out. 

**Q. Do I earn rewards when my VSP deposit is locked for the first 24 hours?**

Yes. As soon as you receive vVSP it is already autocompunding and earning more VSP for you. Nothing more has to be done on your end. 

**Q. Why did I recieve less vVSP than the VSP I put into the VSP pool? Is this a hefty fee?**

There are no fees for depositing into any Vesper pools, including VSP. The vVSP you recieve is not a 1:1 ratio with VSP. Vesper uses an autocompounding approach such that your vVSP is constantly gaining value vs VSP (and thus as more time goes on you can withdraw more and more VSP given the same vVSP amount). 

So for example if you deposit 100 VSP you can expect to see a balance of 100 VSP (which will soon grow) and a vVSP amount (less than 100) that will never change.

**Q. I see there is a 15% yield fee does this mean I will lose 1.5 ETH if I have a 10 ETH balance I want to withdraw?**

No the only fee which you will "feel" or "see" is the 0.6% withdrawal fee. The 15% fee on yield is baked into the backend. It is taken from the total yield the entire pool generated whenever the app goes to distribute it back to the stakers in the pool. So it was money you were never promised and you will never see. Note that the VSP pool itself does not have a 0.6% fee (since the whole point of fees is to provide revenue for buybacks of VSP for VSP stakers)

**Q. How can I track my pool rewards?**

In the Vesper app you will see your balances under the Withdraw column. Your base asset (ETH, wBTC, DAI) will grow as shown in the top balance. The bottom balance is the vAsset (vETH, vwBTC, vDAI) and is a constant that will never change (given you dont deposit or withdraw). 

You can also use zapper.fi and it will show your asset balance as it grows. Note that it doesn't yet support showing VSP rewards given to the pools other than the vVSP pool yet. 

**Q. Can I directly stake my VSP rewards from say the ETH pool to the VSP pool without claiming then depositing?**

Not yet but it is a highly requested feature the team is working on


JLP is a liquidity pool that acts as a market maker across SOL/ETH/BTC pools on Jupiter perps. It's value is = value of holdings + traders pnl + 75% of trading fees. JLC tokens represent your share of the pool. Opening and closing fees dominate the total amount.
The holdings can be measured in real time and in theory JLP should trade = sum of holdings / JLP supply. An additional strategy is add/reduce exposure when JLP deviates from fair value - extra JLP can be minted/redeemed when price deviates. These values can be retrieved from the blockchain, see below example code :
- Theoretical price : https://github.com/julianfssen/jupiter-perps-anchor-idl-parsing/blob/main/src/examples/get-jlp-virtual-price.ts
- Compute pool aum : https://github.com/julianfssen/jupiter-perps-anchor-idl-parsing/blob/main/src/examples/calculate-pool-aum.ts
If you hedge the token exposure through perps, you get a return stream = traders pnl + 75% trading fees + perp funding rate. For capital efficiency, you can use JLP loans to borrow USDC using JLP as collateral up to a 80% LTV.

![[Pasted image 20250924205200.png]]
# 🧀 Fees

### Liquidity provider fees[​](https://docs.uniswap.org/contracts/v2/concepts/advanced-topics/fees#liquidity-provider-fees) <a href="#liquidity-provider-fees" id="liquidity-provider-fees"></a>

There is a **0.3%** fee for swapping tokens. **This fee is split by liquidity providers proportional to their contribution to liquidity reserves.**

Swapping fees are immediately deposited into liquidity reserves. This increases the value of liquidity tokens, functioning as a payout to all liquidity providers proportional to their share of the pool. Fees are collected by burning liquidity tokens to remove a proportional share of the underlying reserves.

Since fees are added to liquidity pools, the invariant increases at the end of every trade. Within a single transaction, the invariant represents `token0_pool / token1_pool` at the end of the previous transaction.

There are many community-developed tools to determine returns. You can also read more in the docs about how to think about [LP returns](https://docs.uniswap.org/contracts/v2/concepts/advanced-topics/understanding-returns).

**When providing liquidity on Jibswap v2:**

* The Jibswap v2 protocol only has a 0.3% fee tier.
* In v2 the fees are auto compounded into the liquidity pool. This means for every swap the fee will go back into the pool, increasing the value of your position.
* When removing Jibswap v2 liquidity positions, Fees are collected with the liquidity.

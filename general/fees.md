# 🧀 Fees

### Liquidity provider fees[​](https://docs.uniswap.org/contracts/v2/concepts/advanced-topics/fees#liquidity-provider-fees) <a href="#liquidity-provider-fees" id="liquidity-provider-fees"></a>

There is a **0.3%** fee for swapping tokens. **This fee is split by liquidity providers proportional to their contribution to liquidity reserves.**

Swapping fees are immediately deposited into liquidity reserves. This increases the value of liquidity tokens, functioning as a payout to all liquidity providers proportional to their share of the pool. Fees are collected by burning liquidity tokens to remove a proportional share of the underlying reserves.

Since fees are added to liquidity pools, the invariant increases at the end of every trade. Within a single transaction, the invariant represents `token0_pool / token1_pool` at the end of the previous transaction.

There are many community-developed tools to determine returns. You can also read more in the docs about how to think about [LP returns](https://docs.uniswap.org/contracts/v2/concepts/advanced-topics/understanding-returns).

### Protocol Fees[​](https://docs.uniswap.org/contracts/v2/concepts/advanced-topics/fees#protocol-fees) <a href="#protocol-fees" id="protocol-fees"></a>

At the moment there are no protocol fees. However, it is possible for a 0.05% fee to be turned on in the future.

More information about a potential future protocol fee can be found [here](https://uniswap.org/blog/uniswap-v2/#path-to-sustainability).

### Protocol Charge Calculation[​](https://docs.uniswap.org/contracts/v2/concepts/advanced-topics/fees#protocol-charge-calculation) <a href="#protocol-charge-calculation" id="protocol-charge-calculation"></a>

In the future, it is possible that a protocol-wide charge of 0.05% per trade will take effect. This represents ⅙th (16.6̅%) of the 0.30% fee. The fee is in effect if feeTo is the recipient of the charge.

This amount would not affect the fee paid by traders, but would affect the amount received by liquidity providers.

Rather than calculating this charge on swaps, which would significantly increase gas costs for all users, the charge is instead calculated when liquidity is added or removed. See the [whitepaper](https://docs.uniswap.org/whitepaper.pdf) for more details.

**When providing liquidity on Jibswap v2:**

* The Jibswap v2 protocol only has a 0.3% fee tier.
* In v2 the fees are auto compounded into the liquidity pool. This means for every swap the fee will go back into the pool, increasing the value of your position.
* When removing Jibswap v2 liquidity positions, Fees are collected with the liquidity.

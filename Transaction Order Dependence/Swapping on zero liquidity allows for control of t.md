Swapping on zero liquidity allows for control of the pool’s price: Swapping on a tick with zero liquidity enables a user to adjust the price of 1 wei of tokens in any direction. As a result, an attacker could set an arbitrary price at the pool’s initialization or if the liquidity providers withdraw all of the liquidity for a short time.

    Recommendation: No straightforward way to prevent the issue. Ensure pools don’t end up in unexpected states. Warn users of potential risks.

    Medium Risk severity finding from ToB’s Audit of Uniswap V3
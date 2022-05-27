Front-running pool’s initialization can lead to draining of liquidity provider’s initial deposits: A front-run on UniswapV3Pool.initialize allows an attacker to set an unfair price and to drain assets from the first deposits. There are no access controls on the initialize function, so anyone could call it on a deployed pool. Initializing a pool with an incorrect price allows an attacker to generate profits from the initial liquidity provider’s deposits.

    Recommendation: 1) moving the price operations from initialize to the constructor, 2) adding access controls to initialize, or 3) ensuring that the documentation clearly warns users about incorrect initialization.

    Medium Risk severity finding from ToB’s Audit of Uniswap V3
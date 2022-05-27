Calls to setParams may set invalid values and produce unexpected behavior in the staking contracts: Certain parameters of the contracts can be configured to invalid values, causing a variety of issues and breaking expected interactions between contracts. setParams allows the owner of the staking contracts to reparameterize critical parameters. However, reparameterization lacks sanity/threshold/limit checks on all parameters.

    Recommendation: Add proper validation checks on all parameters in setParams. If the validation procedure is unclear or too complex to implement on-chain, document the potential issues that could produce invalid values.

    Medium Risk severity finding from ToB’s Audit of 0x Protocol
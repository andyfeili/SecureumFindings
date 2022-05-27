Contract Owner Can Arbitrarily Change Minting Fees and Interest Rates: The issueFeeRate and interestRate variables can both be changed by the EtherCollateral contract owner after loans have been opened. As a result, the owner can control fees such as they equal/exceed the collateral for any given loan.

    Recommendation: While "dynamic" interest rates are common, we recommend considering the minting fee ( issueFeeRate ) to be a constant that cannot be changed by the owner.

    Medium Risk severity finding from Sigma Prime's Audit of Synthetix EtherCollateral
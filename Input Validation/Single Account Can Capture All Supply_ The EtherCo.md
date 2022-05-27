Single Account Can Capture All Supply: The EtherCollateral smart contract does not rely on a maxLoanSize to limit the amount of ETH that can be locked for a loan. As a result, a single account can issue a loan that will reach the total minting supply.

    Recommendation: Make sure this behaviour is understood and consider introducing and enforcing a cap ( maxLoanSize ) on the size of the loans allowed to be opened.

    Sigma Prime's Audit of Synthetix EtherCollateral
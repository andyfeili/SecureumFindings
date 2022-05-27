Insufficient Input Validation: The constructor of the EtherCollateral smart contract does not check the validity of the addresses provided as input parameters. It is possible to deploy an instance of the EtherCollateral contract with the synthProxy , sUSDProxy and depot addresses set to zero. Similarly, the effective interest rate can be equal to zero if interestRate is set to any value lesser than 31536000 ( SECONDS_IN_A_YEAR ), as interestPerSecond will be null.

    Recommendation: Consider introducing require statements to perform adequate input validation.

    Sigma Prime's Audit of Synthetix EtherCollateral
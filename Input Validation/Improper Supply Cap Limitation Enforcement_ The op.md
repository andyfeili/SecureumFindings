Improper Supply Cap Limitation Enforcement: The openLoan() function does not check if the loan to be issued will result in the supply cap being exceeded. It only enforces that the supply cap is not reached before the loan is opened. As a result, any account can create a loan that exceeds the maximum amount of sETH that can be issued by the EtherCollateral contract.

    Recommendation: Introduce a require statement in the openLoan() function to prevent the total cap from being exceeded by the loan to be opened.

    High Risk severity finding from Sigma Prime's Audit of Synthetix EtherCollateral
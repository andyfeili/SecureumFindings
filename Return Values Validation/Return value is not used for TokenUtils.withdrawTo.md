Return value is not used for TokenUtils.withdrawTokens: The return value of TokenUtils.withdrawTokens which represents the actual amount of tokens that were transferred is never used throughout the repository. This might cause discrepancy in the case where the original value of _amount was type(uint256).max.

    Recommendation: The return value can be used to validate the withdrawal or used in the event emitted

    ConsenSys's Audit of DeFi Saver
External Call Reverts if Period Has Not Elapsed: The function notifyRewardAmount() will revert if block.timestamp >= periodFinish. However this function is called indirectly via the Synthetix.mint() function. A revert here would cause the external call to fail and thereby halt the mint process. Synthetix.mint() cannot be successfully called until enough time has elapsed for the period to finish.

    Recommendation: Consider handling the case where the reward period has not elapsed without reverting the call.

    High Risk severity finding from Sigma Prime's Audit of Synthetix Unipool
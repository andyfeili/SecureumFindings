Staking Before Initial notifyRewardAmount Can Lead to Disproportionate Rewards: If a user successfully stakes an amount of UNI tokens before the function notifyRewardAmount() is called for the first time, their initial userRewardPerTokenPaid will be set to zero. The staker would be paid out funds greater than their share of the SNX rewards.

    Recommendation: We recommend preventing stake() from being called before notifyRewardAmount() is called for the first time.

    High Risk severity finding from Sigma Prime's Audit of Synthetix Unipool 
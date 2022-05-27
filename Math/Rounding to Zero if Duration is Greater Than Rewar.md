Rounding to Zero if Duration is Greater Than Reward: The rewardRate value is calculated as follows: rewardRate = reward/duration. Due to the integer representation of these variables, if duration is larger than reward the value of rewardRate will round to zero. Thus, stakers will not receive any of the reward for their stakes. Furthermore, due to the integer rounding, the total rewards distributed may be rounded down by up to one less than duration . As a result, the Unipool contract may slowly accumulate SNX.

    Recommendation: Beware of the rounding issues when calling the notifyRewardAmount() function. We also recommend some way of allowing the excess SNX reward from rounding to be claimed or withdrawn from the Unipool contract.

    Sigma Prime's Audit of Synthetix Unipool
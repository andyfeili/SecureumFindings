 _assertStakingPoolExists never returns true: The _assertStakingPoolExists should return a bool to determine if the staking pool exists or not; however, it only returns false or reverts. The _assertStakingPoolExists function checks that a staking pool exists given a pool id parameter. However, this function does not use a return statement and therefore, it will always return false or revert.

    Recommendation: Add a return statement or remove the return type. Properly adjust the documentation, if needed.

    ToB's Audit of 0x Protocol
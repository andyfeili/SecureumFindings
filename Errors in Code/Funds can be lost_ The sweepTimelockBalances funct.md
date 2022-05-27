Funds can be lost: The sweepTimelockBalances function accepts a list of users with unlocked balances to distribute. However, if there are duplicate users in the list, their balances will be counted multiple times when calculating the total amount to withdraw from the yield service.

    Recommendation: Consider checking for duplicate users when calculating the amount to withdraw.

    OpenZeppelin's Audit of PoolTogether V3
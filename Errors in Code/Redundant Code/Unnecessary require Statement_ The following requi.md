Unnecessary require Statement: The following require statement in Blacklistable.sol can be removed: require(to != address(0)); Indeed, this check is implemented in the _transfer() function in the ERC20.sol smart contract.

    Recommendation: Consider removing the require statement for gas saving purposes.

    Sigma Prime's Audit of InfiniGold
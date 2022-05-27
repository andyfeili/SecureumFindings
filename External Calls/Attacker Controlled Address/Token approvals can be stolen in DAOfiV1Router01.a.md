Token approvals can be stolen in DAOfiV1Router01.addLiquidity(): DAOfiV1Router01.addLiquidity() creates the desired pair contract if it does not already exist, then transfers tokens into the pair and calls DAOfiV1Pair.deposit(). There is no validation of the address to transfer tokens from, so an attacker could pass in any address with nonzero token approvals to DAOfiV1Router. This could be used to add liquidity to a pair contract for which the attacker is the pairOwner, allowing the stolen funds to be retrieved using DAOfiV1Pair.withdraw().

    Recommendation: Transfer tokens from msg.sender instead of lp.sender

    Critical severity finding from Consensys Diligence Audit of DAOfi
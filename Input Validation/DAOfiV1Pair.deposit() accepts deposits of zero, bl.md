DAOfiV1Pair.deposit() accepts deposits of zero, blocking the pool: DAOfiV1Pair.deposit() is used to deposit liquidity into the pool. Only a single deposit can be made, so no liquidity can ever be added to a pool where deposited == true. The deposit() function does not check for a nonzero deposit amount in either token, so a malicious user that does not hold any of the baseToken or quoteToken can lock the pool by calling deposit() without first transferring any funds to the pool.

    Recommendation: Require a minimum deposit amount with non-zero checks

    Medium severity finding from Consensys Diligence Audit of DAOfi
Using empty functions instead of interfaces leaves contract error-prone: WithdrawalDelayerInterface is a contract meant to be an interface. It contains functions with empty bodies instead of function signatures, which might lead to unexpected behavior. A contract inheriting from WithdrawalDelayerInterface will not require an override of these functions and will not benefit from the compiler checks on its correct interface.

    Recommendation: Short term, use an interface instead of a contract in WithdrawalDelayerInterface. This will make derived contracts follow the interface properly. Long term, properly document the inheritance schema of the contracts. Use Slither’s inheritance-graph printer to review the inheritance.

    ToB's Audit of Hermez Network
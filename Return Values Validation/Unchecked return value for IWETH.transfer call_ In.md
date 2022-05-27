Unchecked return value for IWETH.transfer call: In EthUniswapPCVController, there is a call to IWETH.transfer that does not check the return value. It is usually good to add a require-statement that checks the return value or to use something like safeTransfer; unless one is sure the given token reverts in case of a failure.

    Recommendation: Consider adding a require-statement or using safeTransfer

    Medium severity finding from Consensys Diligence Audit of Fei Protocol
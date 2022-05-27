Insufficient use of SafeMath: CurveMath.calculateTrade is used to compute the output amount for a trade. However, although SafeMath is used throughout the codebase to prevent underflows/overflows, it is not used in this calculation. Although we could not prove that the lack of SafeMath would cause an arithmetic issue in practice, all such calculations would benefit from the use of SafeMath.

    Recommendation: Review all critical arithmetic to ensure that it accounts for underflows, overflows, and the loss of precision. Consider using SafeMath and the safe functions of ABDKMath64x64 where possible to prevent underflows and overflows.

    ToB's Audit of DFX Finance
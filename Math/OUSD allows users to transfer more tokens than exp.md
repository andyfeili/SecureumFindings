OUSD allows users to transfer more tokens than expected: Under certain circumstances, the OUSD contract allows users to transfer more tokens than the ones they have in their balance. This issue seems to be caused by a rounding issue when the creditsDeducted is calculated and subtracted.

    Recommendation: Short term, make sure the balance is correctly checked before performing all the arithmetic operations. This will make sure it does not allow to transfer more than expected. Long term, use Echidna to write properties that ensure ERC20 transfers are transferring the expected amount.

    High Risk severity finding from ToB’s Audit of Origin Dollar
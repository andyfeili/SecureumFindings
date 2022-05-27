Unsafe casting: In line 554 of the TaxCollector contract, the value of coinBalance(receiver) is an uint. This is cast to an int and then negated. However, since uint can store higher values than int, it is possible that casting from uint to int may create an overflow.

    Recommendation: Consider verifying that the value of coinBalance(receiver) is within the acceptable range for negative int values before casting and negating. Consider using OpenZeppelin’s SafeCast contract, which provides functions for safely casting between types.

    OpenZeppelin's Audit of GEB Protocol
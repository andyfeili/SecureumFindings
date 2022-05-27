Unnecessary require statements: There are several instances in the code base where the require statements or conditional checks are unnecessary. For instance: In the OracleRelayer contract, the require statement in the modifyParameters function at line 189 checks if the input parameter data > 0. This is unnecessary since the same condition is already checked in the require statement at line 187.

    Recommendation: To simplify the code and prevent wastage of gas, consider removing the unnecessary checks.

    OpenZeppelin's Audit of GEB Protocol
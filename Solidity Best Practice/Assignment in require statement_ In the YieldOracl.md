Assignment in require statement: In the YieldOracle contract, there is a require statement that makes an assignment. This deviates from the standard usage and intention of require statements and can easily lead to confusion.

    Recommendation: Consider moving the assignment to its own line before the require statement and then using the require statement solely for condition checking.

    OpenZeppelin's Audit of BarnBrige Smart Yield Bonds
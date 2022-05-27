Flash minting can be used to redeem fyDAI: The flash-minting feature from the fyDAI token can be used to redeem an arbitrary amount of funds from a mature token.

    Recommendation: Short term, disallow calls to redeem in the YDai and Unwind contracts during flash minting. Long term, do not include operations that allow any user to manipulate an arbitrary amount of funds, even if it is in a single transaction. This will prevent attackers from gaining leverage to manipulate the market and break internal invariants.

    Medium Risk severity finding from ToB’s Audit of Yield Protocol
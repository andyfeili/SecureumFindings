Potential resource exhaustion by external calls performed within an unbounded loop: DydxFlashLoanAbstraction._requestFlashLoan performs external calls in a potentially-unbounded loop. Depending on changes made to DyDx’s SoloMargin, this may render this flash loan provider prohibitively expensive. In the worst case, changes to SoloMargin could make it impossible to execute this code due to the block gas limit.

    Recommendation: Reconsider or bound the loop

    ConsenSys's Audit of Growth DeFi
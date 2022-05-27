Unnecessary event emission: The popDebtFromQueue function of the AccountingEngine contract is emitting a useless event whenever someone tries to call it with a debtBlockTimestamp that has not been saved before.

    Recommendation: To simplify the code and prevent wastage of gas, avoid emitting unnecessary events.

    OpenZeppelin's Audit of GEB Protocol
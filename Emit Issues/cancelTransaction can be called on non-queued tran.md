cancelTransaction can be called on non-queued transaction: Without a transaction existence check in cancelTransaction, an attacker can confuse monitoring systems. cancelTransaction emits an event without checking that the transaction to be canceled exists. This allows a malicious admin to confuse monitoring systems by generating malicious events.

    Recommendation: Short term, check that the transaction to be canceled exists in cancelTransaction. This will ensure that monitoring tools can rely on emitted events. Long term, write a specification of each function and thoroughly test it with unit tests and fuzzing. Use symbolic execution for arithmetic invariants.

    ToB's Audit of Hermez Network
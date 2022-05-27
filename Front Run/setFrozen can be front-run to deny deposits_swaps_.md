setFrozen can be front-run to deny deposits/swaps: Currently, a Curve contract owner can use the setFrozen function to set the contract into a state that will block swaps and deposits. A contract owner could leverage this process to front-run transactions and freeze contracts before certain deposits or swaps are made; the contract owner could then unfreeze them at a later time.

    Recommendation: Short term, consider rewriting setFrozen such that any contract freeze will not last long enough for a malicious user to easily execute an attack. Alternatively, depending on the intended use of this function, consider implementing permanent freezes.

    ToB's Audit of DFX Finance
Switch modifier order: BPool functions often use modifiers in the following order: _logs_, _lock_. Because _lock_ is a reentrancy guard, it should take precedence over _logs_.

    Recommendation: Place _lock_ before other modifiers; ensuring it is the very first and very last thing to run when a function is called.

    ConsenSys's Audit of Balancer Finance
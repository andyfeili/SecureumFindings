Withdrawn Event Log Poisoning: Calling the withdraw() function will emit the Withdrawn event. No UNI tokens are required as this function can be called with amount = 0 . As a result a user could continually call this function, creating a potentially infinite amount of events. This can lead to an event log poisoning situation where malicious external users spam the Unipool contract to generate arbitrary Withdrawn events.

    Recommendation: Consider adding a require or if statement preventing the withdraw() function from emitting the Withdrawn event when the amount variable is zero.

    Sigma Prime's Audit of Synthetix Unipool
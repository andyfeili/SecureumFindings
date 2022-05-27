Chainlink pricer is using a deprecated API: The Chainlink Pricer is currently using multiple functions from a deprecated Chainlink API such as latestAnswer() in L61, getTimestamp() in L74. These functions might suddenly stop working if Chainlink stopped supporting deprecated APIs.

    Recommendation: Consider refactoring these to use the latest Chainlink API.

    OpenZeppelin's Audit of Opyn Gamma Protocol
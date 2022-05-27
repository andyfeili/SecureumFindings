Kyber getRates code is unclear: Function names don’t reflect their true functionalities, and the code uses some undocumented assumptions.

    Recommendation: Refactor the code to separate getting rate functionality with getSellRate and getBuyRate. Explicitly document any assumptions in the code ( slippage, etc).

    ConsenSys's Audit of DeFi Saver
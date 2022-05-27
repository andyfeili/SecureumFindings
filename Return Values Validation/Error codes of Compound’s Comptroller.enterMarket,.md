Error codes of Compound’s Comptroller.enterMarket, Comptroller.exitMarket are not checked: Compound’s enterMarket/exitMarket functions return an error code instead of reverting in case of failure. DeFi Saver smart contracts never check for the error codes returned from Compound smart contracts.

    Recommendation: Caller contract should revert in case the error code is not 0

    Major severity finding from Consensys Diligence Audit of Defi Saver
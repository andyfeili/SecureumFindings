System always assumes USDC is equivalent to USD: Throughout the system, assimilators are used to facilitate the processing of various stablecoins. However, the UsdcToUsdAssimilator’s implementation of the getRate method does not use the USDC-USD oracle provided by Chainlink; instead, it assumes 1 USDC is always worth 1 USD. A deviation in the exchange rate of 1 USDC = 1 USD could result in exchange errors.

    Recommendation: Short term, replace the hard-coded integer literal in the UsdcToUsdAssimilator’s getRate method with a call to the relevant Chainlink oracle, as is done in other assimilator contracts. Long term, ensure that the system is robust against a decrease in the price of any stablecoin.

    Medium Risk severity finding from ToB’s Audit of DFX Finance
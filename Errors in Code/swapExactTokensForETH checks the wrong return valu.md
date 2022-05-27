swapExactTokensForETH checks the wrong return value: Instead of checking that the amount of tokens received from a swap is greater than the minimum amount expected from this swap, it calculates the difference between the initial receiver’s balance and the balance of the router

    Recommendation: Check the intended values

    Major severity finding from Consensys Diligence Audit of DAOfi
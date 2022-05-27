Underflow if TOKEN_DECIMALS are greater than 18: In latestAnswer(), the assumption is made that TOKEN_DECIMALS is less than 18.

    Recommendation: Add a simple check to the constructor to ensure the added token has 18 decimals or less

    ConsenSys's Audit of Aave CPM Price Provider
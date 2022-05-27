Tokens with more than 18 decimal points will cause issues: It is assumed that the maximum number of decimals for each token is 18. However uncommon, it is possible to have tokens with more than 18 decimals, as an example YAMv2 has 24 decimals. This can result in broken code flow and unpredictable outcomes

    Recommendation: Make sure the code won’t fail in case the token’s decimals is more than 18

    Major severity finding from Consensys Diligence Audit of Defi Saver
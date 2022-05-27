Summoner can steal funds using bailout: The bailout function allows anyone to transfer kicked user’s funds to the summoner if the user does not call safeRagequit (which forces the user to lose some funds). The intention is for the summoner to transfer these funds to the kicked member afterwards. The issue here is that it requires a lot of trust to the summoner on the one hand, and requires more time to kick the member out of the LAO.

    Recommendation: By implementing pull pattern for token transfers, kicked member won’t be able to block the ragekick and the LAO members would be able to kick anyone much quicker. There is no need to keep the bailout function.

    Major severity finding from Consensys Diligence Audit of The Lao
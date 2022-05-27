oToken can be created with a non-whitelisted collateral asset: A product consists of a set of assets and an option type. Each product has to be whitelisted by the admin using the whitelistProduct function from the Whitelist contract.

    Recommendation: Consider validating if the assets involved in a product have been already whitelisted before allowing the creation of oTokens.

    OpenZeppelin's Audit of Opyn Gamma Protocol
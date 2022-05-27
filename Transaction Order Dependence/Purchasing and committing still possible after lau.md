Purchasing and committing still possible after launch: Even after GenesisGroup.launch has successfully been executed, it is still possible to invoke GenesisGroup.purchase and GenesisGroup.commit.

    Recommendation: Consider adding validation in GenesisGroup.purchase and GenesisGroup.commit to make sure that these functions cannot be called after the launch.

    Critical severity finding from Consensys Diligence Audit of Fei Protocol
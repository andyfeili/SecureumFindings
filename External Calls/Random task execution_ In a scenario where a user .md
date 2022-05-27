Random task execution: In a scenario where a user takes a flash loan, _parseFLAndExecute() gives the flash loan wrapper contract (FLAaveV2, FLDyDx) the permission to execute functions on behalf of the user’s DSProxy. This execution permission is revoked only after the entire recipe execution is finished, which means that in case that any of the external calls along the recipe execution is malicious, it might call executeAction() back, i.e. Reentrancy Attack, and inject any task it wishes (e.g. take user’s funds out, drain approved tokens, etc)

    Recommendation: A reentrancy guard (mutex) should be used to prevent such attack

    Critical severity finding from Consensys Diligence Audit of Defi Saver
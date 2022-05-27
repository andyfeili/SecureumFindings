Owner can front-run traders by updating adapters: MetaSwap owners can front-run users to swap an adapter implementation. This could be used by a malicious or compromised owner to steal from users. Because adapters are DELEGATECALL’ed, they can modify storage. This means any adapter can overwrite the logic of another adapter, regardless of what policies are put in place at the contract level. Users must fully trust every adapter because just one malicious adapter could change the logic of all other adapters.

    Recommendation: At a minimum, disallow modification of existing adapters. Instead, simply add new adapters and disable the old ones.

    Medium severity finding from Consensys Diligence Audit of MetaSwap
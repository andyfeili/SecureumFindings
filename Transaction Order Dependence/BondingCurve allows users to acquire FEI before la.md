BondingCurve allows users to acquire FEI before launch: allocate can be called before genesis launch, as long as the contract holds some nonzero PCV. By force-sending the contract 1 wei, anyone can bypass the majority of checks and actions in allocate, and mint themselves FEI each time the timer expires.

    Recommendation: Prevent allocate from being called before genesis launch

    Medium severity finding from Consensys Diligence Audit of Fei Protocol
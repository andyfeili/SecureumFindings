Delegate assignment front-running: Any member can front-run another member’s delegateKey assignment. If you try to submit an address as your delegateKey, someone else can try to assign your delegate address to themselves. While incentive of this action is unclear, it’s possible to block some address from being a delegate forever.

    Recommendation: Make it possible for a delegateKey to approve delegateKey assignment or cancel the current delegation. Commit-reveal methods can also be used to mitigate this attack.

    Medium severity finding from Consensys Diligence Audit of The Lao
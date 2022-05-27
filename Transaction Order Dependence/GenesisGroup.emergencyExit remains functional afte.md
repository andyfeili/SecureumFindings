GenesisGroup.emergencyExit remains functional after launch: emergencyExit is intended as an escape mechanism for users in the event the genesis launch method fails or is frozen. emergencyExit becomes callable 3 days after launch is callable. These two methods are intended to be mutually-exclusive, but are not: either method remains callable after a successful call to the other. This may result in accounting edge cases.

    Recommendation: 1) Ensure launch cannot be called if emergencyExit has been called 2) Ensure emergencyExit cannot be called if launch has been called

    Medium severity finding from Consensys Diligence Audit of Fei Protocol
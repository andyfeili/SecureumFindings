Actions not executed atomically might lead to inconsistent state: The setAssetPricer, setLockingPeriod, and setDisputePeriod functions of the Oracle contract execute actions that are always expected to be performed atomically. Failing to do so can lead to inconsistent states in the system.

    Recommendation: Consider implementing an additional function that calls the setAssetPricer, setLockingPeriod, and setDisputePeriod functions, so that these actions can be executed atomically in a single transaction.

    OpenZeppelin's Audit of Opyn Gamma Protocol
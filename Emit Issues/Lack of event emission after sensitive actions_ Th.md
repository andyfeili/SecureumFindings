Lack of event emission after sensitive actions: The _getLatestFundingRate function of the FundingRateApplier contract does not emit relevant events after executing the sensitive actions of setting the fundingRate, updateTime and proposalTime, and transferring the rewards.

    Recommendation: Consider emitting events after sensitive changes take place, to facilitate tracking and notify off-chain clients following the contract’s activity.

    Medium Risk severity finding from OpenZeppelin’s Audit of UMA Phase 4
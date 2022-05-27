Voting period and quorum can be set to zero: When the Governance contract is initialized, the values of votingPeriod and votingQuorum are checked to make sure that they are greater than 0. However, the corresponding setter functions setVotingPeriod and setVotingQuorum allow these variables to be reset to 0. Setting the votingPeriod to zero would cause spurious proposals that cannot be voted. Setting the quorum to zero is worse because it would allow proposals with 0 votes to be executed.

    Recommendation: Consider adding the validation to the setter functions

    Medium Risk severity finding from OpenZeppelin’s Audit of Audius
The quorum requirement can be trivially bypassed with sybil accounts: While the final vote on a proposal is determined via a token-weighted vote, the quorum check in the evaluateProposalOutcome function can be trivially bypassed by splitting one’s tokens over multiple accounts and voting with each of the accounts. Each of these sybil votes increases the proposals[_proposalId].numVotes variable. This means anyone can make the quorum check pass.

    Recommendation: Consider measuring quorum size by the percentage of existing tokens that have voted, rather than the number of unique accounts that have voted.

    High Risk severity finding from OpenZeppelin’s Audit of Audius
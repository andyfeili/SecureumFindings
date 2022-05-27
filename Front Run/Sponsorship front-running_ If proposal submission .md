Sponsorship front-running: If proposal submission and sponsorship are done in 2 different transactions, it’s possible to front-run the sponsorProposal function by any member. The incentive to do that is to be able to block the proposal afterwards.

    Recommendation: Pull pattern for token transfers will solve the issue. Front-running will still be possible but it doesn’t affect anything.

    Major severity finding from Consensys Diligence Audit of The Lao
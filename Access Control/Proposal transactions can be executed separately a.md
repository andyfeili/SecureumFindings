Proposal transactions can be executed separately and block Proposal.execute call: Missing access controls in the Timelock.executeTransaction function allow Proposal transactions to be executed separately, circumventing the Governor.execute function.

    Recommendation: Short term, only allow the admin to call Timelock.executeTransaction

    High Risk severity finding from ToB’s Audit of Origin Dollar
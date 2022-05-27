Proposals could allow Timelock.admin takeover: The Governor contract contains special functions to let the guardian queue a transaction to change the Timelock.admin. However, a regular Proposal is also allowed to contain a transaction to change the Timelock.admin. This poses an unnecessary risk in that an attacker could create a Proposal to change the Timelock.admin.

    Recommendation: Short term, add a check that prevents setPendingAdmin to be included in a Proposal

    High Risk severity finding from ToB’s Audit of Origin Dollar
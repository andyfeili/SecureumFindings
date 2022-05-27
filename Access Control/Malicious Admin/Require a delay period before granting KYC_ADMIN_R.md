Require a delay period before granting KYC_ADMIN_ROLE  Acknowledged: The KYC Admin has the ability to freeze the funds of any user at any time by revoking the KYC_MEMBER_ROLE. The trust requirements from users can be decreased slightly by implementing a delay on granting this ability to new addresses. While the management of private keys and admin access is outside the scope of this review, the addition of a time delay can also help protect the development team and the system itself in the event of private key compromise.

    Recommendation: Use a TimelockController as the KYC_DEFAULT_ADMIN of the eRLC contract

    ConsenSys's Audit of eRLC
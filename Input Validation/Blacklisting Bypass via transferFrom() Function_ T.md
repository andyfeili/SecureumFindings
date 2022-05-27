Blacklisting Bypass via transferFrom() Function: The transferFrom() function in the TokenImpl contract does not verify that the sender (i.e. the from address) is not blacklisted. As such, it is possible for a user to allow an account to spend a certain allowance regardless of their blacklisting status.

    Recommendation: At present the function transferFrom() uses the notBlacklisted(address) modifier twice, on the msg.sender and to addresses. The notBlacklisted(address) modifier should be used a third time against the from address.

    High Risk severity finding from Sigma Prime's Audit of InfiniGold
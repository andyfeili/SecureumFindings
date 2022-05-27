Token Overflow might result in system halt or loss of funds: If a token overflows, some functionality such as processProposal, cancelProposal will break due to SafeMath reverts. The overflow could happen because the supply of the token was artificially inflated to oblivion.

    Recommendation: We recommend to allow overflow for broken or malicious tokens. This is to prevent system halt or loss of funds. It should be noted that in case an overflow occurs, the balance of the token will be incorrect for all token holders in the system

    Major severity finding from Consensys Diligence Audit of The Lao
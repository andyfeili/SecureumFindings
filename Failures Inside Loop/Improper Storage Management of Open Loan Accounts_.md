Improper Storage Management of Open Loan Accounts: When loans are open, the associated account address gets added to the accountsWithOpenLoans array regardless of whether the account already has a loan/is already included in the array. Additionally, it is possible for a malicious actor to create a denial of service condition exploiting the unbound storage array in accountsSynthLoans. 

    Recommendation: 1) Consider changing the storeLoan function to only push the account to the accountsWithOpenLoans array if the loan to be stored is the first one for that particular account ; 2) Introduce a limit to the number of loans each account can have.

    High Risk severity finding from Sigma Prime's Audit of Synthetix EtherCollateral
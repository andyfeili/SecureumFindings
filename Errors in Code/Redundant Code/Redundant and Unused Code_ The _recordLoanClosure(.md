Redundant and Unused Code: The _recordLoanClosure() function returns a boolean ( loanClosed ) which is never used by the calling function (see _closeLoan() , line [312]). Furthermore, since the _recordLoanClosure() function is only called via the _closeLoan() function, this means that synthLoan.timeClosed is always equal to zero (see require statement on line [305]). Therefore, the if statement on line [357] is redundant and unnecessary.

    Recommendation: 1) Using the return value of the _recordLoanClosure() function or changing the function definition to stop returning loanClosed 2) Removing the if statement in line [357]

    Sigma Prime's Audit of Synthetix EtherCollateral
Use delete to clear variables: The Controller contract sets a variable to the zero address in order to clear it. Similarly, the SetToken clears the locker by assigning the zero address.

    Recommendation: The delete key better conveys the intention and is also more idiomatic. Consider replacing assignments of zero with delete statements.

    OpenZeppelin's Audit of Set Protocol
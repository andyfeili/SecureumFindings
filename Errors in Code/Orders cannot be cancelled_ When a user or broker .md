Orders cannot be cancelled: When a user or broker calls cancelOrder, the cancelled mapping is updated, but this has no subsequent effects. In particular, validateOrderParam does not check if the order has been cancelled.

    Recommendation: Consider adding this check to the order validation to ensure cancelled orders cannot be filled.

    Critical Risk severity finding from OpenZeppelin’s Audit of MCDEX Mai Protocol
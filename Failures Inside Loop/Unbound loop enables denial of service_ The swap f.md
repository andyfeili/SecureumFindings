Unbound loop enables denial of service: The swap function relies on an unbounded loop. An attacker could disrupt swap operations by forcing the loop to go through too many operations, potentially trapping the swap due to a lack of gas.

    Recommendation: Bound the loops and document the bounds.

    Medium Risk severity finding from ToB’s Audit of Uniswap V3
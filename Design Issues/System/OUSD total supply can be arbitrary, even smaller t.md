OUSD total supply can be arbitrary, even smaller than user balances: The OUSD token contract allows users to opt out of rebasing effects. At that point, their exchange rate is “fixed”, and further rebases will not have an impact on token balances (until the user opts in).

    Recommendation: Short term, we would advise making clear all common invariant violations for users and other stakeholders. Long term, we would recommend designing the system in such a way to preserve as many commonplace invariants as possible.

    High Risk severity finding from ToB’s Audit of Origin Dollar
Lack of return value checks can lead to unexpected results: Several function calls do not check the return value. Without a return value check, the code is error-prone, which may lead to unexpected results.

    Recommendation: Short term, check the return value of all calls mentioned above. Long term, subscribe to Crytic.io to catch missing return checks. Crytic identifies this bug type automatically.

    High Risk severity finding from ToB’s Audit of Origin Dollar
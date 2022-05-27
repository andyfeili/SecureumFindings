safeApprove does not check return values for approve call: Although the Router contract uses OpenZeppelin’s SafeERC20 library to perform safe calls to ERC20’s approve function, the Orchestrator library defines its own safeApprove function. This function checks that a call to approve was successful but does not check returndata to verify whether the call returned true. In contrast, OpenZeppelin’s safeApprove function checks return values appropriately. This issue may result in uncaught approve errors in successful Curve deployments, causing undefined behavior.

    Recommendation: Short term, leverage OpenZeppelin’s safeApprove function wherever possible. Long term, ensure that all low-level calls have accompanying contract existence checks and return value checks where appropriate.

    ToB's Audit of DFX Finance
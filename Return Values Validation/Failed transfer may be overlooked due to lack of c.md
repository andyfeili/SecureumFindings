Failed transfer may be overlooked due to lack of contract existence check: Because the pool fails to check that a contract exists, the pool may assume that failed transactions involving destructed tokens are successful. TransferHelper.safeTransfer performs a transfer with a low-level call without confirming the contract’s existence. As a result, if the tokens have not yet been deployed or have been destroyed, safeTransfer will return success even though no transfer was executed.

    Recommendation: Short term, check the contract’s existence prior to the low-level call in TransferHelper.safeTransfer. Long term, avoid low-level calls.

    High Risk severity finding from ToB’s Audit of Uniswap V3
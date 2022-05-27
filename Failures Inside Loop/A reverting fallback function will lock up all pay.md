A reverting fallback function will lock up all payouts: In BoxExchange.sol, the internal function _transferEth() reverts if the transfer does not succeed. The _payment() function processes a list of transfers to settle the transactions in an ExchangeBox. If any of the recipients of an ETH transfer is a smart contract that reverts, then the entire payout will fail and will be unrecoverable.

    Recommendation: 1) Implement a queuing mechanism to allow buyers/sellers to initiate the withdrawal on their own using a ‘pull-over-push pattern.’ 2) Ignore a failed transfer and leave the responsibility up to users to receive them properly.

    Critical severity finding from Consensys Diligence Audit of Lien Protocol
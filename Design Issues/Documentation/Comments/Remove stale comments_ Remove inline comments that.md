Remove stale comments: Remove inline comments that suggest the two uint256 values DAOfiV1Pair.reserveBase and DAOfiV1Pair.reserveQuote are stored in the same storage slot. This is likely a carryover from the UniswapV2Pair contract, in which reserve0, reserve1, and blockTimestampLast are packed into a single storage slot.

    Recommendation: Remove stale comments

    ConsenSys's Audit of DAOfi
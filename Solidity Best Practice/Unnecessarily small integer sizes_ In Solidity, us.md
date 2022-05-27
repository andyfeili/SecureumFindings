Unnecessarily small integer sizes: In Solidity, using integers smaller than 256 bits tends to increase gas costs because the Ethereum Virtual Machine must perform additional operations to zero out the unused bits. This can be justified by savings in storage costs in some scenarios, however, that is not generally the case in this codebase.

    Recommendation: Consider using integers of size 256 bits to improve gas efficiency and mitigate function reverts.

    OpenZeppelin's Audit of Fei Protocol
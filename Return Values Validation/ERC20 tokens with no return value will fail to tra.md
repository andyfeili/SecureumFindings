ERC20 tokens with no return value will fail to transfer: Although the ERC20 standard suggests that a transfer should return true on success, many tokens are non-compliant in this regard. In that case, the .transfer() call here will revert even if the transfer is successful, because solidity will check that the RETURNDATASIZE matches the ERC20 interface.

    Recommendation: Consider using OpenZeppelin’s SafeERC20

    Major severity finding from Consensys Diligence Audit of bitbank
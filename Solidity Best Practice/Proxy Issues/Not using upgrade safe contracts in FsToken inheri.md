Not using upgrade safe contracts in FsToken inheritance: The FsToken contract is intended to be an upgradeable contract, used behind a proxy (namely, the FsTokenProxy contract). However, the contracts ERC20Snapshot, ERC20Mintable and ERC20Burnable in the inheritance chain of FsToken are not imported from the upgrade safe library @openzeppelin/contracts-ethereum-package but instead from @openzeppelin/contracts.

    Recommendation: Use the upgrades safe library in this case will ensure the inheritance from Initializable and the other contracts is always linearized as expected by the compiler.

    Medium Risk severity finding from OpenZeppelin’s Audit of Futureswap V2
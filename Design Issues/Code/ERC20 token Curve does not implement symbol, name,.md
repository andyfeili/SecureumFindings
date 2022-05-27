ERC20 token Curve does not implement symbol, name, or decimals: Curve.sol is an ERC20 token and implements all six required ERC20 methods: balanceOf, totalSupply, allowance, transfer, approve, and transferFrom. However, it does not implement the optional but extremely common view methods symbol, name, and decimals.

    Recommendation: Short term, implement symbol, name, and decimals on Curve contracts. Long term, ensure that contracts conform to all required and recommended industry standards.

    ToB's Audit of DFX Finance
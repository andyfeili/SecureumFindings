Variable shadowing from OUSD to ERC20: OUSD inherits from ERC20, but redefines the _ allowances and _ totalSupply state variables. As a result, access to these variables can lead to returning different values.

    Recommendation: Remove the shadowed variables (_ allowances and _ totalSupply) in OUSD.

    ToB's Audit of Origin Dollar
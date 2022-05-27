Named return variables: There is an inconsistent use of named return variables across the entire codebase. 

    Recommendation: Consider removing all named return variables, explicitly declaring them as local variables in the body of the function, and adding the necessary explicit return statements where appropriate. This should favor both explicitness and readability of the project.

    OpenZeppelin's Audit of HoldeFi
Document potential edge cases for hook receiver contracts: The functions withdrawTokenAndCall() and withdrawTokenAndCallOnBehalf() make a call to a hook contract designated by the owner of the withdrawing stealth address. There are very few constraints on the parameters to these calls in the Umbra contract itself. Anyone can force a call to a hook contract by transferring a small amount of tokens to an address that they control and withdrawing these tokens, passing the target address as the hook receiver. 

    Recommendation: Developers of these UmbraHookReceiver contracts should be sure to validate both the caller of the tokensWithdrawn() function and the function parameters.

    ConsenSys's Audit of Umbra
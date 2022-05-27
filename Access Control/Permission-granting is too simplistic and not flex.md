Permission-granting is too simplistic and not flexible enough: The Yield Protocol contracts implement an oversimplified permission system that can be abused by the administrator. The Yield Protocol implements several contracts that need to call privileged functions from each other. However, there is no way to specify which operation can be called for every privileged user. All the authorized addresses can call any restricted function, and the owner can add any number of them. Also, the privileged addresses are supposed to be smart contracts; however, there is no check for that. Moreover, once an address is added, it cannot be deleted.

    Recommendation: Rewrite the authorization system to allow only certain addresses to access certain functions

    ToB's Audit of Yield Protocol 
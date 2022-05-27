Test and production constants in the same codebase: The CoreOrchestrator contract defines the TEST_MODE boolean variable which is used to define several constants in the system. This decreases legibility of production code, and makes the system’s integral values more error-prone. 

    Recommendation: Consider having different environments for production and testing, with different contracts.

    OpenZeppelin's Audit of Fei Protocol
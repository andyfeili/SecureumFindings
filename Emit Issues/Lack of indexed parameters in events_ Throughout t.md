Lack of indexed parameters in events: Throughout the Holdefi’s codebase, none of the parameters in the events defined in the contracts are indexed.

    Recommendation: Consider indexing event parameters to avoid hindering the task of off-chain services searching and filtering for specific events.

    OpenZeppelin's Audit of HoldeFi
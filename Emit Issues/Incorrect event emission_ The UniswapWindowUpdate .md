Incorrect event emission: The UniswapWindowUpdate event of the UniswapAnchoredView contract is currently being emitted in the pokeWindowValues function using incorrect values. In particular, as it is being emitted before relevant state changes are applied to the oldObservation and newObservation variables, the data logged by the event will be outdated.

    Recommendation: Consider emitting the UniswapWindowUpdate event after changes are applied so that all logged data is up-to-date.

    Medium Risk severity finding from OpenZeppelin’s Audit of Compound Open Price Feed – Uniswap Integration
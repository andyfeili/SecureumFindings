Assimilators use a deprecated Chainlink API: The old version of the Chainlink price feed API (AggregatorInterface) is used throughout the contracts and tests. For example, the deprecated function latestAnswer is used. This function is not present in the latest API reference (AggregatorInterfaceV3). However, it is present in the deprecated API reference. In the worst-case scenario, the deprecated contract could cease to report the latest values, which would very likely cause liquidity providers to incur losses.

    Recommendation: Use the latest stable versions of any external libraries or contracts leveraged by the codebase

    Undetermined Risk severity finding from ToB’s Audit of DFX Finance
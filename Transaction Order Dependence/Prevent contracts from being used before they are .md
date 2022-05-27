Prevent contracts from being used before they are entirely initialized: Many contracts allow users to deposit / withdraw assets before the contracts are entirely initialized, or while they are in a semi-configured state. Because these contracts allow interaction on semi-configured states, the number of configurations possible when interacting with the system makes it incredibly difficult to determine whether the contracts behave as expected in every scenario, or even what behavior is expected in the first place.

    Recommendation: Prevent contracts from being used before they are entirely initialized

    ConsenSys's Audit of Growth DeFi
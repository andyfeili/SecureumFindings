Timed.isTimeEnded returns true if the timer has not been initialized: Timed initialization is a 2-step process: 1) Timed.duration is set in the constructor 2) Timed.startTime is set when the method _initTimed is called. Before this second method is called, isTimeEnded() calculates remaining time using a startTime of 0, resulting in the method returning true for most values, even though the timer has not technically been started.

    Recommendation: If Timed has not been initialized, isTimeEnded() should return false, or revert

    Medium severity finding from Consensys Diligence Audit of Fei Protocol
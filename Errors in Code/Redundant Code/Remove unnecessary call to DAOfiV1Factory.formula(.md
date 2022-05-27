Remove unnecessary call to DAOfiV1Factory.formula(): The DAOfiV1Pair functions initialize(), getBaseOut(), and getQuoteOut() all use the private function _getFormula(), which makes a call to the factory to retrieve the address of the BancorFormula contract. The formula address in the factory is set in the constructor and cannot be changed, so these calls can be replaced with an immutable value in the pair contract that is set in its constructor.

    Recommendation: Remove unnecessary calls

    ConsenSys's Audit of DAOfi 
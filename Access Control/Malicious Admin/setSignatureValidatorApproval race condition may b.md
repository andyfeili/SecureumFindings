setSignatureValidatorApproval race condition may be exploitable: If a validator is compromised, a race condition in the signature validator approval logic becomes exploitable. The setSignatureValidatorApproval function (Figure 4.1) allows users to delegate the signature validation to a contract. However, if the validator is compromised, a race condition in this function could allow an attacker to validate any amount of malicious transactions.

    Recommendation: Short term, document this behavior to make sure users are aware of the inherent risks of using validators in case of a compromise. Long term, consider monitoring the blockchain using the SignatureValidatorApproval events to catch front-running attacks.

    Medium Risk severity finding from ToB’s Audit of 0x Protocol
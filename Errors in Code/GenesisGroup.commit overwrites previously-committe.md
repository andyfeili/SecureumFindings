GenesisGroup.commit overwrites previously-committed values: The amount stored in the recipient’s committedFGEN balance overwrites any previously-committed value. Additionally, this also allows anyone to commit an amount of “0” to any account, deleting their commitment entirely.

    Recommendation: Ensure the committed amount is added to the existing commitment.

    Critical severity finding from Consensys Diligence Audit of Fei Protocol
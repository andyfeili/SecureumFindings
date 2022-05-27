Owners can never be removed: The intention of setOwners() is to replace the current set of owners with a new set of owners. However, the isOwner mapping is never updated, which means any address that was ever considered an owner is permanently considered an owner for purposes of signing transactions.

    Recommendation: In setOwners_(), before adding new owners, loop through the current set of owners and clear their isOwner booleans

    Critical finding in ConsenSys's Audit of Paxos
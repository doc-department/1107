# Proof of resources

Proof of storage in the SAFE Network uses a mechanism similar to a [zero knowledge proof](http://en.wikipedia.org/wiki/Zero-knowledge_proof). In this case the check does not require to know the content of any data to be checked, but must know the data is in fact held and held in a manner that is accurate.

This is achieved with the following steps:

1. A checking group of Vaults creates a random string
2. This random string is sent, encrypted to all holders of the data
3. The data holder takes this string and appends to the original data and hashes the result
4. The result is collected and decrypted at the checking group and compared
5. If any Vault returns a different result then it is believed compromised and de-ranked

This mechanism triggers on Get requests and during account transfers. It is non-deterministic and randomised by use by users.

It is considered to be secure and uses zero knowledge, not to conceal content (as anyone can ask for any data), but to ensure any data with a contamination is not required to be transferred.

# Self Encryption

The process of self encryption is vitally important to the secure storage and transmission of data on the SAFE network. The open architecture of the network requires that data be unrecognisable as data and resistant to decryption (even in the event of an encryption algorithm being compromised) to provide users with anonymity and security. The reasons of the self encryption process used in MaidSafe are plentiful, but include

1. The data is to be stored on consumer computers. Any data recognisable as illegal or immoral would be a disincentive to use the system.
2. As the data is being stored in a public and hostile environment, then it may be kept for a long period of time. An attacker, for instance, could keep some data encrypted, hoping for an attack on any encryption algorithm, then decrypt the file.
3. To efficiently store data on a global network, [data deduplication](http://en.wikipedia.org/wiki/Data_deduplication) is a side effect that can maximise space required to store all data. In essence to store X GB will take up only a % of X GB on the network.
4. As data has to be encrypted then the encryption keys should be deduced securely from the data itself, otherwise keys need to be hard coded, or users of the system need to type in passwords continually (there are of course alternatives to make this simpler).

An overview of the process is shown in this diagram

![Figure 1-1](./img/self-encryption.png)


###Notes

As the mechanism used is a variant on [convergent encryption](http://en.wikipedia.org/wiki/Convergent_encryption), it would be possible to recognise data if an attacker had the original file. This depends on access to the data, which in itself is an issue MaidSafe seeks to resolve. In the MaidSafe network physical security is also an important issue.

This requires that the network itself locate the data and make access to this extremely difficult if not actually computationally infeasible. In terms of access, MaidSafe refuses range based searches on data stored per vault. A user would have to obtain physical access to a vault to check the encrypted elements stored.

If this is still not enough security then there is the possibility of users altering files slightly to mask data. There is no link between consumers of data and the data itself in any case. User ID's, login ID's and data manipulation ID's are in fact different cryptographic identities and routing objects. This enforces a physically secure store of data.

###Use in a decentralised network

In a [Distributed Hash Table](http://en.wikipedia.org/wiki/Distributed_hash_table) like MaidSafe, this encryption scheme proves to be invaluable. As stated, the de-duplication aspect is efficient, but the issues surrounding convergent encryption are also mitigated to an extent. In such a network the IP address and port are removed from any Get request for data as well as the ID of the node that held that data. This means the network effectively masks where data is stored and where it comes from.

##Detailed description

Details of the encryption process can be found [here](https://github.com/maidsafe/MaidSafe-Encrypt/wiki/Documentation)


# Guaranteed Vault identification
Vault identification is essential if Vaults are to be responsible in a measured way for resource management.

Without identification any Vault can impersonate another. There are known methods to identify digital identities, such as a certificate authority (such as Verisign) or in some cases a web of trust. As this network has no servers, no human involvement and no trust, neither of these options are suitable.

The Vault identification process involves creating two key pairs. One key pair is a revocation key and is used only to create and invalidate a real key.

The real key pair is created and the public key is signed by the revocation private key and this packet (public key plus signature) is stored on the network as a Vault Identification key type. This key is stored in the location close to the Hash (SHA512) of the packet. This Hash is then used as the Vault identity.

The SAFE Network can retrieve this identification packet on request from any Vault. The only way to alter this packet is by a message signed by the same ID as the one that signed the packet.

This process allows Vaults to be identified as they advertise themselves as the hash of the identification packet that they created and stored.

As only the creator has the private key of this public key contained in the identification packet then we can assume this is the correct Vault. All messages are encrypted with this ID in any case, so fraudulent Vaults would not be able to decrypt such messages, including connect requests which are required to join the network.

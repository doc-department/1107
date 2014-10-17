# Vaults
A vault is small piece of local resource on a user's PC, for example, their hard-drive. Each vault fulfils multiple functions as part of the SAFE Network. Their primary role is the storage of encrypted data that has been passed to it from other vaults around the network.

Another function, or persona, of a vault is to manage other vaults. As chunks of data are passed between vaults the manager part of the vault detects and monitors data integrity.

Vaults can have a transaction manager or transaction validator persona. These personas are used for managing safecoin transfers.

Vaults know nothing of the data they have been asked to store (it can only be decrypted by the client) and because the data is only a small chunk, it is not possible to decipher what the original source data was, for example, a document or communications.

For every vault that holds data there are at least another four more vaults holding the same data. This means that if a vault goes offline or a data chunk becomes corrupted, that data is not lost. Each vault automatically finds another vault to store the data.

Vaults are not visible to the users of the SAFE Network. Instead the user only sees a virtual mounted drive on their PC. With the vaults constantly talking to, and monitoring each other, a user accesses data instantaneously from the mounted drive.

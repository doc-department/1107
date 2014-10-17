# Vault
Vaults are created on a user's PC when they install the MaidSafe client and join the SAFE Network.

The Vault on the user's PC can not be seen by the user. Instead the user sees a virtual mounted hard-drive that provides access to their distributed data.

When a user creates or alters files on their virtual drive, the file goes through several processes to ensure the file is secure and makes best use of the SAFE Network resources.

The file is first encrypted and broken up into chunks as part of the self authentication process. These chunks are then passed to Client managers. A Client manager is another Vault but with a different persona. From the Client managers the Data managers, again another Vault with a different persona, takes the chunks of encrypted data and distributes these around at least another four Data holders, another Vault persona.

The Data holder Vaults are checked by the Data holder managers. The Data holder managers constantly check the status of the Data holders. They report to the Data manager if any of the chunks are corrupted or changed. They also report when a Data holder has gone offline.

If a Data holder manager has reported a Data holder has gone offline, the Data manager decides, based on rankings assigned to Vaults, into which other Vault to put the chunk of data.

This way the chunks of data from the original file are constantly being monitored and supported to ensure the original data can be accessed and decrypted by the original user.

Any movement of data chunks can only be made if there is a consensus from the surrounding Vaults. Each chunk of data has to be validated before it is passed to another Vault.

Finally to ensure security and resilience, Vaults are non-geographically located using an exclusive OR (XOR) function.


[Click here to see a short video on how Vaults work](https://www.youtube.com/watch?v=txvKSeCaEP0)

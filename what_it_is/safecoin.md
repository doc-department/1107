#Safecoins

Safecoin can be earned, traded or purchased. The value of safecoins is determined by the demand for them.

Safecoins are used to access services on the SAFE Network. This encourages constant reuse which results in increasing demand for a finite resource. As a result the value of the safecoins increases over time.

While the coins themselves increase in value, the amount of network services (resources) they buy also increases. This is managed by the Proof of Resource algorithm.


## Safecoin transfer mechanism
On the SAFE Network, Vaults assume various personas or roles, depending on the requests they receive.  For example, the Data manager persona is responsible for managing the integrity and availability of a given piece of data on the network. A separate persona, the Transaction manager, handles all the safecoin transactions.

A Transaction manager group is a trusted group of Vaults which are closest to any given transaction identity. The Transaction manager is responsible for the logic that enables transactions to be completed.

The transaction is open and is read-only to public. This allows an upper layer third party broker app to validate that the transaction is happening or completed.


The procedure of a transfer of credit from **user_A** to **user_B** can be illustrated as follows:

1.	**User_A** contacts the SAFE Network using the instruction ***[user_A.Transfer(user_B, amount, wallet)]***
2.	When the Transaction manager group of **user_A** receives a request, it does the following:

    i)    Debit the amount from **user_A's** wallet

    ii)   Send a request to the Transaction manager

    iii)  Send a notification to the Transaction validator (escrow)

3.	When the Transaction manager group receives a notification, it does the following:

    i)    Send a notification to **user_B's** Vault

    ii)   Create an internal transaction
4.	When **user_B's** Transaction manager group receives a valid notification, it does the following:

    i)    Send an acknowledgement to the Transaction manager group

    ii)   Credit **user_B's** wallet with the amount

![Transfer Mechanism](https://raw.githubusercontent.com/maidsafe/Whitepapers/master/resources/transfer_mechanism_diagram.png)


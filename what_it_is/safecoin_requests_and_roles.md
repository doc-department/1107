# Safecoin requests and roles
Safecoins are another type of data and it has PUT and GET requests defined for it on the SAFE Network. However, unlike normal data, there is no DELETE request available.

The PUT request for safecoins has a "no duplication allowed". If there is already a safecoin with the same name (first 32 bits), the PUT request is rejected. This is handled by the Data manager receiving the request.

An EXCHANGE allows an approved requester to update the details of the safecoin but only if it follows these rules:

* The owner is approved by the majority of 3rd party Vaults (escrow) and owners (previous and current owners considered as approved themselves) can update all fields.
* Each escrow can only update their correspondent field once.
* Each time previous and current owner fields get updated, the safecoin version must be increased by one, and all escrow fields are erased.

The above rules are enforced by the Pmid manager holding the safecoin data. As the ownership field, together with the escrow fields, are used as a 'transaction', the Pmid manager effectively becomes the Transaction manager. In this instance, the safecoin data can also be considered as a receipt object as well.

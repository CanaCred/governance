# Ledger Access Policies

This is a Controlled Document of the Bedrock Governance Framework was approved by the Canadian Credential Network Board of Directors.

| Document Name |Canadian Credential Network Ledger Access Policies |
| --- | --- |
| Version | v0.9 |
| Approval Date | |
| Status | Pre-Launch Phase: Governance Framework Development |
| Governs | Policies for reading and writing to the Canadian Credential Network Utility|
| Governed By | Canadian Credential Network Governance Framework Workgroup |

## 1. Declaration of Intent
The Canadian Credential Network Utility (the "Utility") will operate with limited write access as specified by the Permissioned Write Access processing section declared herein.

The scope of these policies pertains to the full corpus of **Utility Environments**, namely all the ledgers associated with the Canadian Credential Network Utility (i.e.: Production, Staging, Testing).

## 2. Recommended Reading
The terms used in this Controlled Document are more fully explained in the [Glossary](../gf_info/glossary.md), as well as in the [Legal Architecture Overview](../gf_legal/legal_arch.md) which includes a visual diagram.

<!-- TODO:Work through Legal Architecture Overview -->

One topic pertinent to ledger access is the concept of a [Tombstone](https://jira.hyperledger.org/browse/INDY-2082). A Steward MAY, for regulatory or individual business requirements, determine that it needs to forbid access to a ledger entry and therefore require the ability to mark the subject entry as "deleted". While the Canadian Credential Network has taken action to minimize such risk by prohibiting public write access, a *Tombstone* provides an added protection mechanism that will help mitigate risk for Stewards who are contractually obligated to carry out read and write transactions.

**The Utility will allow for Tombstones once this feature is implemented in Hyperledger Indy**. The Canadian Credential Network will collaborate with the Hyperledger Indy Community and the [Canacred Wallet Project](https://github.com/bedrock-consortium/tsc/) (the "Wallet Project") to allow a Steward to:

1. Mark a Transaction as "deleted" thereby suggesting it should no longer be returned in response to requests for read access.
2. Declare a Transaction as "deleted" under one of two categories: *Node-Specific Tombstone* or a *Ledger-Wide Tombstone*.

Tombstones do not modify data on the ledger. Instead they impact the behavior of a Steward Node that serves data from the ledger. In the general, a Tombstone MAY be used by a Steward that is forced to comply with a legal demand to stop returning a specific Transaction, such as a Transaction containing data that is locally considered Personal Data or that is illegal or violates the Transaction Author Agreement in some other way. In such a case, other Stewards may not face the same legal demands and may take different action.

### 1. Transaction Author Agreement
1. The Canadian Credential Network MUST:
	1. Publish a Transaction Author Agreement between a Transaction Author and the Canadian Credential Network (representing the Canadian Credential Network Utility as a whole) specifying the terms and conditions under which Transaction Authors agree to submit write Transactions to the Utility, including the policies defined in this Controlled Document.
	1. Publish a Steward Data Processing Agreement (DPA) specifying the requirements for a Steward to serve as a Data Processor on behalf of Transaction Authors as Data Controllers and the Canadian Credential Network as a Designated Data Controller.
	1. When necessary, revise the Transaction Author Agreement and the Steward DPA under the same policies as a Controlled Document as specified in the ```Governance``` section of the Canadian Credential Network Governance Framework Master Document.
	1. Maintain a published version of the Transaction Author Agreement and the Steward DPA in the [Canadian Credential Network Code Repository](https://github.com/bedrock-consortium/bbu-gf/).
2. A Transaction Author MUST agree not to submit Transactions that contain:
	1. Data that would violate the intellectual property rights of others.
	1. Data that may not lawfully be written to the Utility, where the definition of applicable law in this context is provided in the Transaction Author Agreement.
3. A Transaction Author MUST agree not to submit a Transaction that contains Personal Data.
4. A Transaction Author MUST agree that if it is determined in a court of law that one or more Transactions made by the Transaction Author violated the terms and conditions of the Transaction Author Agreement, the Transaction Author consents to the marking of those Transactions with a Tombstone and, if possible, the revocation of the State Proof(s) pertaining to the Utility data for those Transactions.

### 2. Transaction Endorser Agreement
1. The Canadian Credential Network MUST:
	1. Publish a Transaction Endorser Agreement between the Transaction Endorser and the Canadian Credential Network specifying the terms and conditions under which Transaction Endorsers agree to write Transactions to the Utility, including the policies defined in this Controlled Document.
	1. Publish a Transaction Endorser Data Processing Agreement (DPA) specifying the requirements for a Transaction Endorser to serve as a Data Processor on behalf of Transaction Authors as Data Controllers and the Canadian Credential Network as a Designated Data Controller.
	1. When necessary, revise the Transaction Endorser Agreement and the Transaction Endorser DPA under the same policies as a Controlled Document as specified in the ```Governance``` section of the Canadian Credential Network Governance Framework Master Document.
	1. Publish the current version of the Transaction Endorser Agreement and the Transaction Endorser DPA in the [Canadian Credential Network Code Repository](https://github.com/bedrock-consortium/bbu-gf/).
2. A Transaction Endorser MUST adhere to membership entitlements that constrain the number of transactions that may be submitted as specified in the Transaction Endorser Agreement.
3. A Transaction Endorser MUST:
	1. Only submit Transactions from Transaction Authors who have explicitly agreed to the Transaction Author Agreement by physically signing a copy.
	1. Maintain physical or digital evidence of conformance to this policy.

### 3. Permissioned Write Access
1. The scope of the policies defined in this section is defined as follows:
	1. The policies in this section MUST apply to all Utility Environments.
	1. The policies governing write access to non-production Utility Environments (i.e.: Staging, Testing) MAY be defined separately by other Controlled Documents.
2. Canadian Credential Network Trustees are permitted to write Transactions to the Utility under the following rules:
	1. 	This policy MUST apply only to Trustees acting in their role as Trustees of the Canadian Credential Network.
	1. 	A Trustee MUST only make the following Transactions if the Transaction has been approved by a motion of the Canadian Credential Network Board of Directors.
		1. 	Add or remove a Trustee.
		1. 	Add or remove a Steward.
		1. 	Add or remove a Transaction Endorser.
		1. 	Update or receive updates from the Membership Management System.
	1. 	A Trustee MAY make Utility maintenance Transactions if the Transaction is approved by either the Canadian Credential Network Board of Directors.
3. Canadian Credential Network members who are permitted to serve in the role of Transaction Endorsers MUST agree to the Transaction Endorser Agreement by submitting a physically or digitally signed copy to the Canadian Credential Network.
4. Transaction Authors are permitted to write Transactions to the Utility provided::
	1. Each Transaction includes a valid digital signature from the Transaction Author.
	1. The Transaction is endorsed by an approved Transaction Endorser.
	1. If the Transaction updates the state of a ledger-persisted data structure, it MUST be digitally signed by the same Transaction Author that recorded the previous state.

### 4. Public Write Access
1. Public Write Access is PROHIBITED.
2. All Utility Environments MUST adhere to Permissioned Write Access processing.

### 5. Public Read Access
1. The Utility MUST be publicly available for anyone to submit read transactions.
1. Stewards MUST provide public read access without cost for all Transactions on the Utility unless marked by a Tombstone.
1. Once Tombstone functionality has been:
	3. implemented by the underlying ledger technology,
	4. approved by the Canacred Technical Steering Committee, and
	5. approved by the Canadian Credential Network Board of Directors, a Steward MAY mark a Transaction as a Node-Specific Tombstone if:
		1. Requested by the Transaction Author of a Transaction for a valid reason as specified by the Transaction Author Agreement.
		1. Required of the Steward by a court order.
		1. The Steward has evidence that the Transaction violates the terms and conditions of the Transaction Author Agreement.
1. A Steward MUST NOT use a Node-Specific Tombstone for any other reason.
1. Ledger-Wide Tombstones MUST NOT be implemented until policies governing their usage are published in a future version of this Controlled Document.

NOTE: Ledger-Wide Tombstones are not planned in the near future.

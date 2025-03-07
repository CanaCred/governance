The concepts outlined herein provide an informational synopsis for the operation of the Canadian Credential Network Utility and participation in the Canadian Credential Network. The executable [BBU Participation Agreement](../gf_legal/contracts/bbu_participation_agreement.docx) (the "Participation Agreement"), specifically ```Exhibit B``` and ```Exhibit C```, supersedes this content.

## Utility Infrastructure Requirements
The Utility is an instance of a [ToIP Layer One Public Utility](https://github.com/hyperledger/aries-rfcs/tree/master/concepts/0289-toip-stack#layer-one-public-utilities-for-decentralized-identifiers-dids) based on [Hyperledger Indy](https://www.hyperledger.org/projects/hyperledger-indy) ("Indy"). In order to establish an operational budget for the Utility, several  infrastructure assumptions must be considered.

1. Budgetary requirements dictate how much revenue is required to keep the Utility sustainable.
2. Distributed ledger technologies, like Indy, leverage consensus algorithms that come with an optimal consensus threshold. This threshold value dictates the number of validator nodes required to operate the Utility. To meet the needs of a decentralized ledger, each validator node must be operated by an independent and unique participant. Therefore, a quantity requirement associated with one or more classes of members will be tied to the number of required validator nodes. Validator nodes may also be referred to as *utility infrastructure nodes* or *Stewards* from a historical [Sovrin Foundation](http://sovrin.org) context. See [Glossary](./glossary.md) for more details.

A balance between budget requirements and technology limitations will define the number of validator nodes required to operate the Utility. Initially this will be set at twenty-five (25) utility infrastructure nodes. The set of active nodes on the network will be periodically pulled from a pool of available nodes.

### Validator Node Pool
In order to efficiently operate the ledger associated with the Utility, a combination of production, test, and development environments are necessary. The Governing Board is responsible for defining the requirements associated with the validator pool. It is important to note that such Governing Board decisions will be influenced by both technical performance restrictions as well as budgetary demands.

| Framework Facet | Required Quantity | Comment |
| --- | --- | --- |
| Governing Board Seats | 7 | Minimum Governing Contributors. Governing Board seats can increase but MUST not exceed 15 |
| Minimum Production Pool Size  | 19 | Considers production and Governing Board factors. |
| Minimum Test Pool Size  | 3| Ledger used by Utility Service Provider and Wallet Project contributors.  |
| Minimum Development Pool Size | 3 | Ledger used by Utility Service Provider and Wallet Project contributors.|
| Minimum Total Pool Size | 25 | Considers requirements across all environments. |

### Steward Population Dynamics
The number of Board of Director seats SHOULD be consistent as the population of Stewards (Governing and Operational Contributors) increases.

| Board of Director Seats	| Required Stewards |	BoD%|
| --- | --- | --- |
|7	|25	|0.28|
|9	|36	|0.25|
|11	|44	|0.25|
|13	|52	|0.25|
|15	|60	|0.25|

The Governing Board maintains a **FIFO Waiting List** of Operational Contributors that have maintained consistent participation. Position on the waiting list is based upon date of membership of the Operational Contributor. This list shall be used to offer new Governing Board seats upon availability due to attrition or growth.

## Membership Types
Building on our [Glossary](./glossary.md), participants in the Canacred are referred to as *Trust Community Participants. These business entities agreed to participate in the *Trust Community* known as the Canadian Credential Network. Participation in the Canacred is possible via formal legal contracts or participation agreements.

### Annual Participation
Participation details herein provide a synopsis of the information outlined in "Exhibit B" and "Exhibit C" of the Canadian Credential Network Charter within the [Canadian Credential Network Participation Agreement](../gf_legal/contracts/bbu_partnership_agreement.docx) (the "Participation Agreement").

Private sector entities (businesses) can join and renew membership on an annual basis under three possible membership types:

| Participation Type | Validator Node Hosting Required | Required Governing Body Participation  | Authorized Endorser Privileges (Ledger Writes) |
| --- | --- | --- | --- |
| Governing Contributor | Yes - 1 | Yes - 1 Person Per Governing Body |Yes - Unlimited |
| Operational Contributor | Yes - 1 | Yes - 2 Persons |Yes - Unlimited |
| Contributors | No | No | Yes - Limited |

1. Governing Contributor:
    * **Description**: Contributors that are willing to help with the infrastructure, management, and financial needs of the Utility.
    * **Obligations**:
        1. MUST host one or more utility infrastructure *Validator Nodes* as defined in ```Exhibit C``` of the Participation Agreement.
        2. MUST sign the required Utility Agreements as set forth in ```Exhibit B``` of the Participation Agreement.
        3. MUST assign appropriately skilled resources, as detailed in ```Exhibit B``` of the Participation Agreement, that will meet the required commitments for the Governing Board, the Committees, additional committees or working groups established by the Directed Fund in the future, and the Wallet Project.
    * **Entitlements**:
        1. MAY appoint a representative on the Governing Board, provided, however, that a Utility Service Provider may not appoint a representative to the Governing Board.
        2. MAY appoint a representative to any Committee, provided that a Utility Service Provider may not appoint a representative to the Finance Committee.
        3. MAY act, pending signed Utility Agreements, as a Transaction Endorser.
        4. MAY write Transactions as a Transaction Endorser as defined in ```Exhibit C``` of the Participation Agreement.
    * **Restrictions**:
        1. Participation is limited to the number of Board of Director seats available.
        2. A FIFO waiting list is maintained by Governing Board to allow for new members to fill voids left by exiting members.
        3. Utility Service Providers MAY NOT be a Governing Contributor.
        4. Utility Service Providers MAY NOT participate in the Finance Committee.

    From 12 months after the inception of the Directed Fund, or from such other point in time as the Governing Board may decide, a new Member may join the Directed Fund as a Governing Contributor only if the total number of Governing Board Contributors (including the new Contributor in this count) is equal to or less than 25% of the total number of Stewards of the Utility (e.g., the total of Governing Contributors and Operational Contributors).  The Directed Fund will maintain a waiting list of Operational Contributors that wish to become Governing Contributors, and new Governing Contributors spots will be allocated according to seniority of Operational Contributors status among Operational Contributors on the waiting list.

2. Operational Contributor
    * **Description**: Contributors that are willing to help with the infrastructure, management, and financial needs of the Network. Minimally, this requires the contributor to contribute a *Validator Node* to the operation of the Ledger.
    * **Obligations**:
        1. MUST host one or more utility infrastructure *Validator Nodes* as defined in ```Exhibit C``` of the Participation Agreement.
        2. MUST sign the required Utility Agreements as set forth in ```Exhibit B``` of the Participation Agreement.
        3. MUST assign appropriately skilled resources, as detailed in ```Exhibit B``` of the Participation Agreement, that will meet the required commitments of at least one Committee and the Wallet Project.
    * **Entitlements**:
        1. MAY appoint a representative to any Committee.
        2. MAY act, pending signed Utility Agreements, as a Transaction Endorser.
        3. MAY write Transactions as a Transaction Endorser as defined in ```Exhibit C``` of the Participation Agreement.
        4. MAY request to be added to the Governing Contributor waiting list.
    * **Restrictions**:
        1. Participation is limited to the number of nodes required to maintain optimal consensus performance. The optimal limit here must take into consideration a balance with decentralization requirements. The Governing Board will annually determine the number of nodes required to meet both consensus, decentralization, and budgetary requirements.

3. Contributors
    * **Description**: Contributors that are willing to be responsible for the endorsement of transactions to the ledger.
    * **Entitlements**:
        1. MAY appoint a representative to any Committee.
        2. MAY act, pending signed Utility Agreements, as a Transaction Endorser.
        3. MAY write Transactions as a Transaction Endorser as defined in ```Exhibit C``` of the Participation Agreement.

4. All Members are entitled to:
    1. Participate in Directed Fund general meetings, initiatives, events and any other activities; and
    2. Identify themselves as members of the Canadian Credential Network Utility Fund supporting the Canadian Credential Network community.

### Participants and non-participants

1. Transaction Author
    * **Description**: Any entity that is the submitter of a write transaction in support of using the ledger for decentralized identity interactions.
    * **Obligations**:
        1. MUST sign the required *Transaction Author Agreement* as set forth in ```Exhibit B``` of the Participation Agreement.
        2. MAY interact with a *Transaction Endorser* for the processing of write requests to the ledger.
    * **Restrictions**:
        1. Can only submit those transaction types outlined in the [CCNU Constitution](https://github.com/CanaCred/governance/blob/master/docs/gf_info/masterdoc.md), specifically the [ledger access policies](../gf_controlled/ledger_access_policies.md) and [ledger data policies](../gf_controlled/ledger_data_policies.md).
    * **Entitlements**:
        1. Ability to use ledger for decentralized identity interactions.  

2. Contributors to the Wallet Project: Contributions to the Wallet Project are made pursuant to the terms of the Technical Charter for the Wallet Project.

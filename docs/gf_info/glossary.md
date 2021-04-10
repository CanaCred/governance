# Glossary 
## Foundational Glossaries

The Canadian Credential Network is working on a convergence of industry terms between several glossary efforts, namely:

* [PCTF Glossary Recommendation](https://diacc.ca/wp-content/uploads/2020/09/PCTF-Glossary-Final-Recommendation_V1.0.pdf)
* [Sovrin Glossary](https://docs.google.com/document/d/1gfIz5TT0cNp2kxGMLFXr19x1uoZsruUe_0glHst2fZ8)
* [TOIP Glossary]()

The contents herein are considered additional terms specific to the **Canadian Credential Network**.

>Note:

## Canacred Glossary missing terms and definitions

We will substitute term **member** with the term **participant**. We will have two types of **Participants**: **Contributors** - those with the write access and **Readers*** - those with the read access only.

Self-Certification, 

Certification or Accreditation, 

Participation Application Practices and Procedures, 

Identity Utility Administrator (Authorised Network Administrator), 

*Canacred Open Source Code*, 

Utility Service Provider, 

Hosting Provider,

Validator and Observer Nodes, 

*Crisis Management Plan*, 

Network Interface Controller, 

Diffuse Trust Principle, 

High Availability Principle, 

Transaction Author, 

Data Controller, 

Data Processor, 

FIFO Waiting [list](https://queue-it.com/queue-first-in-first-out/)

Trust Anchor

Registry

**?** Trust Mechanism

**?** Trust Author

## Abstract from  PCTF Glossary**:

The PCTF Glossary provides definitions and examples for terms that appear across DIACC PCTF documentation. The content of the PCTF Glossary is:
1. **Terms**–The words or phrases that appear frequently and that are used with a specific intent (i.e., not their everyday English meaning) in the PCTF documentation
2. **Definitions**–A statement that provides the accepted and precise meaning of the associated term in the PCTF context
3. **Examples**–Examples or non-examples may be included to help clarify the intended meaning of a term; the examples provided are not intended to be an exhaustive list.
4. **Synonyms**–Terms with same or similar meaning used in other communities of interest

## Terms from PCTF Glossary
### Entity
An entity is a thing with a distinct and independent existence such as a person, organization, or device that can be subject to legislation, policy, or regulations within a context, and which may have certain rights, duties, and obligations. An entity can perform one or more roles in the digital ecosystem. 
There are two types of entities: atomic entities and compound entities. An atomic entity is an entity that cannot be decomposed into smaller units. Persons are atomic entities. A compound entity is an entity that is comprised of one or more atomic entities. Organizations are compound entities.
### Relationship
A relationship is an association between two or more entities. The entities in the relationship can be any combination of atomic entities and compound entities. Relationships between entities must be differentiated from interactions between entities (i.e.,
transaction execution).

## Abstract from Bedrock Business Utility Glossary

### Steward
A general term for an organization that is responsible for providing and maintaining a portion of the infrastructure necessary to establish a public identity utility. Minimally, the organization must meet the requirements to be a member of the public identity utility and must operate at least one ```Node```.

### Node
A computer network server running an instance of the code necessary to operate a distributed ledger or blockchain. In the Canadian Credential Network, a Node is operated by a Steward running an instance of the Canacred Open Source Code to maintain the Canacred Network Utility ( or DID Ledger). A Node must be either a Validator Node or an Observer Node.

### Canacred Open Source Code
The computer software that is installed on all Nodes associated with the Canacred Network Utility (CCNU). This code determined by the Canacred Board of Directors. The CCNU adheres to code selection and version guidance provided by the Technical Steering Committee ("TSC") of the Canacred Wallet Project. The TSC collaborates within the Hyperledger Indy Project of the Linux Foundation to establish a TSC approved version of Hyperledger Indy within the the Canacred Code Repository managed by the TSC.

### Canacred Ledger Environments
The corpus of DID Ledgers used by the Canadian Credential Network to operate the Canacred Network Utility. For example: ```prod```, ```test```, and ```dev```.

### DID Namespace

Building on URI Standards, the DID Specification allows for both  root namespace (did:xxx) and sub-namespace (did:xxx:yyy) conventions.

### Governing Body

An organization or consortium that is responsible for the management of an Identity Utility Network.

### Backbone Network

A distinct system of domain specific ledgers operated by decentralized peer nodes and associated with a DID Namespace. Governed by its own governance framework. See also *Identity Utility Network*.

### Peer-Net (*Deprecated*)

A distinct system of domain specific ledgers operated by decentralized peer nodes and associated with a DID Namespace. Governed by its own governance framework. See also *Backbone Network*.

### Network of Networks

A decentralized collection of discoverable and interoperable Identity Utility Networks. The internet is an exemplar of a network of networks structure based on DNS and URI standards.

### DID Ledger
A distinct system of domain specific ledgers operated by decentralized peer nodes and associated with a DID Namespace.
See *Identity Utility Network (IUN)*

### Identity Utility Network (IUN)

A distinct system of domain specific ledgers operated by decentralized peer nodes and associated with a DID Namespace.
Preferably built on Hyperledger Indy, this ```DID Ledger```, is governed by an independent governing body and its own governance framework. Due to the overuse of terms such as "Network" and "Ledger", the term "Utility" has been accepted by the Canadian Credential Network to allow for additional clarity. See also *Backbone Network*.

### Remote Identity Utility (Remote IUN)

An Identity Utility Network associated with a DID Root Namespace that operates under its own Governance Framework.

### Decentralized DID Namespace Registry (DDNR)

Provides registration, discovery, and access for an Identity Utility Network.

### Identity Utility Administrator

See *Utility Service Provider*

### Utility Service Provider

The provider of operational and maintenance services for an Identity Utility Network.

### Trustee
An Identity Owner entrusted with specific identity control responsibilities by another Identity Owner or with specific governance responsibilities by a Governance Framework. See *Recovery Key Trustee*

### Consortium Trustee
A Trustee who is a member of the Canadian Credential Network Board of Directors. The trust in Consortium Trustees is bestowed collectively on behalf of all Identity Owners.

### Key Recovery
The process of recovering access to and control of a set of Private Keys—or an entire Wallet—after loss or compromise. Key Recovery is a major focus of the emerging DKMS standard for cryptographic key management. See also Recovery Key.

### Recovery Key
A special Private Key used for purposes of recovering a Wallet after loss or compromise. In the DKMS key management protocol, a Recovery Key may be cryptographically sharded for secret sharing among multiple Trustees.

### Recovery Key Trustee
A Trustee trusted by another Identity Owner to authorize sharing back a Recovery Key for purposes of restoring a Wallet after loss or compromise.

### Membership Management System
The means by which the Governing Board tracks membership entitlements and status. This MAY be implemented via a Salesforce tenant operated by the Linux Foundation with custom hooks into the Canacred Network Utility.

### Digital Trust Ecosystem
An interdependent group of enterprises, people and/or things that share a standardized trust model for mutually beneficial purposes, such as consumer and commercial interactions that are verifiable.

### CLI Private Key
The Private-Key used by a Steward when interacting with the Indy CLI.

### Validator Private Key
The Private-Key used by the Validator Node when performing concensus.



# Block Array White Paper

#### Version Information
#### Author:

Block Array Corporation

www.blockarray.com





----------
Table of Contents 


1. Abstract
  1. Overview
2. Overview of the Supply Chain Industry
  1. Problems
  2. Use Cases
  3. Solutions
    1. Blockchain Network
    2. Industry Specific Applications
    3. Infrastructure 
3. Ecosystem
  1. Goals
  2. Design Considerations
4. Blockchain Specifications
  1. Requirements
  2. Unique Implementations
  3. ARY Token
  4. Performance Benchmarks
5. Applications
  1. Trucking
  2. Logistics
  3. Data Analytics
  4. Insurance
  5. Retail
6. Roadmap
7. Corporate Information
  1. Overview
  2. Commercialization 
8. References 
9. Appendix


----------





this section left intentionally blank 






----------






copyright and disclaimer page






----------


# Abstract




----------


# Overview


Global operations need consistent global standards to be applied across their supply chain, and this is only going to become increasingly difficult with legacy enterprise systems and increased legal costs. Laws recently passed like The California Transparency Supply Chain Act or the Electronic Logging Data Mandate for Trucking add additional burdens to businesses trying to comply with the law, coupled with more demands on increasingly outdated IT systems - this then creates multiple problems for firms. 

Use Case Examples 


#### Electronic Logging Device Mandate

The Electronic Logging Device Mandate (ELD) is intended to help create a safer work environment for drivers, and make it easier and faster to accurately track, manage, and share records of duty status (RODS) data (FMCSA 2018). An ELD synchronizes with a vehicle engine to automatically record driving time, for easier, more accurate hours of service (HOS) recording.


  The ELD Mandate Includes provisions to help prevent data tampering and harassment of drivers.

What is the impact of this new law?


> Under Federal regulations, the motor carrier is responsible for training and monitoring its drivers to ensure compliance with Hours of Service rules.  Any driver violation may also be held against the carrier. Failing to establish an effective Hours of Service monitoring and compliance system can result in fines of thousands of dollars.  In extreme cases, motor carrier officials have even received jail sentences.

So any violation in failing to comply with this new law could mean 


Four Driver Status Modes
The choices of duty status when a property-carrying driver records his or her time on a record of duty status, or R.O.D.S

| off duty | sleeper berth | driving | on duty/not driving |



| Hours of Service Rules       |
| ---------------------------- |
| 10 hours off-duty            |
| 14-hour duty period          |
| 11 hours driving             |
| 30 minute break              |
| 60 hours/7-day on-duty limit |
| 70 hours/8-day on-duty limit |


Add to these rules are the burdensome additional regulations such as when


1. Once the duty period starts, it runs for 14 consecutive hours after which the driver may not drive a CMV again until having another 10 or more consecutive hours off-duty. Nothing stops the running of the 14 hour clock.


2. During the 14-hour duty period, which some people refer to as a “driving window,” you may drive a maximum of 11 hours.


3. When you reach a total of 60 on-duty hours in 7 days, you must have a period of at least 34 consecutive hours off duty. (There is an alternative available for carriers that operate every day of the week-- that is a maximum of 70 hours in 8 days.)


4. Requires an off-duty break at some point during the duty period. The rule says that you may not drive a CMV if it has been 8 or more hours since your last off-duty period of at least 30 minutes.


5. For every 5 duty periods that they return to their starting point, they may choose one 16-hour duty period.


6. The counting of the maximum 60 or 70 hours on duty restarts anytime a driver has at least 34 consecutive hours off duty.
                                                                                                        source: FMCSA 2018 

<explainer paragraph>




Distributor Cross Docking: This is where a distributor consolidates inbound products from various vendors into a mulit-SKU pallet, which is delivered as soon as the last product is received. Computer distributors often source components and consolidate them into one shipment in merge-in-transit centers before delivering them to the customer, and rarely have the same vendor for all the products. Think of a Desktop tower, a monitor, a keyboard, and mouse that are combined into one package at a cross-dock for delivery to the customer as a single package. 

Retail cross-docking: This involves the consolidation of shipments from different shippers and vendors to be sorted onto outbound trucks for different stores. WalMart pioneered this system in the 1980s to gain a competitive advantage against competitors such as Sears or Kmart.



----------


# Ecosystem

Our ecosystem includes a variety of solutions aimed at leveraging existing technologies and market fit. 


- Both Blockchain and Traditional Solutions
- Web and Mobile
- B2B and B2C Solutions 
- Analytics and Intelligence Toolset


Our Ecosystem strives to cover these core competencies

Compliance and Accountability
Document  Authentication and Management
Data Forecasting, Insights and Analytics

Our approach has been to offer clear use cases for blockchain applications. These are qualified by the following parameters

Strong case for Data Ownership
Trust-less Record Keeping
Removal of “middlemen” 
<additional>
<additional>

Therefore our product listings are:
Passports for Drivers, Vehicles and Assets
Documents & Records: Bills of Lading, Industry Specific Documents, Legally Mandated Records
Barcodes -  


### Passports - Driver, Vehicle and Asset

Driver records are a great use case.


| Identifying Information for Supporting Documents                                                                                                                                                                                          |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Driver name or carrier-assigned identification number, either on the document or on another document enabling the carrier to link the document to the driver. The vehicle unit number can also be used if it can be linked to the driver; |
| Date                                                                                                                                                                                                                                      |
| Location (including name of nearest city, town, or village)                                                                                                                                                                               |
| Time                                                                                                                                                                                                                                      |

*These must be listed on the supporting documents in order to be eligible for use.*

| Supporting Documents 

Documents that must be retained by law                                                              |
| -------------------------------------------------------------------------------------------------------------------------- |
| Bills of lading, itineraries, schedules, or equivalent documents that show the starting and ending location for each trip; |
| Dispatch records, trip records, or equivalent documents;                                                                   |
| Expense receipts related to “on-duty/not driving” periods (meals, lodging, fuel, etc.);                                    |
| Fleet management system communication records;                                                                             |
| Payroll records, settlement sheets, or equivalent documents showing payment to a driver.                                   |


What happens if a log was anchored incorrectly? 
The ELD regulation provides for this, as both the original and edited versions must be retained. Any edits to the log, either by the motor carrier or driver must be annotated as to the reason for the edit. On the Driver Passport page, both records are accessible. 


https://airtable.com/shrCzCmWXhYaIs4oX





## Object Naming Service 

In order to use DNS to find information about an item, the item’s GS1 Identification Key must be converted into a format that DNS can understand, which is the typical, “dot” delimited, left-to-right form of all domain names. As the purpose of ONS is to discover data and services associated with a GS1 Identification Key and multiple sets of data and services may exist for that key, the appropriate DNS record type is the Naming Authority PoinTeR (NAPTR) [RFC 3403]. This record type contains several fields for denoting the protocol, services, and features that a given service endpoint exposes. It also allows the service endpoint to be expressed as a URI, thus allowing complex services to be encoded in a standard way. The figure below describes a typical ONS query from start to finish from the viewpoint of an application. In this example, the starting point is a bar code or RFID tag. However, the source of the GS1 IdentificationKey is not restricted to data carriers; it could be part of a transaction document (e.g. a purchase order), an event record, a master data record, or any other source.



## EPCIS

EPCIS – Electronic Product Code Information Service It is an international standard adopted by GS1 in September 2016 to Identify, Capture and Share Information using barcodes/etc. It enables disparate applications to leverage Electronic Product Code (EPC) data by sharing that data. The EPC data is shared within and across enterprise boundaries. Sharing this data enables all participants within an EPCIS compliant ecosystem to gain visibility into the status of all EPC “marked” digital or physical items (also known as EPCIS “objects”) within a given business context. Simply put, EPCIS provides a framework that allows trading partners to know the status of a given trade item or conveyance. 

EPCIS events affect the status of a trade item or conveyance by changing or setting the object’s disposition (its current state, such as sold, expired, recalled, in transit, or active). “EPCIS is a standard which provides the means to Identify real-world entities so that they may be the subject of electronic information that is stored and/or communicated by end users/clients. GS1 identification standards include standards that define unique identification codes (called GS1 Identification Keys), such as the Global Trade Item Number.” [GS1] 

It provides the means to automatically Capture data that is carried directly on physical objects, bridging the world of physical things and the world of electronic information.” [GS1] GS1 data capture standards include definitions of bar code and radio-frequency identification (RFID) data carriers which allow identifiers to be affixed directly to a physical object, and standards that specify consistent interfaces to readers, printers, and other hardware and software components that connect the data carriers to business applications. 

It also provides the means to share information, both between trading partners and internally, providing the foundation for electronic business transactions, electronic visibility of the physical or digital world, and other information applications. GS1 standards for information sharing include this EPCIS Standard which is a standard for visibility event data. Other standards in the “Share” group are standards for master data and for business transaction data, as well as discovery standards that help locate where relevant data resides across a supply chain and trust standards that help establish the conditions for sharing data with adequate security.

Description of EPCIS Event Data
EPCIS is structured in a way to define business processes as individual business steps. Information of a single EPCIS event data is organized into four different dimensions:


- What The identifiers of the object(s) or other entities that are the subject of the event 
- When The date and time when the event took place, and the local time zone in effect 
- Where The identifier of the location at which the event occurred, and identifier of the location where the object(s) are expected to be following the event 
-  Why Information about the business context, including: a identifier that indicates the business step taking place (e.g., shipping, receiving, etc.), an identifier that indicates the business state of the object(s) following the event (e.g., active, recalled, damaged, etc.), identifiers of the shipping and receiving parties (if the event is part of a process of transfer between parties), links to relevant business transaction documents (e.g., a purchase order, an invoice, etc.), instance- or lot-level master data, and/or other information defined via user extensions. 

The EPCIS data model calls for an identifier, EPCIS allows any URI/URL to be used to store additional data. We use this model because of interoperability with barcodes across the globe.

Why EPCIS is important
EPCIS Event Data The Core Business Vocabulary (CBV) is a GS1 Standard that defines specific data values to populate the EPCIS data model. This ensures that all parties who exchange EPCIS data have a common and consistent understanding of the semantic meaning of that information. [GS1] By documenting supply chain events, EPCIS data complements other types of data exchange in the supply chain, such as business transaction data (exchanged with GS1 eCom) and master data (exchanged with GS1 Global Data Synchronization Network or GDSN).


> EPCIS provides visibility on a “need-to-know” basis for goods.

A company implementing EPCIS can use the authenticated identity of a trading partner in conjunction with pre-defined business rules (smart contracts/chaincode) to determine which information is made available to that partner. 


| Business Applications that utilize EPCIS event data |
| --------------------------------------------------- |
| Product Authentication                              |
| Pharmaceutical Pedigree                             |
| Product and food traceability                       |
| Inventory Management                                |
| Shipment Tracking                                   |
| Electronic Article Surveillance (EAS)               |
| Promotion Tracking                                  |







----------


# Blockchain Specifications 

Designing both a performant and scalable blockchain requires drawing on various disciplnes, from computer science to business administration. Creating a network that enhances the benefits of using a blockchain is typically focused on various criteria involving benchmarking. Performance has been shown not to be a barrier for adoption by businesses, but rather the lack of applications, adherance to industry standards, and consideration of business-wide impact of certain activies (i.e. accounting implications that arise from the use of cryptocurrencies). 


> “Differences in performance between chains are usually almost entirely due to differences in the protocols and the implementations, not the consensus algorithm”
> Go Ethereum p.g. 8


## Requirements 

Our requirements list:


- Adoption of Industry Standards/Compliance with Standards 
  - PCI DSS, FIPS, ISO Standards
- Easy Key Management 
- Ability for 100% Privacy
- Ability for determinism in state (no hard-forking)
- Ability to withstand off-chain attack vectors, e.g:
  - Bribery
  - Cartel Forming
- Ability to withstand on-chain attack vectors, e.g:
  - 51% Attack
  - Refusal to Participate
  - Sybil Attack
- Reduce the use of cryptocurrency to a bare minimum 
- Adherence to Strict Data Retention and Privacy policies (e.g. GDPR)
- Multiple Security Audits by outside Firms
- Contract outside Security Firms at the designing and conception phase of products
- Rigorous pilot study with large enough sample size 
- Multiple testing phases with different user base
- Create a Blockchain Network Management Plan that documents design, development, distribution, deployment, maintenance, and end-of-life procedures for any network service

<paragraph >


## Model


- Assets - Asset definitions enable the exchange of almost anything with monetary value over the network, from whole foods to antique cars to currency futures.
- Chaincode - Chaincode execution is partitioned from transaction ordering, limiting the required levels of trust and verification across node types, and optimizing network scalability and performance.
- Ledger Features - The immutable, shared ledger encodes the entire transaction history for each channel, and includes SQL-like query capability for efficient auditing and dispute resolution.
- Privacy through Channels - Channels enable multi-lateral transactions with the high degrees of privacy and confidentiality required by competing businesses and regulated industries that exchange assets on a common network.
- Security & Membership Services - Permissioned membership provides a trusted blockchain network, where participants know that all transactions can be detected and traced by authorized regulators and auditors.
- Consensus -a Byzantine Fault Tolerant (BFT) consensus protocol, PBFT or RBFT.



## Implementation 

paragraph 

### State Database
CouchDB additionally enables rich query against the smart contract data, when chaincode values (e.g. assets) are modeled as JSON data.

you can also perform complex rich queries against the chaincode data values, using the CouchDB JSON query language within chaincode. These types of queries are excellent for understanding what is on the ledger. 

### Endorsement Policies

### Masternodes
paragraph 


1. Primary
2. Secondary
3. Heartbeat
#### Primary

Primary nodes provide specific services:

- Membership Service Provider
- Validating Peers

These are to ensure server uptime 

#### Secondary

Data Layer nodes
Non-Validating Peers
These are to ensure the public layer channel redundancy. 


> Think of Primary as “Miners” and Secondary as “Full Nodes” - they keep a record of the entire chain but do not commit blocks to the chain

$$\sigma = \alpha * 1.37$$
where $$\sigma$$ is the amount of Secondary and $$\alpha$$ is the amount of Primary nodes and $$1.37$$ is a fixed constant determined by us

#### Heartbeat 

Heartbeat nodes are specific network participants for the gossip protocol. They are responsible for the ordering of transactions.

Dynamic leader election
Dynamic leader election enables organization peers to elect one peer which will connect to the ordering service and pull out new blocks. Leader is elected for set of peers for each organization independently.
Elected leader is responsible to send the heartbeat messages to the rest of the peers as an evidence of liveness. If one or more peers won’t get heartbeats updates during period of time, they will initiate a new round of leader election procedure, eventually selecting a new leader. In case of a network partition in the worst case there will be more than one active leader for organization thus to guarantee resiliency and availability allowing the organization’s peers to continue making progress. After the network partition is healed one of the leaders will relinquish its leadership, therefore in steady state and in no presence of network partitions for each organization there will be only one active leader connecting to the ordering service.
Following configuration controls frequency of the leader heartbeat messages:

    peer:
      gossip:
            election: leaderAliveThreshold: 10s



### ARY Token
  

The Block Array Token, "ARY" is an Ethereum standard compliant "ERC-20" blockchain asset. The asset is our implementation of a software license that is used in a variety of ways for the end customer. The ARY token can be thought of as an access card, granting the end user the ability to interact with various applications and infrastructure. The ARY token enables the user rights of access depending on the amount of tokens they have in their possession. Along with access rights they are granted an allotment of network resources based on the amount of ARY held.
*** insert equation here ***
ARY is not a currency nor a virtual asset ment to be used for the payments of goods and services.
This design choice was made because of the following factors

[ ] Ease of Use
[ ] Lower Wallet Requirements
[ ] Little Accounting/GAAP considerations
[ ] Less Accounting Headache


The amount of ARY tokens is preliminary and has not been finalized yet

| Tier      | # of ARY Tokens |
| --------- | --------------- |
| Primary   | 40,000          |
| Secondary | 22,500          |
| Heartbeat | 7,500           |



Mitigating Attack Vectors

By distributing the network among individuals who have our ARY token, they reduce the chance of businesses being able to form a cartel for the purpose of disrupting the network. 

![Distribution of the Network among all Participants](https://www.dropbox.com/s/zbbacvd6r9w84bo/Screenshot%202018-04-23%2013.39.51.png?raw=1)



token as network incentive 

The following digram illustrates how the ARY Blockchain distributes rewards by using the Ethereum Blockchain (therby the ERC-20 token).




![](https://www.dropbox.com/s/m92bfzsfew7i8ei/Screenshot%202018-04-23%2013.41.30.png?raw=1)





Requirements

  1. Unique Implementations
  2. ARY Token
  3. Performance Benchmarks



----------

References

FMCSA 
https://www.fmcsa.dot.gov/hours-service/elds/electronic-logging-devices

D.O.T 
https://www.gpo.gov/fdsys/pkg/FR-2015-12-16/pdf/2015-31336.pdf



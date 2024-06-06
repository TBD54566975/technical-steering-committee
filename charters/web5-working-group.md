# Web5 Working Group Charter

**Start Date**: June 7, 2024

**End Date**: December 31, 2024 

**DRI**: [Frank Hinek](https://github.com/frankhinek)

## Motivation and Background

[Web5](https://developer.tbd.website/projects/web5/) is defined as...

> A decentralized web platform that puts you in control of your data and identity.

> The web democratized the exchange of information, but it's missing a key layer: identity. We struggle to secure personal data with hundreds of accounts and passwords we can’t remember. On the web today, identity and personal data have become the property of third parties.

> Web5 brings decentralized identity and data storage to your applications. It lets devs focus on creating delightful user experiences, while returning ownership of data and identity to individuals.

TBD has been building Web5 (nearly) since its inception. Web5 is the foundational layer of the TBD stack upon which decentralized applications, protocols, and services can be built. Today, Web5 is a collection of projects that are built on open standards pertaining to decentralized identity and self-sovereign technologies like Decentralized Identifiers (DIDs), and Verifiable Credentials (VCs), and Decentralized Web Nodes (DWNs) for secure personal storage and decentralized protocols.

A key driver for this initiative is tbDEX, a use case that exemplifies the potential of the Web5 technology stack. tbDEX leverages Web5 to enable secure, decentralized value exchanges without intermediaries. This project highlights the practical applications and benefits of Web5 technologies, serving as a proof of concept that will guide the development and adoption of similar decentralized applications.

Through this Working Group, we aim to continue building a robust and scalable framework for Web5, providing developers with the tools they need to build innovative and secure decentralized applications.

## Scope

* Selection of standards pertaining to digital identifiers, credentials, storage, and associated protocols.

* Implementation of a common set of standards using a well-defined API for the usage of these standards across programming languages.

* Support for the needs of the TBD business unit, including, but not limited to the feature set required by [tbDEX](https://developer.tbd.website/projects/tbdex/).

* Conformance infrastructure such as test vectors, test suites to encourage compatible implementations across programming languages.

* Enable the development of Decentralized Applications (dApps) using technologies such as Decentralized Identifiers (DIDs) and Verifiable Credentials (VCs).

## Deliverables

### 1. Web5 Specification

**Description**: Develop and maintain the [Web5 Specification](https://github.com/TBD54566975/web5-spec/), that clearly specify:

**DRI**: [Gabe Cohen](https://github.com/decentralgabe)

**Scope of Work**:

* Specification of the digital identity standards we will implement (e.g. specific DID methods, verifiable credential data models, credential issuance protocols) along with specific implementation details (e.g. required features, minimal subsets, etc.).

* An API used to interact with the digital identity standards we implement, able to be uptaken across Web5 SDKs.

* Test vectors from which conformance to each feature in the specification can be achieved.

### 2. Web5 SDKs

**Description**: Develop and maintain Web5 SDKs which shall conform to the Web5 Specification.

**DRI**: [Frank Hinek](https://github.com/frankhinek)

**Scope of Work**:

* SDKs in [Typescript](https://github.com/TBD54566975/web5-js), [Kotlin](https://github.com/TBD54566975/web5-kt), [Swift](https://github.com/TBD54566975/web5-swift), [Dart](https://github.com/TBD54566975/web5-dart), [Go](https://github.com/TBD54566975/web5-go), and [Rust](https://github.com/TBD54566975/web5-rs).

* SDKs shall demonstrate conformance to the test vectors defined by the Web5 specification.

* SDKs shall be well-documented according to each language's conventions, as well as being surfaced through the [developer site](https://developer.tbd.website/docs/).

* SDKs shall follow the guidance of the Rust Working Group in adopting a Rust core to limit developer overhead. 

### 3. DID DHT

**Description**: Develop and maintain the DHT Decentralized Identifier method (did:dht).

**DRI**: [Gabe Cohen](https://github.com/decentralgabe)

**Scope of Work**:

* Develop and maintain the [DID DHT Method Specification](https://did-dht.com/) and [DID DHT Method Registry](https://did-dht.com/registry).

* Develop and maintain an open source implementation of a [DID DHT Gateway Server](https://did-dht.com/#gateways).

* Develop and maintain a conformance testing suite for DID DHT clients, including test vectors and implementation reports.

* Ensure conformant implementation of the DID DHT method across **Web5 SDK** implementations.

### 4. Decentralized Web Nodes (DWNs)

**Description**: Develop and maintain the Decentralized Web Node specification and associated implementations.

**DRI**: [Daniel Buchner](https://github.com/csuwildcat)

**Scope of Work**:

* Build and maintain an SDK for Decentralized Web Nodes (DWN). This SDK will facilitate the integration of and interaction with DWNs, promoting decentralized data storage and management. To be built upon the work already in [web5-js](https://github.com/TBD54566975/web5-js).

* Develop and maintain a DWN Server to allow anyone to host Decentralized Web Nodes easily and efficiently. This server will be crucial for the deployment and scaling of DWNs. To be built off the work in [dwn-sdk-js](https://github.com/TBD54566975/dwn-sdk-js).

* Develop a demonstration of a web and mobile application (in conjunction with the subsequent work item) that integrates the deliverables above to showcase the capabilities and potential of Web5.

### 5. Identity Agent

**Description**: A mobile application (both iOS and Android) to manage users' DIDs, VCs, and permissions to DWNs. The Identity Agent App will provide a user-friendly interface for handling digital identities and credentials in a secure manner.

**DRI**: [Tim Shamilov](https://github.com/shamilovtim)

**Scope of Work**:

* Develop and maintain a cross-platform mobile application that facilitates the management of DIDs, VCs, and permissions interfacing with DWNs.

* Develop a demonstration of a web and mobile application (in conjunction with the subsequent work item) that integrates the deliverables above to showcase the capabilities and potential of Web5.

## Success Criteria

1. **Web5 Specification**
	
	* A published v1.0 specification with a common API and test vectors.

	* A test suite demonstrating conformance for each test vector, demonstrating compatability across multiple implementations (via Web5 SDKs).

2. **Web5 SDKs**

        * Across the aforementioned languages, feature completeness in accordance with version 1.0 of the Web5 specification's feature set and API.

	* Demonstrated interoperability via the Web5 specification test suite.

	* Uptake of a Rust core where applicable (note: uptake of a Rust core may not be viable in some languages, like JS).

	* Successful implementation of tbDEX SDK Using the Web5 SDK against the v1.0 specification.

4. **DID DHT**

	* A published v1.0 specification and registry with a Gateway API and client test vectors.

	* An open source server implementation fully implementing the v1.0 specification's Gateway API.

	* At least two v1.0 open source client implementations in different programming languages.

	* Complete test vector coverage via an automated test suite demonstrating multiple conformant implementations (via Web5 SDKs).

5. **Decentralized Web Nodes (DWNs)**

	* Partners will be able to self-deploy Decentralized Web Nodes (DWNs) leveraging the DWN Server.

6. **Identity Agent**

   * A publicly available and installable demo application, capable of providing an end-to-end experience, integrating features from the Web5 SDK and DWN projects to showcase the power and potential of Web5 technologies.

   * Production of at least one recorded demonstration of an end-to-end experience using the demo application on both iOS and Android. 

## Coordination

This group favors document-driven coordination, documenting communications and decisions. The group will be facilitated via the [Technical Steering Comittee](https://github.com/TBD54566975/technical-steering-committee) and the set of repositories specific to each of the work items and deliverables listed above, making use of GitHub Issues and a common GitHub project for the entire Working Group's corpus.

The Working Group will closely collaborate with the tbDEX and Working Group to ensure alignment and support for the tbDEX protocol and requirements. Similarly, the Working Group will coordinate closely with the Rust Working Group for the uptake of a Rust Core throughout the Web5 SDKs. Coordination will surface through the TSC, associated GitHub repositories, and communication tools (Slack, Discord).

## Communication

The working group will communicate primarily in a written manner via GitHub: filing issues and Requests for Comments (RFCs) directly to the respective GitHub repository (e.g. Web5-spec and Web5 SDKs, DID DHT, DWN Server, Identity Agent, etc.).

The group will establish dedicated public and private communication channels as necessary (e.g., TBD Slack, TBD Discord) for real-time discussions and quick resolution of issues.

The Working Group DRI will coordinate weekly updates for each of the group's work items, with the respective DRIs of each work item, to share with the TSC.
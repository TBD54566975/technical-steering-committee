# Web5 Working Group Charter

**Start Date**: 2024/06/06  
**End Date**: 2025/06/05  
**DRI**: Frank Hinek

## Motivation and Background
As the digital landscape evolves, there is a growing demand for technologies that enhance user privacy, security, and autonomy. Web5 aims to fulfill these requirements by building on the principles of decentralization established by its predecessors.

The Web5 Working Group is formed to address the critical need for developing the code and infrastructure necessary to support the next generation of decentralized applications, collectively referred to as Web5.

A key driver for this initiative is tbDEX, a use case that exemplifies the potential of the Web5 technology stack. tbDEX leverages Web5 to enable secure, decentralized value exchanges without intermediaries. This project highlights the practical applications and benefits of Web5 technologies, serving as a proof of concept that will guide the development and adoption of similar decentralized applications.

Through this Working Group, we aim to create a robust and scalable framework for Web5, providing developers with the tools they need to build innovative and secure decentralized applications. By focusing on core components such as Verifiable Credentials (VC), Decentralized Identifiers (DID), and Decentralized Web Nodes (DWN), we will lay the foundation for a more open and user-centric web.

## Scope

1. Support requirements driven from the development of tbDEX.
2. Enable the development of DApps (decentralized apps) through the creation of SDKs for:
   - Verifiable Credentials (VC)
   - Decentralized Identifiers (DID)
   - Decentralized Web Nodes (DWN)

## Deliverables

1. **DID SDK – SDK**

   **Description**:  
   Develop an SDK for Decentralized Identifiers (DID). This SDK will provide developers with the necessary tools to create, manage, and utilize DIDs in their applications.

   **DRI**:  
   - `js` - Henry Tsai
   - `kotlin` - Jiyoon Koo
   - `swift` - Kirah Sapong
   - `rust` - Kendall Weihe?

2. **VC SDK – SDK**

   **Description**:  
   Develop an SDK for Verifiable Credentials (VC). This SDK will enable developers to issue, verify, and manage verifiable credentials, ensuring secure and trustworthy digital interactions.

   **DRI**:  
   - `js` - Henry Tsai
   - `kotlin` - Jiyoon Koo
   - `swift` - Kirah Sapong
   - `rust` - Kendall Weihe?


3. **DWN SDK – SDK**

   **Description**:  
   Create an SDK for Decentralized Web Nodes (DWN). This SDK will facilitate the integration of and interaction with DWNs, promoting decentralized data storage and management.

   **DRI**:  
   Liran Cohen, Henry Tsai

4. **DWN Server – Infrastructure**

   **Description**:  
   Develop a DWN Server to allow anyone to host a new Decentralized Web Node easily and efficiently. This server will be crucial for the deployment and scaling of DWNs.

   **DRI**:  
   Liran Cohen, Henry Tsai

5. **Identity Wallet App – Mobile Application**

   **Description**:  
   Create a mobile application to manage users' DIDs, VCs, and permissions to DWNs. This Identity Wallet App will provide a user-friendly interface for handling digital identities and credentials securely.

   **DRI**:  
   Tim Shamilov

6. **Demo App – Application**

   **Description**:  
   Develop a demonstration application that integrates the deliverables above to showcase the capabilities and potential of Web5.

   **DRI**:  
   Daniel Buchner

## Success Criteria

The success of the Web5 Working Group will be determined by the following criteria:

1. **Successful Implementation of tbDEX SDK Using the Web5 SDK**:  
   The tbDEX SDK should be able to leverage capabilities provided by the Web5 SDKs (DID SDK, VC SDK, Crypto SDK) for its implementation.

2. **Successful Third Party Deployment of DWN by Our Partners**:  
   Partners should be able to deploy Decentralized Web Nodes (DWNs) leveraging the DWN Server, demonstrating its ease of use and effectiveness in real-world applications.

3. **Successful End-to-End App Experience of the Demo App**:  
   The demo application should provide a seamless and fully functional end-to-end experience, integrating all deliverables (DID SDK, VC SDK, DWN SDK, DWN Server, Identity Wallet App) to showcase the power and potential of Web5 technologies.

## Coordination

This group favors document-driven coordination, documenting communications and decisions. More specifically, the Web5 Working Group will closely collaborate with the tbDEX Working Group to ensure alignment and support for the tbDEX protocol and requirements. 

- Filing issues and Requests for Comments (RFC) directly to the respective GitHub repository.
- Sharing formal documentation and specifications through GitHub repositories.
- Establishing a dedicated communication channel (e.g., Slack) for real-time discussions and quick resolution of issues.

## Communication
We will heavily rely on GitHub Issues for external asynchronous communication and feedback. We use Discord for more real-time communication.

Progress will be reviewed and reported to the TSC (Technical Steering Committee) as needed or at the TSC's requested frequency. Each review will include a detailed progress report covering milestones achieved, upcoming tasks, and any roadblocks.

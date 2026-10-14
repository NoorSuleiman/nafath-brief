Version: NAFATH-V2
Track: Networking

## Overview

A reliable 5G emergency service depends on several technical areas working together. At the software level, safe and idempotent HTTP methods can help applications handle repeated requests correctly. AI models should be evaluated carefully to avoid overfitting and to perform well on new data. Mobile applications also need offline capabilities and reliable data synchronization when connectivity is interrupted. At the network level, 5G network slicing can provide dedicated resources and service characteristics for critical emergency communications. Cybersecurity is also essential, as a clear incident response process helps detect, contain, and recover from attacks. Finally, suitable data models support efficient storage and analysis of operational information. Together, these areas can improve the availability, reliability, security, and continuity of a 5G service for emergency response teams. My Networking question focuses on how 5G network slicing can support reliable communication for emergency services.

## Software

Safe HTTP methods are GET, HEAD, OPTIONS, and TRACE because they are mainly used to retrieve or check information without changing the server’s state. Idempotent methods include these methods as well as PUT and DELETE. This is important when a client retries a failed request because repeating an idempotent request should have the same intended result as sending it once. In contrast, retrying a non-idempotent request such as POST may cause the same action to happen more than once.

Resource: RFC 9110 – HTTP Semantics, Sections 9.2.1 and 9.2.2 – https://www.rfc-editor.org/rfc/rfc9110.html

## AI

Overfitting happens when a machine learning model learns the training data too closely, including noise and patterns that may not apply to new data. As a result, the model may perform very well on the training data but poorly on unseen data. Cross-validation helps detect this by splitting the data into several parts and testing the model on different parts while training on the others. If the model performs well on training data but shows weaker or inconsistent results during validation, it may be overfitting.

Resource: scikit-learn – Underfitting vs. Overfitting – https://scikit-learn.org/stable/auto_examples/model_selection/plot_underfitting_overfitting.html

## Mobile

When the responder’s mobile app is offline, it should continue to provide access to previously stored information and allow important actions or updates to be recorded locally. The app should clearly indicate that it is offline and keep unsynchronized changes in a local queue. When the connection returns, the app should send the pending changes to the server and update the local data with the latest server information. Any conflicting changes should be handled using a defined synchronization rule to avoid losing important data.

Resource: Firebase Documentation – Enabling Offline Capabilities – https://firebase.google.com/docs/database/android/offline-capabilities

## Networking

5G network slicing allows a physical network to be divided into multiple logical networks, with each slice designed for different requirements. For emergency services, a dedicated slice can provide suitable performance, reliability, and resource allocation for critical communications. This can help emergency teams maintain important services even when other parts of the network are experiencing heavy traffic. Network slicing therefore supports the use of 5G for applications that require dependable and prioritized communication.

Resource: 3GPP – 5G Network Slicing – https://www.3gpp.org/technologies/5g-system-overview

## Cybersecurity

The incident response lifecycle provides a structured approach for handling a security incident. It includes four main phases: preparation, detection and analysis, containment, eradication and recovery, and post-incident activity. Preparation establishes plans and resources before an incident occurs. Detection and analysis identify and assess the attack. Containment limits its impact, while eradication removes the threat and recovery restores affected services. Finally, post-incident activities review what happened and identify improvements to prevent similar incidents in the future.

Resource: NIST – Computer Security Incident Handling Guide (SP 800-61 Rev. 2) – https://csrc.nist.gov/pubs/sp/800/61/r2/final

## Data

A star schema has a central fact table connected directly to dimension tables, making the structure simple and easier to query. A snowflake schema further normalizes the dimension tables into additional related tables, which can reduce data duplication but makes queries more complex. For daily service usage reports by region, a star schema is more suitable because the structure is simpler and supports faster and easier reporting queries.

Resource: Microsoft Learn – Understand star schema and snowflake schema – https://learn.microsoft.com/en-us/power-bi/guidance/star-schema
## Misconception in My Track

A common misconception is that network slicing simply gives emergency services a completely separate physical network. In reality, network slicing creates logical networks on shared physical infrastructure, with each slice configured to meet specific service requirements. This means emergency traffic can receive suitable resources and performance without requiring a separate physical network. 3GPP explains that network slicing allows multiple logical networks to be created on the same physical network infrastructure.

## Open Question

I would like to verify how network operators prioritize emergency traffic when several network slices are competing for limited resources during a major emergency.

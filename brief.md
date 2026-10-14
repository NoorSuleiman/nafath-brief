Version: NAFATH-V2
Track: Networking

## Overview

A reliable 5G emergency service depends on several technical areas working together. At the software level, safe and idempotent HTTP methods can help applications handle repeated requests correctly. AI models should be evaluated carefully to avoid overfitting and to perform well on new data. Mobile applications also need offline capabilities and reliable data synchronization when connectivity is interrupted. At the network level, 5G network slicing can provide dedicated resources and service characteristics for critical emergency communications. Cybersecurity is also essential, as a clear incident response process helps detect, contain, and recover from attacks. Finally, suitable data models support efficient storage and analysis of operational information. Together, these areas can improve the availability, reliability, security, and continuity of a 5G service for emergency response teams. As a Networking track participant, I am particularly interested in how network slicing can support reliable communication under changing network conditions.

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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question

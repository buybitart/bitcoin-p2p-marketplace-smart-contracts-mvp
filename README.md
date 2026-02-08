# ⚡ Bitcoin-based P2P Marketplace (MVP) - Smart Contracts

Peer-to-peer online marketplace powered by **Bitcoin & Lightning Network (Smart Contracts)**, designed for secure, private, and fast transactions without intermediaries.

**STAGE I**
 - Buyer and Seller set a Smart-contract
 - Buyer deposits funds with the Smart-contract

**STAGE II**
 - Seller ships goods once sees the funds locked by the smart-contract
 - Smart-contract is tracking goods delivery

**STAGE III**
 - Upon the goods are delivered Smart-contract releases funds to the Buyer

<img width="1536" height="1024" alt="1" src="https://github.com/user-attachments/assets/61d42481-26bc-4c80-9fa1-ef54bc5cbfff" />


---

## 🔁 How does this work

1. **The Buyer and the Seller agree on the trade** and create a smart contract on the Lightning Network  
   (Blockchain Smart Contracts: https://lightning.network/how-it-works/).

2. **The Lightning Network locks the Buyer’s funds** to guarantee payment upon delivery:
   - the Lightning Network locks cryptocurrency funds directly within the blockchain smart contract.

3. **The Seller ships the goods** via a logistics company and submits the tracking number to the Lightning Network  
   
4. **Upon confirmation of delivery to the Buyer** (the tracking information matches the Buyer’s address specified in the smart contract),  
   the Lightning Network releases the payment to the Seller.

<img width="1536" height="1024" alt="2" src="https://github.com/user-attachments/assets/bcb70024-cdbe-49bb-a690-3a38b4c1fe46" />

---

## 📚 Table of Contents

- [Overview](#-overview)
- [Platform Key Components](#-platform-key-components)
- [Platform Components](#-platform-components)
- [Solution Architecture](#-solution-architecture)
- [Technology Stack](#-technology-stack)
- [Project Timeline](#-project-timeline)
- [Project Status](#-project-status)

---

## 🚀 Overview

We are going to develop an **MVP for an exclusive online marketplace** that operates on a **peer-to-peer (P2P) model** using **Bitcoin as the only available payment method**. Later on, it can be expanded to other cryptocurrencies and FIAT.

Our focus is on ensuring **security, user-friendliness, and privacy** of the platform.

Key features include:
- user registration and authentication;
- profile management;
- seller product upload and management;
- efficient product search and filtering for buyers.

Secure transactions are implemented using **blockchain smart contracts**, integrating:
- a **multi-signature Bitcoin wallet**;
- **frosted transactions** to hold funds until goods are received.

The platform also includes:
- feedback and rating systems;
- notification system;
- support modules.

In terms of design and usability, the platform emphasizes a **minimalistic and interactive interface**, optimized for all device categories.

From a technical perspective, the solution uses **modern scalable technologies**, including:
- Kafka for efficient event handling;
- automated deployment and scaling via **Docker and AWS EKS (Kubernetes)**;
- a **microservices-based architecture** with API integration capabilities.

Security and privacy are treated as a priority, ensuring:
- GDPR compliance;
- data encryption at all stages;
- two-factor authentication (2FA).

---

## ✨ Platform Key Components

<img width="1536" height="1024" alt="3" src="https://github.com/user-attachments/assets/91354271-11d2-44fe-8d40-ed5d522a7ac7" />


---

## 🧩 Platform Components

### **1. eCommerce Platform**

A comprehensive Bitcoin-centric platform designed to facilitate seamless buying and selling experiences.

Core functionality includes:
- user registration;
- product management;
- efficient search;
- feedback mechanisms;
- notifications;
- support modules.

The platform operates in a **peer-to-peer (P2P) mode**, enabling direct transactions between buyers and sellers without intermediaries.

---

### **2. Administrative Module**

The administrative component provides a centralized hub for **super administrators and sellers**.

It includes:
- an analytical dashboard with key metrics;
- Orders and Users management;
- transaction monitoring;
- financial activity management;
- GDPR compliance tools, including user blocking and deletion.

Sellers have visibility into their own transactions, ensuring transparency and control.

---

### **3. Lightning Network (Bitcoin)**

Users receive **Lightning wallet accounts via the LNDHub system**, creating nodes on the Lightning Network.

The system:
- opens payment channels between user nodes and the main hub node;
- enables fast off-chain payments;
- opens channels to external Lightning nodes and on-chain settlement addresses.

Users can:
- deposit funds;
- withdraw funds;
- settle balances on-chain when required.

Payments are routed through the hub, ensuring low fees and high speed.

For withdrawals:
- balances are routed back to the hub;
- an on-chain transfer is made to the user’s external wallet.

Each user has access to a dashboard displaying:
- balance;
- transaction history;
- channel status;
- connectivity information.

Planned advanced features include:
- channel rebalancing;
- pathfinding;
- submarine swaps;
- integration with exchanges and merchants.

---

### **4. Security and Privacy**

The platform is developed in strict compliance with **GDPR** requirements.

Key aspects include:
- structured data storage;
- robust backup mechanisms;
- advanced encryption protocols;
- data anonymization practices.

This approach ensures data protection and regulatory compliance.

---

### **5. Project Infrastructure**

The project infrastructure is based on a **microservices architecture** to ensure modularity and scalability.

Key components:
- Kafka for event stream processing;
- Docker for containerization;
- AWS EKS / Kubernetes for orchestration and scaling;
- an API layer for system integration and future expansion.

---

## 🏗 Solution Architecture

<img width="1536" height="1024" alt="5" src="https://github.com/user-attachments/assets/eb3e4960-1d72-407c-9041-54805b2a82f2" />



### Solution Architecture Description

1. **API Gateway** – single entry point for all client requests.
2. **Service Layer (SVC)** – orchestration of core business logic.
3. **Authentication Service (AUTH)** – user authentication and session management.
4. **Wallet Service (WALLET)** – Bitcoin wallet operations.
5. **Inventory Service (INV)** – product and inventory management.
6. **Order Service (ORDS)** – order lifecycle and smart contract execution.
7. **Payment Service (PAY)** – Bitcoin payment processing.
8. **MPC Wallet Service (MPC)** – multi-party computation for wallet security.
9. **LNDHub Service (LNDHUB)** – Lightning Network wallet service.
10. **Notification Service (NOTIF)** – user and system notifications.
11. **Feedback & Ratings Service (FEEDB)** – feedback and reputation system.

---

## 🛠 Technology Stack

### Frontend
- React
- Redux / Redux-Saga
- MUI v5
- Axios
- i18n

### Backend
- Java 17
- Spring Boot
- Spring Cloud Gateway
- PostgreSQL
- Kafka
- gRPC

### Blockchain
- Bitcoin
- Lightning Network
- LNDHub

---

## 🗓 Project Timeline

- Estimated duration: **~5–6 months**
- MVP-focused development approach
- Iterative delivery
- Dedicated stabilization phase

---

## 🚧 Project Status

The project currently has a **defined MVP scope**, architecture, technology stack, timeline, and budget estimation.
At this stage, the project is **in search of financing and implementation of the MVP**.

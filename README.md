# Client-Server Distributed System

## Overview
This project implements a distributed logistics system. A central server (C++) coordinates deliveries, inventory, and supply chains between thousands of autonomous clients in a supply network. 
This system enables clients to exchange essential goods like food, medicine, and equipment through hubs, warehouses, and delivery trucks.

---

## Types of Clients

- **Warehouses** (automatic clients in C)  
  Local inventory managers. Report stock, receive orders, trigger restocking.

- **Hubs** (automatic clients in C)  
  Intermediate distribution points. Reroute supplies, confirm shipments.

- **Delivery Trucks** (simulated agents)  
  Represent moving shipments. Report GPS, confirm pickups/deliveries.

- **Privileged Operators** (human users in Go)  
  Access the system via a **REST API**. Used for supervision, overrides, and admin control.

---

## Core Features

- **Real-time inventory tracking**
- **Supply routing optimization**
- **Emergency alert handling**
- **Secure hostname-based authentication and salted password hashing**
- **Fault tolerance and high availability – MySQL database**
- **Structured message formats in JSON** 
- **Logging of all transactions for traceability**

---

## Communication Protocols

- **TCP Sockets** (IPv4 & IPv6) between Server and automated clients (Hubs, Warehouses, Trucks)
- **RESTful HTTP API** for communication with Privileged Operators

---

## Scalability & Performance

Designed to support **over 1,000 hubs and warehouses** simultaneously. Uses modular shared libraries and concurrent processing to handle high transaction volumes efficiently.

---

## Programming Languages

- **C++** — Central server and core logic  
- **C** — Warehouses, hubs, and delivery trucks clients  
- **Go** — REST API server (for human operators)

---

## Technologies & Tools

- **Docker** – Containerized deployment  
- **CMake** – Build automation  
- **Conan** – Dependency management for C/C++  
- **MySQL** – Persistent storage of inventory and transactions  
- **GitHub Actions** – CI/CD  
- **Sockets (IPv4/IPv6)** – Network communication  
- **Shared Libraries (.so)** – Modular client functionality

---

## How to Run

_Coming soon_

A Docker Compose setup will orchestrate:
- The central server
- Multiple client containers
- The MySQL database
- The REST API gateway

---

## Folder Structure

_Coming soon_

Expected:
- `server/` — Core logic (C++)
- `clients/` — Hubs, warehouses, and delivery trucks (C)
- `common/` — Shared protocols & data structures
- `api/` — RESTful interface (Go)
- `database/` — SQL schema & seed data
- `scripts/` — Deployment scripts

---

## Credits

This project was developed for **Laboratory Work 1** of the course **Operating Systems II**, taught by **Engineer Gabriel Valenzuela** at the **Facultad de Ciencias Exactas, Físicas y Naturales (FCEFyN), Universidad Nacional de Córdoba (UNC)**.

Developed by **Juan Ignacio Sassi**.

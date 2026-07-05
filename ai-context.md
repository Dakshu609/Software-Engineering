# Cloud Gaming Console Platform (Software Engineering Project)

## Project Overview

This project is a **Software Engineering (SE)** academic project based on a **Cloud Gaming Console Platform**. The goal is to design and document a complete software system that allows users to play games hosted on cloud servers through a web application. The focus is on software engineering artifacts (SRS, UML, ER Diagram, DFD, Database Design, etc.) rather than implementing a real cloud gaming service.

> **Important:** The project simulates cloud gaming infrastructure. It does **not** implement actual game streaming like Xbox Cloud Gaming or NVIDIA GeForce NOW.

---

# Project Title

**Cloud Gaming Console Platform**

---

# Project Description

GameSphere Technologies is developing a web-based Cloud Gaming Console Platform that enables users to play games hosted on cloud servers without requiring high-end hardware.

Users can:

- Register and Login
- Browse available games
- Search games
- Launch games
- Save game progress
- Resume games from any device
- View gaming history
- Subscribe to premium plans

Administrators can:

- Manage users
- Manage games
- Manage cloud servers
- Monitor platform activities

The application is intended as a Software Engineering academic project and demonstrates complete software analysis and design.

---

# Scope

The project focuses on:

- Software Requirement Specification (SRS)
- Requirement Analysis
- Functional Requirements
- Non-Functional Requirements
- Use Case Diagram
- ER Diagram
- DFD
- Class Diagram
- Database Design
- Testing
- Documentation

Actual GPU cloud streaming is **not** implemented.

---

# Main Modules

## User Module

- Registration
- Login
- Profile Management
- Subscription
- Play Games
- Cloud Save
- Gaming History

---

## Game Module

- Browse Games
- Search Games
- View Game Details
- Launch Game
- Game Categories
- Ratings

---

## Server Module

- Allocate Cloud Server
- Host Games
- Monitor Server Load
- Server Status
- Region Management

---

## Admin Module

- Manage Users
- Add/Edit/Delete Games
- Manage Cloud Servers
- View Reports
- Monitor Sessions

---

# Functional Requirements

| ID | Requirement | Priority |
|----|-------------|----------|
| R1 | User Registration | High |
| R2 | User Login | High |
| R3 | Search Games | High |
| R4 | Launch Game | High |
| R5 | Cloud Save | High |
| R6 | Subscription Management | High |
| R7 | Gaming History | Medium |
| R8 | Admin Dashboard | High |

---

# Non-Functional Requirements

## Performance

- Available 24×7
- Support at least 200 concurrent users
- Search response within 2 seconds
- Game launch within 10 seconds

## Security

- Password hashing
- HTTPS communication
- Secure authentication
- Session timeout
- Protected cloud save data

## Reliability

- Recover interrupted sessions
- Preserve cloud save data

## Design Constraints

- Web-based application
- HTML5
- Modern browser support
- REST API architecture
- Relational Database

---

# Technology Stack

Frontend

- HTML5
- CSS3
- JavaScript
- React (optional)

Backend

- Node.js + Express

or

- Python + Flask/FastAPI

Database

- MySQL / PostgreSQL

---

# Identified Conceptual Classes

After requirement analysis, the following conceptual classes were identified.

Primary Classes

- User
- Game
- Server
- Admin

Additional Classes

- Subscription Plan
- Payment
- Gaming Session
- Cloud Save
- Gaming History
- Notification

---

# ER Diagram Design

The ER model follows **Chen Notation**.

## Entities

### USER

Attributes

- User_ID (Primary Key)
- Username
- Full_Name
- Email
- Password
- DOB
- Join_Date
- Subscription
- Account_Status
- Phone_No (Multivalued)
- Age (Derived)

---

### GAME

Attributes

- Game_ID (Primary Key)
- Game_Name
- Genre
- Developer
- Release_Date
- Rating
- File_Size
- Required_Plan
- Description

---

### SERVER

Attributes

- Server_ID (Primary Key)
- Server_Name
- Region
- IP_Address
- Capacity
- Current_Load
- GPU_Type
- RAM_Size
- Status

---

### ADMIN

Attributes

- Admin_ID (Primary Key)
- Admin_Name
- Email
- Password
- Phone_No
- Role
- Access_Level
- Last_Login

---

# ER Relationships

### USER — PLAYS — GAME

Relationship

PLAYS

Cardinality

Many-to-Many (M:N)

Meaning

A user can play multiple games, and a game can be played by multiple users.

---

### GAME — HOSTED_ON — SERVER

Relationship

HOSTED_ON

Cardinality

Many-to-One (M:1)

Meaning

Multiple games can be hosted on one cloud server.

---

### ADMIN — MANAGES — USER

Relationship

MANAGES

Cardinality

One-to-Many (1:N)

Meaning

One admin manages multiple users.

---

### ADMIN — MANAGES — GAME

Relationship

MANAGES

Cardinality

One-to-Many (1:N)

Meaning

One admin manages multiple games.

---

### ADMIN — MONITORS — SERVER

Relationship

MONITORS

Cardinality

One-to-Many (1:N)

Meaning

One admin monitors multiple cloud servers.

---

# ER Diagram Notation

The ER diagram must use standard Chen notation.

- Rectangle → Entity
- Ellipse → Attribute
- Double Ellipse → Multivalued Attribute
- Dashed Ellipse → Derived Attribute
- Underlined Attribute → Primary Key
- Diamond → Relationship
- Connectors → Relationships
- Cardinality → 1:1, 1:N, M:N

---

# Practical 3 (ER Modeling)

The practical follows the same writing style as the provided Library Information System practical.

It contains:

- Introduction
- Entity Identification
- User Entity
- Game Entity
- Server Entity
- Admin Entity
- Relationship Explanation
- Figure References

Figures

- Figure 1 — User Entity
- Figure 2 — Game Entity
- Figure 3 — Server Entity
- Figure 4 — Admin Entity
- Figure 5 — Complete ER Diagram

---

# Database Entities

Main tables include:

- Users
- Games
- Servers
- Admins
- GamingSessions
- CloudSaves
- SubscriptionPlans
- Payments
- GamingHistory
- Notifications

---

# Assumptions

- Users require an active subscription to launch premium games.
- Every game is hosted on one active cloud server.
- One cloud server can host multiple games.
- Administrators manage users, games, and servers.
- Passwords are stored using hashing algorithms.
- Cloud save data is linked to user accounts.
- Actual cloud streaming is simulated.

---

# Project Goal

The objective is to build a complete Software Engineering project with proper documentation and design artifacts rather than a production-ready cloud gaming platform.

The final deliverables should include:

- SRS
- Case Study
- Requirement Analysis
- Functional & Non-functional Requirements
- Use Case Diagram
- ER Diagram
- DFD
- Class Diagram
- Database Design
- Normalization
- Test Cases
- Gantt Chart
- Risk Analysis
- Final Documentation

---

# Important Instruction for Any AI

When generating future content for this project:

- Maintain consistency with the Cloud Gaming Console Platform domain.
- Use the entities **User**, **Game**, **Server**, and **Admin** as the core model.
- Follow Chen notation for ER diagrams.
- Keep all documentation in a formal Software Engineering report style similar to university practical manuals.
- Do not introduce unrelated entities unless necessary.
- Treat the platform as a **simulation of cloud gaming**, not a real game streaming infrastructure.
- Ensure all diagrams, database schemas, and documentation remain internally consistent with the requirements and ER model described above.

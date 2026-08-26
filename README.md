# Blood Bank Inventory & Emergency Donor Matcher

## Step 1 - Outcome

### 1. System Identified

**System:** Blood Bank Inventory & Emergency Donor Matcher

The system is intended to support real-time blood bank inventory management and emergency donor matching during critical blood shortages.

### 2. Actors Identified

| Actor | Interaction with the System |
|---|---|
| Emergency Requester | Raises an emergency blood request |
| Blood Bank Manager | Manages and monitors blood inventory |
| Donor | Receives/responds to emergency donation requests |
| SMS/Notification Service | Sends emergency SMS alerts |

The lab handout requires at least three actors for the UML use-case model. These four actors provide the required external participants.

### 3. Main System Functions Identified

The following candidate functions were extracted from the problem statement:

1. Submit an emergency blood request
2. Check real-time blood inventory
3. Match the requested blood type
4. Monitor blood-unit shelf life
5. Allocate blood units
6. Identify compatible donors
7. Check donor eligibility
8. Determine donor distance/radius
9. Send emergency notifications
10. Prevent duplicate allocation of a blood bag

These functions will later be used to derive the functional requirements and UML use cases.

### 4. Requirements Already Provided by the Problem Statement

#### FR-001 — Given Functional Requirement

**Description:**  
The system shall cross-reference emergency blood unit requests against real-time blood bank inventory and broadcast SMS alerts to compatible donors within a 10 km radius.

**Priority:** High

**Acceptance Criteria:**
- **Pass:** Compatible donors are notified within 30 seconds of the emergency flag.
- **Fail:** An incompatible blood group is alerted.

#### NFR-001 — Given Non-Functional Requirement

**Description:**  
The inventory ledger must maintain strict transactional consistency, preventing simultaneous allocation of the same blood bag.

The problem statement identifies this requirement under **Performance & Security**.

**Acceptance Criteria:**  
Benchmarking tests should confirm the required latency and security behavior under simulated peak load.

### 5. Requirements Structure for the Next Step

The final Requirements Table must contain exactly **7 requirements**:

#### Functional Requirements

- FR-001 — Given in the problem statement
- FR-002 — To be developed
- FR-003 — To be developed
- FR-004 — To be developed
- FR-005 — To be developed

#### Non-Functional Requirements

- NFR-001 — Given in the problem statement
- NFR-002 — To be developed

Therefore:

**5 Functional Requirements + 2 Non-Functional Requirements = 7 total requirements**

### 6. Step 1 Outcome

Step 1 establishes the system scope and provides the raw material for the requirements-engineering phase.

At the end of Step 1, we have:

- Identified the system.
- Identified the actors.
- Identified the major system functions.
- Identified the two requirements already supplied by the problem statement.
- Established the required structure of the final requirements table.

The next step is to construct the complete **Requirements Table** containing FR-001 to FR-005 and NFR-001 to NFR-002, with descriptions, priorities, measurable acceptance criteria, and rationales.

---

## Source

Based on:

- **Lab 1: Requirements Engineering & UML Use-Case Modelling — Student Handout**
- **Problem Statement #12 — Healthcare & Telemedicine: Blood Bank Inventory & Emergency Donor Matcher**

# Blood Bank Inventory & Emergency Donor Matcher

## Step 1 - Outcome

### 1. System Identified

**System:** Blood Bank Inventory & Emergency Donor Matcher

The system is intended to support real-time blood bank inventory management and emergency donor matching during critical blood shortages.

### 2. Actors Identified

| Actor | Interaction with the System |
|---|---|
| Emergency Requester | Raises an emergency blood request |
| Blood Bank Manager | Manages and monitors blood inventory |
| Donor | Receives/responds to emergency donation requests |
| SMS/Notification Service | Sends emergency SMS alerts |

The lab handout requires at least three actors for the UML use-case model. These four actors provide the required external participants.

### 3. Main System Functions Identified

The following candidate functions were extracted from the problem statement:

1. Submit an emergency blood request
2. Check real-time blood inventory
3. Match the requested blood type
4. Monitor blood-unit shelf life
5. Allocate blood units
6. Identify compatible donors
7. Check donor eligibility
8. Determine donor distance/radius
9. Send emergency notifications
10. Prevent duplicate allocation of a blood bag

These functions will later be used to derive the functional requirements and UML use cases.

### 4. Requirements Already Provided by the Problem Statement

#### FR-001 — Given Functional Requirement

**Description:**  
The system shall cross-reference emergency blood unit requests against real-time blood bank inventory and broadcast SMS alerts to compatible donors within a 10 km radius.

**Priority:** High

**Acceptance Criteria:**
- **Pass:** Compatible donors are notified within 30 seconds of the emergency flag.
- **Fail:** An incompatible blood group is alerted.

#### NFR-001 — Given Non-Functional Requirement

**Description:**  
The inventory ledger must maintain strict transactional consistency, preventing simultaneous allocation of the same blood bag.

The problem statement identifies this requirement under **Performance & Security**.

**Acceptance Criteria:**  
Benchmarking tests should confirm the required latency and security behavior under simulated peak load.

### 5. Requirements Structure for the Next Step

The final Requirements Table must contain exactly **7 requirements**:

#### Functional Requirements

- FR-001 — Given in the problem statement
- FR-002 — To be developed
- FR-003 — To be developed
- FR-004 — To be developed
- FR-005 — To be developed

#### Non-Functional Requirements

- NFR-001 — Given in the problem statement
- NFR-002 — To be developed

Therefore:

**5 Functional Requirements + 2 Non-Functional Requirements = 7 total requirements**

### 6. Step 1 Outcome

Step 1 establishes the system scope and provides the raw material for the requirements-engineering phase.

At the end of Step 1, we have:

- Identified the system.
- Identified the actors.
- Identified the major system functions.
- Identified the two requirements already supplied by the problem statement.
- Established the required structure of the final requirements table.

---

# Step 2 - Requirements Table

The following table contains exactly five Functional Requirements and two Non-Functional Requirements as required for Lab 1.

| Req ID | Type | Description | Priority | Acceptance Criteria | Rationale |
|---|---|---|---|---|---|
| **FR-001** | Functional | The system shall cross-reference emergency blood unit requests against real-time blood bank inventory and broadcast SMS alerts to compatible donors within a 10 km radius. | High | **Pass:** Compatible donors are notified within 30 seconds of the emergency flag.<br>**Fail:** An incompatible blood group is alerted. | Ensures timely notification of eligible donors and prevents alerts to incompatible donors during critical shortages. |
| **FR-002** | Functional | The system shall provide real-time monitoring of blood inventory, including blood group, component type, quantity, and expiry date. | High | **Pass:** Inventory data is updated in real time and available to users within 5 seconds of any change.<br>**Fail:** Inventory shows outdated or incorrect quantity/expiry information. | Accurate, up-to-date inventory visibility is critical for safe issue of blood and to avoid stock-outs. |
| **FR-003** | Functional | The system shall automatically identify compatible donors based on blood group compatibility, donor eligibility, and proximity within a 10 km radius. | High | **Pass:** Only eligible, compatible donors within 10 km are returned in the match list.<br>**Fail:** Ineligible or distant (>10 km) donors are shown in the match list. | Matches the right donors quickly to improve response time in emergencies. |
| **FR-004** | Functional | The system shall allow blood bank staff to record and update donor eligibility status based on donation history and medical criteria. | Medium | **Pass:** Eligibility status is updated and reflected across donor matching within 5 seconds.<br>**Fail:** Donors with expired/ineligible status remain available for matching. | Ensures only safe and eligible donors are contacted for emergencies. |
| **FR-005** | Functional | The system shall maintain and update shelf-life information for all blood components and trigger alerts for units nearing expiry. | Medium | **Pass:** Expiry alerts are generated for units within 24 hours to expiry.<br>**Fail:** Expired units are available for issue or no alert is generated. | Minimizes wastage and prevents issue of expired blood components. |
| **NFR-001** | Nonfunctional (Performance & Security) | The inventory ledger must maintain strict transactional consistency, preventing simultaneous allocation of the same blood bag. | High | **Pass:** Benchmarking tests confirm no duplicate allocation under peak load (1000 concurrent requests).<br>**Fail:** The same blood bag is allocated concurrently to multiple requests. | Protects patient safety and maintains trust in the system. |
| **NFR-002** | Nonfunctional (Availability) | The system shall maintain at least 99.5% uptime, measured monthly. | Medium | **Pass:** Monthly uptime logs show ≥ 99.5% availability.<br>**Fail:** Monthly uptime falls below 99.5%. | High availability is essential for life-critical emergency operations. |

### Requirements Summary

| Category | Count |
|---|---:|
| Functional Requirements | 5 |
| Non-Functional Requirements | 2 |
| **Total** | **7** |

---

## Source

Based on:

- **Lab 1: Requirements Engineering & UML Use-Case Modelling — Student Handout**
- **Problem Statement #12 — Healthcare & Telemedicine: Blood Bank Inventory & Emergency Donor Matcher**

````markdown
# Blood Bank Inventory & Emergency Donor Matcher

## Step 1 - Outcome

### 1. System Identified

**System:** Blood Bank Inventory & Emergency Donor Matcher

The system is intended to support real-time blood bank inventory management and emergency donor matching during critical blood shortages.

### 2. Actors Identified

| Actor | Interaction with the System |
|---|---|
| Emergency Requester | Raises an emergency blood request |
| Blood Bank Manager | Manages and monitors blood inventory |
| Donor | Receives/responds to emergency donation requests |
| SMS/Notification Service | Sends emergency SMS alerts |

The lab handout requires at least three actors for the UML use-case model. These four actors provide the required external participants.

### 3. Main System Functions Identified

The following candidate functions were extracted from the problem statement:

1. Submit an emergency blood request
2. Check real-time blood inventory
3. Match the requested blood type
4. Monitor blood-unit shelf life
5. Allocate blood units
6. Identify compatible donors
7. Check donor eligibility
8. Determine donor distance/radius
9. Send emergency notifications
10. Prevent duplicate allocation of a blood bag

### 4. Requirements Already Provided by the Problem Statement

#### FR-001 — Given Functional Requirement

**Description:**  
The system shall cross-reference emergency blood unit requests against real-time blood bank inventory and broadcast SMS alerts to compatible donors within a 10 km radius.

**Priority:** High

**Acceptance Criteria:**

- **Pass:** Compatible donors are notified within 30 seconds of the emergency flag.
- **Fail:** An incompatible blood group is alerted.

#### NFR-001 — Given Non-Functional Requirement

**Description:**  
The inventory ledger must maintain strict transactional consistency, preventing simultaneous allocation of the same blood bag.

**Type:** Performance & Security

**Acceptance Criteria:**  
Benchmarking tests should confirm the required latency and security behavior under simulated peak load.

---

# Step 2 - Requirements Table

| Req ID | Type | Description | Priority | Acceptance Criteria | Rationale |
|---|---|---|---|---|---|
| **FR-001** | Functional | The system shall cross-reference emergency blood unit requests against real-time blood bank inventory and broadcast SMS alerts to compatible donors within a 10 km radius. | High | **Pass:** Compatible donors are notified within 30 seconds of the emergency flag.<br>**Fail:** An incompatible blood group is alerted. | Ensures timely notification of eligible donors and prevents alerts to incompatible donors during critical shortages. |
| **FR-002** | Functional | The system shall provide real-time monitoring of blood inventory, including blood group, component type, quantity, and expiry date. | High | **Pass:** Inventory data is updated in real time and available to users within 5 seconds of any change.<br>**Fail:** Inventory shows outdated or incorrect quantity/expiry information. | Accurate, up-to-date inventory visibility is critical for safe issue of blood and to avoid stock-outs. |
| **FR-003** | Functional | The system shall automatically identify compatible donors based on blood group compatibility, donor eligibility, and proximity within a 10 km radius. | High | **Pass:** Only eligible, compatible donors within 10 km are returned in the match list.<br>**Fail:** Ineligible or distant (>10 km) donors are shown in the match list. | Matches the right donors quickly to improve response time in emergencies. |
| **FR-004** | Functional | The system shall allow blood bank staff to record and update donor eligibility status based on donation history and medical criteria. | Medium | **Pass:** Eligibility status is updated and reflected across donor matching within 5 seconds.<br>**Fail:** Donors with expired/ineligible status remain available for matching. | Ensures only safe and eligible donors are contacted for emergencies. |
| **FR-005** | Functional | The system shall maintain and update shelf-life information for all blood components and trigger alerts for units nearing expiry. | Medium | **Pass:** Expiry alerts are generated for units within 24 hours to expiry.<br>**Fail:** Expired units are available for issue or no alert is generated. | Minimizes wastage and prevents issue of expired blood components. |
| **NFR-001** | Nonfunctional (Performance & Security) | The inventory ledger must maintain strict transactional consistency, preventing simultaneous allocation of the same blood bag. | High | **Pass:** Benchmarking tests confirm no duplicate allocation under peak load (1000 concurrent requests).<br>**Fail:** The same blood bag is allocated concurrently to multiple requests. | Protects patient safety and maintains trust in the system. |
| **NFR-002** | Nonfunctional (Availability) | The system shall maintain at least 99.5% uptime, measured monthly. | Medium | **Pass:** Monthly uptime logs show ≥ 99.5% availability.<br>**Fail:** Monthly uptime falls below 99.5%. | High availability is essential for life-critical emergency operations. |

---

# Step 3 - UML Use-Case Diagram

## Actors

The UML use-case diagram contains the following actors:

1. **Emergency Requester**
2. **Blood Bank Manager**
3. **Donor**
4. **SMS / Notification Service** — external system

## Use Cases

| Use Case ID | Use Case |
|---|---|
| **UC-01** | Submit Emergency Blood Request |
| **UC-02** | Check Blood Inventory |
| **UC-03** | Identify Compatible Donors |
| **UC-04** | Manage Blood Inventory |
| **UC-05** | Monitor Donor Eligibility |
| **UC-06** | Send Emergency Notifications |
| **UC-07** | Respond to Donation Request |

## Actor Associations

| Actor | Associated Use Cases |
|---|---|
| **Emergency Requester** | UC-01 — Submit Emergency Blood Request |
| **Blood Bank Manager** | UC-02 — Check Blood Inventory; UC-04 — Manage Blood Inventory; UC-05 — Monitor Donor Eligibility |
| **Donor** | UC-07 — Respond to Donation Request |
| **SMS / Notification Service** | UC-06 — Send Emergency Notifications |

## UML Relationships

### `«include»`

**UC-01 → UC-02**

Submitting an emergency blood request includes checking the current blood inventory.

**UC-02 → UC-03**

The inventory-checking process includes identifying compatible donors when the available blood inventory is insufficient.

**UC-03 → UC-06**

Identifying compatible donors includes sending emergency notifications to the eligible matches.

### `«extend»`

**UC-07 → UC-06**

Responding to an emergency notification is optional behavior that occurs after an emergency notification has been sent.

---

## UML Diagram — Mermaid Representation

```mermaid
flowchart LR

    ER["Emergency Requester"]
    BM["Blood Bank Manager"]
    D["Donor"]
    SMS["SMS / Notification Service<br/><i>external system</i>"]

    subgraph SYS["Blood Bank Inventory & Emergency Donor Matcher System"]

        UC1(["UC-01<br/>Submit Emergency<br/>Blood Request"])
        UC2(["UC-02<br/>Check Blood Inventory"])
        UC3(["UC-03<br/>Identify Compatible<br/>Donors"])
        UC4(["UC-04<br/>Manage Blood Inventory"])
        UC5(["UC-05<br/>Monitor Donor Eligibility"])
        UC6(["UC-06<br/>Send Emergency<br/>Notifications"])
        UC7(["UC-07<br/>Respond to Donation<br/>Request"])

        UC1 -. "«include»" .-> UC2
        UC2 -. "«include»" .-> UC3
        UC3 -. "«include»" .-> UC6
        UC7 -. "«extend»" .-> UC6
    end

    ER --- UC1

    BM --- UC2
    BM --- UC4
    BM --- UC5

    D --- UC7

    SMS --- UC6
````

---

## Diagram Legend

| Symbol                        | Meaning                                     |
| ----------------------------- | ------------------------------------------- |
| Solid line                    | Association between an actor and a use case |
| Dashed arrow with `«include»` | Mandatory included behavior                 |
| Dashed arrow with `«extend»`  | Optional/conditional behavior               |
| Rectangle                     | System boundary                             |
| Oval                          | Use case                                    |
| Stick figure                  | Actor                                       |

---

## Step 3 Outcome

At the end of Step 3, the UML model contains:

* **4 actors**
* **7 use cases**
* Actor-to-use-case associations
* **3 `«include»` relationships**
* **1 `«extend»` relationship**
* A defined system boundary
* An external SMS/Notification Service

The diagram is ready to be created in **draw.io, Lucidchart, or another UML modelling tool** and exported as a PDF for the final Lab 1 submission.

---

## Source

Based on:

* **Lab 1: Requirements Engineering & UML Use-Case Modelling — Student Handout**
* **Problem Statement #12 — Healthcare & Telemedicine: Blood Bank Inventory & Emergency Donor Matcher**

````


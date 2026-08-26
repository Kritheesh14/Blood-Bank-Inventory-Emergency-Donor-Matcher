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

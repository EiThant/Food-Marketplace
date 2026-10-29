# Sprint 1 – Product Backlog and Sprint Plan

**Group 32 · Bristol Regional Food Network**
**Use Case 1:** Producer Product Listing and Inventory Management
**Prepared by:** Arda Pekar

## 1. Initial Product Backlog

Nine user stories, all from the producer's point of view. Each story has an acceptance criterion so we know when it is done.

- **Functionality A – Product Listing & Validation:** stories 1–5
- **Functionality B – Inventory & Seasonal Availability:** stories 6–9
- **Priority:** High = the marketplace cannot work without it; Medium = builds on other stories

| # | As a producer, I want… | Acceptance criterion | Function | Priority |
|---|---|---|---|---|
| 1 | to add a new product to the marketplace | All mandatory fields are captured (name, description, category, price, quantity, availability period, farm origin) | A · Listing | High |
| 2 | the system to validate product information | Missing or invalid fields are rejected with a clear message | A · Listing | High |
| 3 | organic certification to be verified | Organic claims are checked by the external / simulated service | A · Listing | High |
| 4 | to correct invalid product information | I can edit and resubmit; only valid listings are published | A · Listing | High |
| 5 | to be told if certification cannot be checked | The listing is held, I am informed and the check is retried | A · Listing | High |
| 6 | to update stock quantity | The new quantity is saved and shown to customers | B · Inventory | High |
| 7 | zero-stock products to become unavailable automatically | At zero stock the product cannot be ordered | B · Inventory | High |
| 8 | to manage seasonal availability | The product is only shown inside its availability period | B · Inventory | High |
| 9 | replenished products to become available again | Restocked and in season → available again | B · Inventory | Medium |

**Summary:** 9 stories – 8 High, 1 Medium. Story 5 covers the exception path required by Use Case 1.

## 2. Sprint Plan and Responsibilities

| Sprint | Deliverable | Owner | Status |
|---|---|---|---|
| Sprint 1 (12 Oct) | Stakeholder analysis and case overview | Cem Basogul | Done |
| | Major business processes and strategic BPMN | Aye Thiri Mon | In review |
| | Product backlog and sprint plan | Arda Pekar | Done |
| | Two candidate major functionalities | Ei Ei Thant | Awaiting approval |
| | Meeting notes, GitHub and contribution evidence | Ogan Bertun Alpaydin | Ongoing |
| Sprint 2 (2 Nov) | i* Strategic Dependency and Strategic Rationale models | [add owner] | Planned |
| | Operational BPMN — Functionality A | [add owner] | Planned |
| | Operational BPMN — Functionality B | [add owner] | Planned |
| | Initial Camunda processes, user tasks and Forms | [add owner] | Planned |
| Sprint 3 (23 Nov) | End-to-end Camunda automation, service tasks, integration, LESP, final demo | All members | Planned |

Weekly stand-ups track progress; all work is versioned on GitHub. Final submission: **10 December 2026, before 14:00**.

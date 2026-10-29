# Sprint 1 Meeting Notes

| | |
|---|---|
| Project | Bristol Regional Food Network – Digital Marketplace |
| Module | UFCFTR-30-3 Distributed and Enterprise Software Development, Task 1 |
| Group | 32 |
| Date | [23/10/2026] |
| Present | all five members |
| Absent | [none] |
| Notes by | Ogan Bertun Alpaydin |

## Agenda

1. Case study and which use case we take
2. Stakeholders
3. Business processes and the strategic BPMN
4. Two candidate functionalities
5. Backlog and sprint plan
6. Who does what

## 1. Case study and use case

The marketplace links local food producers with customers within 20 miles of Bristol city centre. We are taking Use Case 1: Producer Product Listing and Inventory Management. It covers adding products, validating the details, checking organic certification, stock levels and seasonal availability.

## 2. Stakeholders

We went through the case study and agreed on five stakeholders for our use case:

- **Producer** – adds products, updates stock and sets seasonal availability. Technical skills vary a lot, so updates need to be quick and simple.
- **Marketplace system** – validates product details, publishes valid listings and keeps availability up to date.
- **Certification service** (external or simulated) – checks organic claims. It might not always be available, so we need to think about what happens then.
- **Customer** – sees published products and whether they're available.
- **Administrator** – looks after marketplace operations and food safety issues.

Customer segments from the case study: young professionals and families, community groups (schools, care homes, voluntary groups) and independent restaurants and cafés. The payment provider comes in when customers order, which is outside our use case.

## 3. Business processes and strategic BPMN

We listed the main processes of the whole marketplace:

1. Manage product listings and inventory (our use case)
2. Manage customer orders
3. Process payments and settlements (including the 5% commission)
4. Manage food safety and traceability
5. Communicate with customers and producers

Points raised about the BPMN draft:

- The strategic BPMN has to show the whole enterprise at a high level, not just our use case. The current draft only shows the listing flow, so we need an enterprise-level diagram as well.
- External Service is a lane in the same pool at the moment. That means the links are sequence flows, not message flows. We'll make it a separate pool in the operational model.
- Camunda is showing two warnings on the diagram. These need fixing.
- Ask the tutor if the level of detail is right before finalising.
- Diagrams must be drawn by us. The brief says AI-generated diagrams count as plagiarism.

## 4. Two candidate functionalities

**A. Product Listing and Validation** – producer enters product details, system checks required fields and dates, organic claims go to the certification service, invalid data goes back for correction, valid listings are published.

**B. Inventory and Seasonal Availability** – producer updates stock and availability dates, products are hidden at zero stock and come back when restocked in season.

Why these two: they're linked but do different jobs. A gets listings right, B keeps them current. Both have user tasks, automated checks, decisions and exception paths, which we'll need for Camunda later.

The brief says the module team has to agree the functionalities before we start detailed work. Possible question from the tutor: both come from the same use case, so we should be ready to explain the split.

## 5. Backlog and sprint plan

- Backlog written as user stories from the producer's side, each with a priority and an acceptance criterion.
- Stories are linked to functionality A or B.
- Sprint plan lists each deliverable with an owner and status. Sprint 2 owners to be decided at the Sprint 2 planning meeting.

## 6. Decisions

| Decision | Status |
|---|---|
| Use Case 1: Producer Product Listing and Inventory Management | Agreed |
| Five stakeholders as listed in section 2 | Agreed |
| Five main business processes for the strategic BPMN | Agreed |
| Two Functionalities | Agreed |
| All work kept on GitHub, each member commits from their own account | Agreed |
| Sprint 1 owners as in section 7 | Agreed |

## 7. Sprint 1 owners

| Member | Deliverable | Deadline | Status |
|---|---|---|---|
| Cem Basogul | Stakeholder analysis, case overview | Before Sprint 1 review | |
| Ei Ei Thant| Business processes, strategic BPMN | Before Sprint 1 review | |
| Arda Pekar | Product backlog, sprint plan | Before Sprint 1 review | |
| Aye Thiri Mon | Two candidate functionalities | Before Sprint 1 review | |
| Ogan Bertun Alpaydin | Meeting notes, GitHub and contribution evidence | Before Sprint 1 review | |

## 8. Actions

Action | Owner | Due |
|---|---|---|
| Confirm the two functionalities with the tutor | Ei | Before Sprint 2 (2 Nov) |
| Draw the enterprise-level strategic BPMN and fix the Camunda warnings | Aye | Before Sprint 2 (2 Nov) |
| Rename the BPMN file in the repo (currently "New BPMN diagram.bpmn") | Aye | Before Sprint 2 (2 Nov) |
| Commit own Sprint 1 work from own GitHub account with a clear message | Everyone | Before Sprint 1 review |
| Upload these notes | Bertun | Same day |
| Add the module team to the private repo, or ask how they want access | Ei | Before Sprint 2 (2 Nov) |
| Ask the module team if the Contribution Matrix rows should be changed for Camunda work (template is written for Django) | Bertun | Before Sprint 2 (2 Nov) |

## Key dates

| | |
|---|---|
| Sprint 2 (30%) | from 2 November 2026 |
| Sprint 3 and final demo (50%) | from 23 November 2026 |
| Final repository submission | 10 December 2026, before 14:00, no late window |

## Next meeting

* **Date:** [03/11/2026]
* **Agenda:** check actions above, tutor feedback on A and B, BPMN changes, Sprint 2 owners and deadlines 

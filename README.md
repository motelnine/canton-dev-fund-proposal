# Development Fund Proposal

| Field | Value |
| --- | --- |
| Author | Token Path LLC — Nico R. Willis, Managing Director |
| Org | Token Path LLC |
| Status | Proposed — Foundation review pending |
| Created | 2026-11-05 |
| Funding request | 1,900,000 Canton Coin (CC) |
| Initial milestone | 350,000 CC |
| Delivery period | 24 weeks |
| Project | Canton Open Tax-Lot Interoperability and Proof-of-Basis Reference Infrastructure |

## Executive Summary

### Establishing an Open Economic and Tax-Intelligence Infrastructure Layer for Canton

Canton is establishing the infrastructure through which regulated financial assets can be issued, held, transferred and settled in distributed-ledger environments. As institutional adoption expands, an essential capability must accompany the ownership record: a reliable means of preserving and verifying the economic and tax history of each investment across its lifecycle.

Tokenization changes the mechanisms for recording and transferring securities; it does not remove the underlying requirements for adjusted cost basis, tax-lot accounting, corporate actions, dividend and income classification, wash-sale analysis, regulatory tax reporting, proxy voting and voluntary corporate-action elections. These latter two workflows also require accurate entitlement records, deadlines, authorized instructions and auditable outcomes. Those functions generally reside in established financial systems and do not automatically move with a tokenized security or its settlement event.

Token Path LLC proposes to develop an **open-source, Canton-native tax-lot interoperability and Proof-of-Basis reference framework**. The framework will enable appropriately authorized Canton applications to request economic calculations from external providers, receive standardized references and signed evidence, verify data provenance, and reconcile the resulting information with relevant ledger activity. Confidential taxpayer and investment-level data will remain off-ledger under institutional access controls.

The project also proposes a provider-neutral governance and election-event extension that links authorized holdings and record-date entitlements to proxy-voting instructions and voluntary corporate-action elections. It will track event references, eligibility, instruction status, deadlines and acknowledgments without replacing regulated voting agents, custodians or corporate-action processing systems.

The project is designed as shared ecosystem infrastructure, not a proprietary tax-calculation service. Its reference implementation will operate with a public deterministic mock provider and documented interfaces, allowing Canton developers and independent institutions to adopt the framework without a Netbasis license or commercial relationship with Token Path.

**Requested decision:** Conditional authorization of the first 350,000 CC milestone within a proposed five-stage, 24-week program totaling up to 1,900,000 CC. Each subsequent tranche would require objective technical evidence and the Foundation's applicable approval process.

### Strategic Foundation

Token Path draws on the institutional cost-basis and tax-intelligence experience associated with Netbasis, developed by NetWorth Services.

Netbasis supports sophisticated tax-lot accounting, cost-basis adjustments, corporate actions, dividend processing and complex wash-sale calculations across traditional financial assets.

This experience informs the design of the proposed integration framework, its calculation references and its auditability requirements; it does not establish that the proposed Canton components have already been implemented.

Grant-funded software will be provider-neutral and independently executable using publicly documented reference components. Existing Netbasis algorithms, licensed datasets and customer implementations will remain outside the funded deliverables.

## Problem Statement

### The Missing Economic Data Layer

Tokenized securities require more than an accurate ownership record.

Throughout an investment's lifecycle, economic events can alter its tax basis, ownership attributes, income classification and reporting obligations.

These events include:

- Purchases, sales and partial dispositions.
- Fractional tax-lot allocations and adjustments.
- Stock splits, mergers, reorganizations and other corporate actions.
- Voluntary corporate-action elections, including tender, exchange and optional consideration elections.
- Proxy-voting notices, record-date entitlements, voting instructions and vote-status reconciliation.
- Dividend distributions and income reclassifications.
- Wash-sale adjustments and deferred losses.
- Transfers between custodians, institutions and authorized ownership environments.

Although Canton can support regulated asset workflows, the associated economic calculations frequently remain in separate off-ledger systems.

Without a standardized integration framework, institutions must independently develop mechanisms to connect these calculations with tokenized asset activity.

This fragmentation creates duplicated development costs, inconsistent data interfaces, reconciliation challenges and difficulties preserving historical economic information across institutional boundaries.

### Proposed Solution

Token Path proposes a reusable Canton-native reference architecture linking authorized ledger events with qualified off-ledger economic-data providers through a common, versioned interface.

The reference implementation will demonstrate standardized calculation requests, authenticated provider responses, cryptographically verifiable evidence, tax-lot references and structured reconciliation workflows.

Sensitive taxpayer information and detailed investment records will remain off-ledger unless explicitly authorized for disclosure.

## Project Objectives

The project will pursue seven principal objectives.

**Objective 1 — Establish a Canton Tax-Lot Interoperability Standard**

Develop standardized Daml contracts, event schemas and API specifications for exchanging economic and tax-lot references between Canton applications and authorized calculation providers.

**Objective 2 — Enable Real-Time Economic Data Synchronization**

Provide a reference mechanism for connecting issuance, transfers, dispositions, corporate actions and dividend events with corresponding tax-lot and cost-basis processing.

**Objective 3 — Introduce Verifiable Proof-of-Basis**

Develop cryptographically signed attestations establishing the provenance, integrity, calculation reference and version history of tax-basis information.

**Objective 4 — Preserve Institutional Privacy**

Use Canton authorization controls and off-ledger storage to ensure sensitive investment and taxpayer information is accessible only to appropriately authorized parties.

**Objective 5 — Support Multiple Calculation Providers**

Publish provider-neutral interfaces allowing qualified third-party tax engines and institutional data services to integrate without relying on proprietary Netbasis technology.

**Objective 6 — Support Proxy Voting and Corporate-Action Elections**

Define optional, provider-neutral event and instruction schemas for record-date voting entitlements, proxy materials, voting instructions, election options, cutoff times, acknowledgments and outcome reconciliation. Authorization will be enforced and the reference implementation will not independently determine beneficial ownership or execute votes and elections on behalf of an institution.

**Objective 7 — Accelerate Canton Ecosystem Adoption**

Deliver documented, open-source infrastructure that reduces the cost and complexity of implementing economic and tax-data continuity across Canton applications.

## Implementation Mechanics

![Canton Daml authorization matrix](assets/attachment-1/figure-2.png)

*Figure 1. Daml authorization matrix reproduced from the technical architecture attachment; detailed controls and contract choices remain specified in Attachment 2.*


The framework will consist of five core components and a proposed governance/election extension. The extension will reuse the authorization, evidence and reconciliation services while preserving distinct operational and legal workflows.

### Component A — Canton Smart Contract Layer

Develop reusable Daml templates and workflows representing:

- Oracle requests and responses.
- Tax-lot references.
- Cost-basis adjustment references.
- Corporate-action notifications.
- Dividend and income events.
- Proxy meeting notices, record-date entitlement references and voting-instruction status.
- Voluntary corporate-action election notices, option selections and instruction status.
- Proof-of-Basis attestations.
- Reconciliation exceptions.

The contracts will enforce authorization through appropriate Canton party roles, signatories, observers and controllers.

### Governance and Corporate-Action Election Extension

A separately scoped extension will expose canonical event references and authorized instruction workflows for proxy voting and voluntary corporate-action elections. It will support record-date and beneficial-entitlement references, distribution of notices and materials, ballot or election options, cutoff timestamps, revocations or amendments where permitted, submission receipts, status updates and final reconciliation. It will provide integration hooks for existing proxy service providers, transfer agents, custodians and corporate-action agents, rather than attempting to replace their legal responsibilities. The reference mock provider will simulate instructions and acknowledgments; live submission requires an authorized external provider and any necessary permissions.

### Component B — Oracle Coordination Layer

An off-ledger oracle coordinator will connect authorized Canton events to calculation-provider services.

Its responsibilities will include event ingestion, request validation, authorization checks, idempotency, retries, correlation identifiers, durable checkpoints and exception handling.

The coordinator will maintain traceable relationships between ledger events and economic-data responses.

### Component C — Provider-Neutral Calculation Interface

A standardized API and adapter framework will support external calculation providers.

The reference implementation will include a deterministic mock provider capable of executing representative basis-adjustment, tax-lot, dividend and corporate-action scenarios.

An optional Netbasis adapter may demonstrate institutional-grade calculation integration, but the publicly funded framework will remain fully functional without Netbasis credentials, licenses or proprietary data.

### Component D — Proof-of-Basis Attestation

The framework will generate verifiable evidence manifests containing relevant calculation identifiers, version information, timestamps, provider identities, input/output commitments and cryptographic signatures.

These attestations will allow authorized parties to verify that referenced calculation information originated from an identified provider and has not been altered.

Proof-of-Basis establishes attribution and data integrity; it does not independently certify the legal correctness of a tax calculation.

### Component E — Reconciliation and Audit Infrastructure

The system will include tools for detecting and resolving missing events, duplicate messages, mismatched records, stale references and calculation exceptions.

Audit records will support authorized investigation and reproducible testing without exposing confidential information to unauthorized network participants.

## Architectural Alignment and Open-Source Commitment

The primary beneficiaries of the proposed infrastructure will be Canton developers and institutional network participants.

Grant-funded deliverables will include:

1. Reusable Daml contracts and authorization examples.
2. Publicly documented API and data schemas.
3. Ledger event adapters and oracle middleware.
4. Provider-neutral SDKs and a deterministic mock calculation provider.
5. Proof-of-Basis signing and verification libraries.
6. Reconciliation and exception-handling utilities.
7. Automated tests and security documentation.
8. Containerized deployment examples and developer documentation.

Token Path proposes Apache-2.0 licensing for newly developed grant-funded software, subject to final legal review.

The project will maintain a clear distinction between publicly funded components and pre-existing proprietary intellectual property.

Netbasis algorithms, proprietary financial datasets, existing commercial products, private customer implementations and Token Path's broader cross-chain services are excluded from the grant scope.

No participant will be required to purchase a Netbasis license to use the open-source reference framework.

## Institutional Use Cases

![Exhibit 2E — Proxy voting and voluntary corporate-action election lifecycles](assets/attachment-1/exhibit-2e-event-lifecycles.svg)

*Exhibit 2E. Proposed proxy-voting and voluntary corporate-action election lifecycles. Authorized agents remain responsible for instruction execution and final outcomes.*


### Use Case 1 — Tokenized Security Issuance

An authorized application establishes an economic-data reference for newly issued tokenized securities, allowing subsequent ownership and lifecycle events to be associated with a consistent record.

### Use Case 2 — Security Transfers and Tax-Lot Continuity

When a tokenized security transfers between authorized parties, the oracle framework enables appropriate tax-lot references and economic-data commitments to be preserved and reconciled.

### Use Case 3 — Corporate Actions

Stock splits, mergers and reorganizations trigger standardized economic-data workflows that allow relevant cost-basis and quantity adjustments to be calculated by an authorized provider and referenced within Canton.

### Use Case 4 — Dividend and Income Processing

Dividend events can be associated with income classifications, relevant record and payment dates, and subsequent adjustments or reclassifications.

### Use Case 5 — Proxy Voting and Governance Participation

For an authorized tokenized-security holding, the framework can associate a proxy meeting notice and record-date entitlement reference with a voting-instruction request. The authorized intermediary or voting agent remains responsible for validating eligibility, distributing materials, accepting and executing instructions, and reporting outcomes. The open reference workflow records permissioned status updates, evidence references and reconciliation exceptions, including fractional or omnibus holdings where applicable.

### Use Case 6 — Voluntary Corporate-Action Elections

Tender offers, exchange offers, optional cash-or-stock consideration and similar events can be represented through versioned notices, eligible position references, election options, deadlines, authenticated instructions and provider acknowledgments. The workflow will support instruction amendments or withdrawals only when the underlying event rules permit them and will reconcile election outcomes with subsequent position and cost-basis adjustments.

### Use Case 7 — Proof-of-Basis and Audit Verification

Authorized participants can validate signed economic-data commitments and identify the provider, calculation version and relevant event history supporting a tax-lot reference.

### Use Case 8 — Exception Management

The framework detects missing, duplicated or inconsistent economic-data responses and produces structured reconciliation records for institutional review.

## Canton Ecosystem Benefits

The initiative is intended to produce measurable benefits beyond Token Path's commercial operations.

**Reduced Development Duplication:** Canton participants can adopt common interfaces rather than building separate oracle integrations for each application.

**Improved Interoperability:** Standardized tax-lot references and calculation requests enable multiple providers and applications to participate in common workflows.

**Institutional Readiness:** The framework addresses operational requirements that become increasingly important as traditional securities and their lifecycle events migrate to distributed ledger infrastructure.

**Privacy-Preserving Verification:** Canton applications can verify authorized economic-data commitments without exposing complete investment histories or taxpayer records on a broadly accessible ledger.

**Governance and Election Interoperability:** Common entitlement and instruction references can reduce integration duplication for proxy voting and voluntary corporate-action elections while leaving execution and legal validation with authorized intermediaries.

**Expanded Developer Capabilities:** Public SDKs, schemas, demonstrations and test fixtures will lower barriers to building financial applications requiring tax and economic intelligence.

**Long-Term Ecosystem Utility:** The resulting infrastructure can support additional calculation providers, applications and institutional workflows beyond the initial project.

## Ecosystem Adoption and Validation

Token Path proposes to engage at least two independent Canton ecosystem participants during development.

The preferred participant categories are:

- An issuer, tokenization platform or application developer.
- A custodian, transfer agent, broker-dealer or other institutional infrastructure provider.

Before requesting second-stage funding, Token Path will seek written expressions of interest identifying the proposed integration use case, technical contact, testing environment and expected participation.

These expressions of interest will be documented as development commitments or evaluation intentions, not as paying customers unless supported by executed commercial agreements.

The final project milestone will require two independently verifiable integration demonstrations or pilot implementations.

Where commercial confidentiality prevents public identification, independent verification arrangements will be agreed with the Foundation.

## Milestones and Deliverables

The project will be delivered over 24 weeks through five independently reviewable milestones.

### Milestone 1 — Architecture and Feasibility

**Duration:** Weeks 1–4

**Funding:** 350,000 CC

Deliverables:

- Final reference architecture.
- Daml authorization and contract specifications.
- Canonical data schemas.
- Initial Proof-of-Basis evidence model.
- Open-source repository and IP provenance register.
- Deterministic mock-provider prototype.
- Threat model and preliminary security controls.
- Named technical delivery resources and documented cost estimates.

**Acceptance Criteria:** Independent reviewers can reproduce the initial reference workflow, inspect the public interfaces and validate that no proprietary Netbasis dependency is required.

### Milestone 2 — Oracle Integration and Tax-Lot Workflow

**Duration:** Weeks 5–10

**Funding:** 475,000 CC

Deliverables:

- Canton Ledger API event consumer.
- Durable oracle coordinator.
- Calculation-provider interface and SDK.
- Basis-adjustment request/response workflow.
- Proof-of-Basis signature generation and verification.
- Automated authorization, replay and idempotency tests.
- At least two documented independent ecosystem expressions of interest.

**Acceptance Criteria:** A reproducible end-to-end demonstration connects an authorized Canton event with a provider-neutral calculation response and verifiable evidence commitment.

### Milestone 3 — Corporate Actions, Dividends and Reconciliation

**Duration:** Weeks 11–16

**Funding:** 475,000 CC

Deliverables:

- Corporate-action processing references, including voluntary election notices, options and instruction-status schemas.
- Dividend and income-event workflows.
- Proxy meeting, record-date entitlement and voting-instruction reference workflows with deterministic mock acknowledgments.
- Fractional tax-lot adjustment examples.
- Reconciliation and exception-management utilities.
- Event replay, duplicate detection and mismatch testing.
- Updated technical documentation and test fixtures.

**Acceptance Criteria:** Independent reviewers can execute representative corporate-action, dividend, proxy-voting and voluntary election scenarios using mock providers, including deadline, duplicate-instruction and authorization failures, and reproduce exception-handling results.

### Milestone 4 — Security, Resilience and Deployment

**Duration:** Weeks 17–20

**Funding:** 350,000 CC

Deliverables:

- Independent security assessment.
- Authorization and privacy validation.
- Key-management and signature-verification controls.
- Performance and fault-recovery testing.
- Deployment automation and operational runbooks.
- Remediation of identified critical and high-severity security findings.

**Acceptance Criteria:** Independent security review is completed, critical and high-severity findings are resolved or formally accepted under agreed controls, and the reference implementation can be reproducibly deployed.

### Milestone 5 — Ecosystem Integration and Handover

**Duration:** Weeks 21–24

**Funding:** 250,000 CC

Deliverables:

- Two independently verifiable external integrations or pilot demonstrations, potentially including a governance or corporate-action election workflow where an authorized participant elects to test one.
- Final public release of the reference framework.
- Developer integration guides.
- Technical workshops and example applications.
- Public issue tracking and contribution documentation.
- Twelve-month maintenance and governance plan.

**Acceptance Criteria:** Two independent Canton participants demonstrate use of the common interfaces, and the final reference implementation is publicly documented and independently reproducible.

## Funding Request and Payment Breakdown

Token Path requests a **maximum allocation of 1,900,000 CC** over 24 weeks. The proposed distribution below aligns funding with discrete engineering, security and ecosystem-validation deliverables. The allocation is a funding request, not an assertion of approved expenditures.

| Milestone | Target completion | Requested funding | Share of request |
|:--|:--|--:|--:|
| M1 — Architecture and feasibility | Week 4 | 350,000 CC | 18.42% |
| M2 — Oracle and tax-lot integration | Week 10 | 475,000 CC | 25.00% |
| M3 — Corporate actions and reconciliation | Week 16 | 475,000 CC | 25.00% |
| M4 — Security, resilience and deployment | Week 20 | 350,000 CC | 18.42% |
| M5 — Ecosystem adoption and handover | Week 24 | 250,000 CC | 13.16% |
| **Total** | **24 weeks** | **1,900,000 CC** | **100.00%** |

### Proposed Authorization Structure

Token Path seeks **initial conditional authorization of 350,000 CC for Milestone 1**. The remaining **1,550,000 CC** would be considered only after the applicable milestone evidence, technical review and Foundation approvals. This staged structure limits initial exposure and provides explicit continuation checkpoints.

### Budget Accountability

Before grant contracting, Token Path will submit a supporting USD-denominated cost schedule covering:

- Canton/Daml engineering.
- Oracle middleware and API development.
- Security and privacy engineering.
- Infrastructure, testing and deployment.
- Developer documentation and ecosystem integration.
- Independent security review.
- A separately controlled contingency allowance.

The budget will identify personnel commitments, estimated hours, loaded rates, vendor quotations and the agreed CC valuation methodology.

No unsupported CC/USD conversion assumption is included in this proposal.

Funding will not be used to acquire or develop proprietary Netbasis algorithms or to subsidize unrelated commercial Token Path activities.

## Project Team and Delivery Governance

**Executive Sponsor:** Nico R. Willis, Managing Director, Token Path LLC.

**Technical Delivery Lead:** To be named before contracting.

**Canton/Daml Engineering:** Qualified engineering resources to be identified and committed before project commencement.

**Oracle and API Engineering:** Dedicated backend integration resources to be identified.

**Security Review:** Independent specialist or firm to be engaged before Milestone 4.

**Ecosystem Integration Coordination:** Designated project lead responsible for independent adopter engagement and pilot execution.

### Governance

Token Path will establish a structured delivery and reporting process including:

- Weekly engineering progress updates.
- Monthly technical demonstrations.
- Public issue and risk tracking.
- Version-controlled deliverables.
- Milestone acceptance reports.
- Documented security findings and remediation.
- Transparent financial reporting against the approved project budget.

Foundation representatives and designated independent technical reviewers will be provided appropriate access to review funded deliverables.

## Security and Privacy Framework

![Canton infrastructure deployment and security](assets/attachment-1/figure-6.png)

*Figure 2. Reference infrastructure deployment and security boundaries; proposed design, not a live deployment.*

![Exhibit 2D — Governance and election trust boundaries](assets/attachment-1/exhibit-2d-trust-boundaries.svg)

*Exhibit 2D. Proposed proxy-voting and voluntary-election trust boundaries, separating Canton references from restricted off-ledger records.*


The project will be designed around the security and confidentiality requirements of institutional financial applications.

Key controls will include:

**Authorization:** Daml signatory, observer and controller models, together with appropriately scoped participant permissions.

**Data Minimization:** Sensitive account, taxpayer and detailed tax-lot information will remain off-ledger unless disclosure is specifically authorized.

**Cryptographic Integrity:** Signed evidence manifests, domain-separated hashes, version identifiers and replay protection.

**Operational Security:** Encrypted transport, managed keys, least-privilege access, logging controls and secure deployment configurations.

**Resilience:** Durable processing checkpoints, retry handling, exception queues and recovery procedures.

**Independent Review:** Security testing and remediation before final deployment acceptance.

The governance and election extension will not imply that a signed instruction was legally valid, accepted by the tabulator, or executed by the relevant agent. Eligibility, cutoffs, beneficial ownership and final vote or election execution remain subject to the authorized service provider and applicable rules.

The framework will not represent a cryptographic signature as proof that an underlying tax calculation is legally correct. Calculation accuracy remains the responsibility of the relevant provider and its supporting data.

## Sustainability and Backward Compatibility

Token Path proposes to maintain the grant-funded reference implementation for at least 12 months following final acceptance, subject to the grant agreement.

Maintenance activities will include security updates, compatibility testing, issue triage, documentation improvements and periodic public releases.

The repository will include contributor guidance, a security disclosure policy and a maintainer succession plan.

The architecture will remain provider-neutral so additional ecosystem participants can contribute adapters, test cases and extensions.

Commercial services offered separately by Token Path or other providers will not be prerequisites for using the publicly funded toolkit.

## Project Risks and Mitigation

**Ecosystem Adoption Risk:** Independent participation will be demonstrated through documented expressions of interest before second-stage funding and external integration evidence at project completion.

**Execution Risk:** Named engineering resources, staffing commitments and delivery responsibilities will be required before contracting.

**Budget Risk:** Funding will be tied to an itemized budget, an agreed CC valuation methodology and milestone acceptance.

**Proprietary Dependency Risk:** The reference implementation must function using a public mock provider without a Netbasis license.

**Privacy Risk:** Sensitive information will remain off-ledger, with authorized disclosure controls and independent security testing.

**Technical Integration Risk:** Canton compatibility, event replay, error recovery and versioned interfaces will be tested through reproducible scenarios.

**Long-Term Maintenance Risk:** A twelve-month maintenance commitment and third-party contribution process will be established.

## Acceptance Criteria and Success Metrics

Project success will be measured through verifiable ecosystem outputs rather than Token Path commercial revenue or Canton Coin rewards.

The principal success measures are:

1. A publicly accessible and documented open-source implementation.
2. A complete reference workflow operating without proprietary Netbasis services.
3. Reproducible Canton authorization, oracle-request and Proof-of-Basis verification tests.
4. Working corporate-action, dividend, proxy-voting, voluntary-election and reconciliation reference examples.
5. Completion of independent security assessment and required remediation.
6. Two independently verifiable external integrations or pilot demonstrations.
7. Publication of developer documentation, test fixtures and maintenance commitments.

Detailed throughput and latency targets will be baselined during Milestone 1 and approved before Milestone 2.

## Requested Foundation Decision

Token Path LLC requests the Canton Foundation’s consideration of the proposed open-source infrastructure initiative and **conditional authorization of 350,000 CC for Milestone 1**, within a maximum proposed funding envelope of **1,900,000 CC over 24 weeks**.

Milestone 1 will establish the architecture, authorization model, canonical interfaces, public development baseline and independently reproducible feasibility evidence needed to evaluate continued funding.

Authorization of later milestones will remain contingent on independently reviewable technical progress, documented ecosystem participation and successful acceptance of the relevant deliverables.

The initiative is intended to provide Canton with a reusable economic and tax-data interoperability framework that strengthens institutional tokenized-asset infrastructure while preserving privacy, provider choice and open development.

**Token Path's objective is to make verifiable economic and tax-lot continuity a reusable infrastructure capability across the Canton ecosystem.**

## Supporting Technical Attachments

The following documents accompany the Proposal and provide the detailed technical, operational and governance material referenced in this proposal:

| Attachment | Supporting document | Link |
|:--:|:--|:--|
| 2 | Detailed Technical Architecture, Authorization and Trust Model (including Exhibits 2A–2E) | [2026-11-tokenpath-02-attachment-2-detailed-technical-architecture.md](https://github.com/motelnine/canton-dev-fund-proposal/blob/main/docs/2026-11-tokenpath-02-attachment-2-detailed-technical-architecture.md) |
| 3 | Canonical Data and API Specifications | ([2026-11-tokenpath-03-attachment-3-canonical-data-and-api-specifications.md](https://github.com/motelnine/canton-dev-fund-proposal/blob/main/docs/2026-11-tokenpath-03-attachment-3-canonical-data-and-api-specifications.md) |
| 4 | Daml Contracts, Oracle Integration and Test Plan | [2026-11-tokenpath-04-attachment-4-daml-contracts-oracle-integration-test-plan.md](https://github.com/motelnine/canton-dev-fund-proposal/blob/main/docs/2026-11-tokenpath-04-attachment-4-daml-contracts-oracle-integration-test-plan.md) |
| 5 | Security, Privacy, Deployment and Resilience Plan | [2026-11-tokenpath-05-attachment-5-security-privacy-deployment-resilience-plan.md](https://github.com/motelnine/canton-dev-fund-proposal/blob/main/docs/2026-11-tokenpath-05-attachment-5-security-privacy-deployment-resilience-plan.md)|
| 6 | Detailed Budget, Staffing and Milestone Funding | [2026-11-tokenpath-06-attachment-6-detailed-budget-staffing-milestone-funding.md](https://github.com/motelnine/canton-dev-fund-proposal/blob/main/docs/2026-11-tokenpath-06-attachment-6-detailed-budget-staffing-milestone-funding.md)|
| 7 | Ecosystem Adoption and Independent Pilots | [2026-11-tokenpath-07-attachment-7-ecosystem-adoption-independent-pilots.md](https://github.com/motelnine/canton-dev-fund-proposal/blob/main/docs/2026-11-tokenpath-07-attachment-7-ecosystem-adoption-independent-pilots.md) |
| 8 | Intellectual Property, Open-Source Governance and Sustainability | [2026-11-tokenpath-08-attachment-8-ip-open-source-governance-sustainability.md](https://github.com/motelnine/canton-dev-fund-proposal/blob/main/docs/2026-11-tokenpath-08-attachment-8-ip-open-source-governance-sustainability.md)|

The supporting attachments describe the proposed design and acceptance evidence; any unexecuted partner commitments, unconfirmed staffing, third-party audit arrangements or vendor quotations remain subject to verification before grant contracting.

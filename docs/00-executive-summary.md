# Token Path LLC — Canton Development Fund Executive Summary

| **Project**                   | Canton Open Tax-Lot Interoperability and Proof-of-Basis Reference Infrastructure |
|-------------------------------|----------------------------------------------------------------------------------|
| **Applicant**                 | Token Path LLC                                                                   |
| **Funding Request**           | 1,900,000 CC                                                                     |
| **Initial Milestone Funding** | 350,000 CC                                                                       |
| **Development Period**        | 24 weeks                                                                         |

# Executive Summary

Token Path LLC proposes to develop an open-source, Canton-native interoperability infrastructure that connects tokenized securities with the economic, tax, corporate-action, and shareholder-governance information required by institutional capital markets.

As traditional financial assets transition toward tokenized ownership and settlement, financial institutions must preserve more than transaction records. They must maintain accurate adjusted cost basis, tax-lot histories, corporate-action adjustments, shareholder voting entitlements, and voluntary election instructions throughout the investment lifecycle.

Token Path’s proposed infrastructure addresses these requirements through a provider-neutral oracle framework that connects authorized Canton ledger events with trusted off-ledger institutional data providers. The architecture will support standardized economic-data references, cryptographically signed Proof-of-Basis attestations, and auditable event histories without exposing confidential investor information or proprietary calculation methodologies on-chain.

# Core Infrastructure Capabilities

- **Tax-Lot and Cost-Basis Interoperability:** Standardized references for acquisition history, fractional ownership, partial dispositions, adjusted cost basis, and tax-lot continuity.

- **Proof-of-Basis Attestations:** Cryptographically verifiable evidence linking authorized ledger events to institutional economic-data records.

- **Corporate-Action Processing:** Reference workflows for mandatory corporate actions, dividend reclassifications, basis adjustments, and reconciliation.

- **Proxy Voting and Shareholder Governance:** Standardized workflows for voting entitlements, proxy communications, voting instructions, acknowledgments, and reconciliation of voting outcomes.

- **Voluntary Corporate-Action Elections:** Interoperable election workflows supporting tender offers, exchange offers, election deadlines, instruction status, and final processing outcomes.

- **Institutional Security and Privacy:** Canton/Daml authorization controls, off-ledger confidential data management, signed messages, and independently testable security safeguards.

# Open-Source Development Strategy

The grant-funded infrastructure will be designed as a reusable public-good contribution to the Canton ecosystem, including Daml reference contracts, canonical data schemas, documented APIs, mock-provider implementations, integration examples, and automated testing frameworks.

Token Path will maintain a clear separation between this open-source infrastructure and proprietary commercial services. Its existing Netbasis institutional tax-intelligence platform may serve as an optional data-provider integration, but the reference infrastructure will operate independently of Netbasis licensing, algorithms, and proprietary datasets.

The project will also preserve the operational responsibilities of authorized custodians, transfer agents, voting agents, and corporate-action service providers rather than attempting to replace their regulated functions.

# Development and Funding

The proposed 24-week program will be executed through five independently verifiable milestones covering architecture and specifications, core interoperability development, expanded economic and governance workflows, security validation, and ecosystem adoption.

Token Path requests 1,900,000 CC, beginning with an initial authorization of 350,000 CC for Milestone 1. The remaining 1,550,000 CC would be released through subsequent milestone approvals, subject to documented deliverables and acceptance criteria.

# Strategic Value to the Canton Ecosystem

The proposed infrastructure addresses a fundamental requirement for institutional tokenization: preserving the complete economic and ownership-related history of an investment as securities move between traditional financial infrastructure and digital settlement environments.

By extending interoperability beyond settlement to include tax intelligence, corporate actions, proxy voting, and investor elections, the project seeks to reduce fragmented integrations, improve data consistency, strengthen auditability, and lower the barriers to institutional adoption.

**Token Path’s objective is to provide Canton with a reusable, provider-neutral economic and governance interoperability layer that enables tokenized securities to retain the financial intelligence and shareholder rights required throughout their lifecycle.**

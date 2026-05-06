# Standards & API Reference

> Project: Compliance Policy Manager · Generated: 2026-05-06

## Industry Standards & Specifications

### ISO Standards

**ISO 37301:2021 — Compliance Management Systems**
- URL: https://www.iso.org/standard/75080.html
- The primary certifiable standard for compliance management systems, replacing ISO 19600:2014. Specifies requirements for establishing, developing, implementing, evaluating, maintaining, and improving a compliance management system (CMS). Highly relevant as the definitive international framework underpinning what a compliance policy manager must support, including policy lifecycle, obligation registers, and whistleblower provisions.

**ISO 19600:2014 — Compliance Management Systems: Guidelines** (withdrawn)
- URL: https://www.iso.org/standard/62342.html
- The predecessor to ISO 37301, now formally withdrawn. Still referenced in legacy deployments. Provided guidance-only (non-certifiable) recommendations for CMS implementation. Understanding the delta between ISO 19600 and ISO 37301 is important for migration tooling.

**ISO 9001:2015 — Quality Management Systems**
- URL: https://www.iso.org/standard/62085.html
- Clause 7.1.6 (Organisational Knowledge) and Clause 7.5 (Documented Information) impose document control requirements that directly overlap with policy management workflows: creation, review, approval, distribution, and retention of documented policies and procedures.

**ISO 27001:2022 — Information Security Management Systems**
- URL: https://www.iso.org/standard/27001
- Requires organisations to establish, document, review, and communicate information security policies (Clause A.5.1). Annex A controls include policy management obligations that a compliance policy manager must be capable of evidencing.

**ISO 30401:2018 — Knowledge Management Systems**
- URL: https://www.iso.org/standard/68683.html
- Provides requirements for knowledge management systems, relevant to how policy knowledge is captured, versioned, distributed, and retained across an organisation. Particularly pertinent to AI-assisted policy creation and retrieval use cases.

---

### Regulatory Frameworks

**HIPAA Security Rule (45 CFR Part 164)**
- URL: https://www.hhs.gov/hipaa/for-professionals/security/laws-regulations/index.html
- Requires covered entities to develop, document, and implement security policies and procedures. HIPAA mandates retention of all compliance documentation (policies, procedures, training records) for a minimum of six years from creation or last effective date. Policy management tooling must support tamper-evident audit trails and retention scheduling.

**GDPR (EU Regulation 2016/679)**
- URL: https://gdpr-info.eu/
- Imposes requirements on data protection policies, including documenting lawful basis for processing, maintaining Records of Processing Activities (RoPAs), and evidencing employee awareness of data protection obligations. Policy attestation and acknowledgment workflows are directly relevant to demonstrating GDPR compliance accountability.

**PCI DSS v4.0.1 — Payment Card Industry Data Security Standard**
- URL: https://www.pcisecuritystandards.org/document_library/
- Requirement 12 mandates a comprehensive information security policy, with annual scope confirmation and documentation (Requirement 12.3.2). All 51 future-dated v4.0 requirements became mandatory on 31 March 2025. Policy version control, annual review attestation, and targeted risk analysis documentation are core policy management obligations.

**US ESIGN Act (Electronic Signatures in Global and National Commerce Act, 2000)**
- URL: https://www.ncua.gov/regulation-supervision/manuals-guides/federal-consumer-financial-protection-guide/compliance-management/deposit-regulations/electronic-signatures-global-and-national-commerce-act-e-sign-act
- Grants legal recognition to electronic signatures and records, provided all parties consent to transact electronically. Directly enables electronic policy acknowledgment and attestation workflows. Four validity requirements: intent to sign, consent to electronic transaction, business consent documentation, and consumer disclosure.

**UETA — Uniform Electronic Transactions Act**
- URL: https://www.uniformlaws.org/committees/community-home?CommunityKey=2c04b76c-2b7d-4399-977e-d5876ba7e034
- State-level counterpart to the ESIGN Act, enacted in 49 US states. Governs the legal validity of electronically signed policy acknowledgments at the state level.

---

### W3C & IETF Standards

**RFC 7519 — JSON Web Tokens (JWT)**
- URL: https://datatracker.ietf.org/doc/html/rfc7519
- Defines compact, URL-safe means of representing claims between parties. Relevant for encoding policy acknowledgment tokens, signed attestation records, and user identity assertions within a policy management platform.

**RFC 7515 — JSON Web Signature (JWS)**
- URL: https://datatracker.ietf.org/doc/html/rfc7515
- Defines the structure and processing rules for digitally signed JSON data. Enables cryptographically verifiable policy acknowledgment records and tamper-evident audit log entries.

**RFC 6749 — OAuth 2.0 Authorization Framework**
- URL: https://datatracker.ietf.org/doc/html/rfc6749
- The foundational standard for delegated API access. All major compliance platforms (Hyperproof, Drata, Vanta) use OAuth 2.0 for API authentication. Essential for integrations with identity providers and third-party systems.

**RFC 7643 & RFC 7644 — SCIM 2.0 (System for Cross-domain Identity Management)**
- URLs: https://datatracker.ietf.org/doc/html/rfc7643 and https://datatracker.ietf.org/doc/html/rfc7644
- Defines a standard schema (RFC 7643) and HTTP protocol (RFC 7644) for automating user provisioning and de-provisioning across systems. A compliance policy manager must distribute policies to the correct users; SCIM integration enables automatic audience management as users join, change roles, or leave the organisation.

**RFC 5246 / RFC 8446 — TLS (Transport Layer Security)**
- URL: https://datatracker.ietf.org/doc/html/rfc8446
- TLS 1.3 is the required transport security standard for all API communications in compliance contexts. HIPAA, PCI DSS, and SOC 2 all mandate encryption in transit.

---

### Data Model & API Specifications

**OpenAPI Specification 3.1 (OAS 3.1)**
- URL: https://spec.openapis.org/oas/v3.1.1.html
- The industry-standard specification for documenting RESTful APIs. All major GRC platforms expose REST APIs described via OpenAPI. OAS 3.1 is fully compatible with JSON Schema draft 2020-12, enabling richer schema definitions for policy objects, control mappings, and attestation records. The webhooks object (introduced in OAS 3.1) supports event-driven notifications for policy lifecycle events.

**JSON Schema (Draft 2020-12)**
- URL: https://json-schema.org/specification
- Provides the vocabulary for describing and validating JSON data structures. Useful for defining canonical schemas for policy documents, attestation records, obligation mappings, and audit evidence payloads.

**OASIS XACML 3.0 — eXtensible Access Control Markup Language**
- URL: https://docs.oasis-open.org/xacml/3.0/xacml-3.0-core-spec-os-en.html
- The standard for defining fine-grained, attribute-based access control (ABAC) policies. Defines the five-component architecture: Policy Administration Point (PAP), Policy Retrieval Point (PRP), Policy Decision Point (PDP), Policy Enforcement Point (PEP), and Policy Information Point (PIP). Directly relevant to role-based policy distribution and access scoping. XACML 4.0 Committee Specification Draft 01 was published February 2026.

---

### Security & Authentication Standards

**OpenID Connect Core 1.0**
- URL: https://openid.net/specs/openid-connect-core-1_0.html
- Identity layer on top of OAuth 2.0. Used by compliance platforms for SSO integration with enterprise identity providers (Okta, Azure AD, Google Workspace). Enables seamless user authentication into a policy management portal without separate credential management.

**NIST SP 800-53 Rev 5 — Security and Privacy Controls for Federal Information Systems**
- URL: https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final
- Comprehensive catalogue of security and privacy controls. Policy and Procedures (PL-1, PL-2, PL-4) controls directly map to policy creation, distribution, and acknowledgment requirements that a compliance policy manager must automate.

**NIST Cybersecurity Framework (CSF) 2.0**
- URL: https://www.nist.gov/cyberframework
- Provides the Govern, Identify, Protect, Detect, Respond, Recover functions. The Govern function (added in CSF 2.0) explicitly calls out policy management, roles, and accountability as foundational cybersecurity activities.

**NIST SP 800-228 (IPD) — Guidelines for API Protection for Cloud-Native Systems**
- URL: https://csrc.nist.gov/pubs/sp/800/228/ipd
- Addresses identification and analysis of risk factors during API development and runtime, and recommends controls for pre-runtime and runtime API protection. Relevant for hardening the compliance platform's own API surface.

**SOC 2 Trust Services Criteria (AICPA)**
- URL: https://www.aicpa-cima.com/resources/download/soc-2-trust-services-criteria
- The AICPA's Trust Services Criteria underpin SOC 2 audits. CC2.2 (Communication of Policies and Procedures) and CC9.2 (Vendor/Business Partner Management) are directly addressed by policy distribution and attestation capabilities. A compliance policy manager itself should be SOC 2 Type II certified.

---

### MCP Server Specifications

The Model Context Protocol (MCP) is relevant for AI-native extensions to a compliance policy manager. An MCP server exposing compliance data could allow AI assistants to query policy status, retrieve obligation mappings, and surface pending attestations.

- MCP Specification: https://modelcontextprotocol.io/specification
- Relevant resources: policy documents, control records, attestation status, obligation registers, and risk mappings would all be natural MCP resource types.

---

## Similar Products — Developer Documentation & APIs

### Drata

- **Description:** Continuous security and compliance automation platform supporting SOC 2, ISO 27001, HIPAA, PCI DSS, and 15+ frameworks. Includes policy management, evidence collection, and vendor risk management.
- **API Documentation:** https://developers.drata.com/api-docs/
- **Developer Portal:** https://developers.drata.com/
- **Standards:** REST/JSON, OpenAPI
- **Authentication:** OAuth 2.0
- **Notes:** Open API product page describes automated evidence and reporting; policy endpoints allow retrieval and update of compliance documentation.

### Vanta

- **Description:** Trust management platform automating SOC 2, ISO 27001, HIPAA, and GDPR compliance. Features continuous monitoring, policy distribution, and auditor-ready evidence collection.
- **API Documentation:** https://developer.vanta.com/docs/vanta-api-overview
- **Developer Portal:** https://developer.vanta.com/
- **Standards:** REST/JSON, OpenAPI
- **Authentication:** OAuth 2.0
- **Notes:** RESTful API with broad endpoint coverage for controls, tests, and user management.

### Hyperproof

- **Description:** Operations-focused GRC platform for managing compliance programs, controls, and evidence across multiple frameworks. Includes policy management and risk workflow capabilities.
- **API Documentation:** https://developer.hyperproof.app/hyperproof-api
- **Developer Portal:** https://developer.hyperproof.app/
- **SDKs:** Hypersync SDK for custom integrations
- **Standards:** REST/JSON, OpenAPI (Controls API exposed as OpenAPI spec)
- **Authentication:** OAuth 2.0 (authorization code and client credentials grant types)
- **Notes:** Controls API at `developer.hyperproof.app/hyperproof-api/controls/controls.openapi` is a concrete OpenAPI specification for compliance controls.

### OneTrust

- **Description:** Privacy, security, and data governance platform. Includes policy management APIs for creating, distributing, and retrieving compliance policies, standards, procedures, and privacy notices.
- **API Documentation:** https://developer.onetrust.com/onetrust/reference/onetrust-api-reference
- **Developer Portal:** https://developer.onetrust.com/
- **Key Endpoints:** `GET /policies` (list policies by compliance document type), `GET /policies/{id}` (retrieve policy details)
- **Standards:** REST/JSON, OpenAPI
- **Authentication:** OAuth 2.0
- **Notes:** Tugboat Logic (acquired by OneTrust) capabilities are now part of OneTrust GRC & Security Assurance Cloud.

### Sprinto

- **Description:** Modern GRC automation platform targeting fast-growing tech companies. Supports SOC 2, ISO 27001, HIPAA, PCI DSS, and AI risk frameworks.
- **API Documentation:** https://developer.sprinto.com/docs/sprinto-developer-api-documentation
- **Standards:** GraphQL (not REST); all API calls use HTTPS; responses in JSON
- **Authentication:** API Key (generated via Sprinto web application by admin users)
- **Notes:** Sprinto's use of GraphQL rather than REST is architecturally distinct from most GRC platform APIs.

### LogicGate

- **Description:** Risk Cloud platform providing configurable GRC workflows including GDPR data mapping, risk assessments, incident management, and policy management.
- **API Documentation:** https://docs.logicgate.com/
- **Standards:** REST/JSON
- **Authentication:** API Key / OAuth
- **Notes:** Emphasises workflow automation and customisability over pre-built compliance frameworks.

### Workiva

- **Description:** Unified platform for financial reporting, ESG, GRC, and audit management. Targets enterprise and regulated-industry compliance teams.
- **API Documentation:** https://developers.workiva.com/
- **Support Center API Section:** https://support.workiva.com/hc/en-us/sections/13356759670548-API
- **Standards:** REST/JSON
- **Authentication:** OAuth 2.0
- **Notes:** Exposes APIs for Documents, Spreadsheets, Presentations, Graph, Tasks, and Wdata (data management). Relevant for organisations needing compliance integrated with financial reporting.

### AuditBoard

- **Description:** Connected risk platform for audit management, SOX compliance, risk assessments, and policy management. Integrates with Office 365, Salesforce, and Slack.
- **API Documentation:** https://apitracker.io/a/auditboard
- **Standards:** REST/JSON
- **Authentication:** API Key / OAuth
- **Notes:** Strong focus on internal audit workflows alongside policy management.

---

## Notes

### Gaps and Emerging Areas

- **Verifiable Credentials for Attestation:** The W3C Verifiable Credentials Data Model (https://www.w3.org/TR/vc-data-model/) and OpenID for Verifiable Credential Issuance (OID4VCI) represent an emerging approach to cryptographically verifiable policy acknowledgment records. While not yet mainstream in GRC platforms, these standards may become significant for portable, auditor-verifiable attestation.

- **AI Governance Policies:** ISO/IEC 42001:2023 (AI Management Systems) is an emerging standard requiring organisations to establish AI-specific policies and controls. Compliance policy managers will increasingly need to support AI governance policy templates and obligation tracking aligned to this standard.

- **SCIM Adoption in GRC:** SCIM 2.0 is widely implemented in identity providers but inconsistently adopted by GRC and policy management platforms. A purpose-built AI-native tool could differentiate by offering first-class SCIM support for automatic policy audience management.

- **Webhook Standardisation:** Policy lifecycle events (published, acknowledged, expired, revised) lack a cross-vendor webhook schema standard. OpenAPI 3.1's webhooks object provides the specification mechanism, but the event vocabulary is proprietary per vendor.

- **ISO 37301 Tooling Gap:** Despite ISO 37301:2021 being the premier certifiable compliance management standard, few commercial tools explicitly map their features to its clause structure. An AI-native platform with native ISO 37301 clause mapping would fill a meaningful market gap.

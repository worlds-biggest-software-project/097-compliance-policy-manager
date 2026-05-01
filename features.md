# Compliance Policy Manager — Feature & Functionality Survey

> Candidate #97 · Researched: 2026-05-01

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| NAVEX PolicyTech (NAVEX One) | Enterprise policy lifecycle SaaS | Commercial (proprietary) | https://www.navex.com/en-us/platform/employee-compliance/policytech-policy-management-software/ |
| Riskonnect Policy Management | Enterprise GRC + policy SaaS | Commercial (proprietary) | https://riskonnect.com |
| LogicGate Risk Cloud | No-code GRC SaaS | Commercial (proprietary) | https://www.logicgate.com |
| Sprinto | SMB compliance automation SaaS | Commercial (proprietary) | https://sprinto.com |
| PowerDMS | Policy + training SaaS (public safety / healthcare) | Commercial (proprietary) | https://www.powerdms.com |
| Doctract | SMB policy management SaaS | Commercial (proprietary) | https://www.doctract.com |
| SweetProcess | Policy and procedure SaaS | Commercial (proprietary) | https://www.sweetprocess.com |
| Eramba | Open-source GRC and policy manager | Open Source (AGPL / commercial) | https://www.eramba.org |
| Confluence + plugins | Wiki-based policy documentation | Commercial (proprietary, Atlassian) | https://www.atlassian.com/software/confluence |
| Compliance.ai (Archer) | Regulatory change management SaaS | Commercial (proprietary) | https://www.compliance.ai |
| Archer Evolv Compliance | Enterprise AI compliance SaaS | Commercial (proprietary) | https://www.archerirm.com/evolv-compliance |

## Feature Analysis by Solution

### NAVEX One PolicyTech

**Core features**
- Policy document authoring environment with rich-text editing and template library
- Configurable multi-stage review and approval workflow (writer → reviewer → approver → publisher)
- Automated employee distribution: policies delivered directly to relevant employees based on role, department, location, or other attributes
- Attestation tracking: records individual employee acknowledgements with timestamp and version reference
- Version control with automatic archiving of superseded policy versions
- Audit-ready reporting: who has viewed a policy, when, and which version was attested to
- Mobile and tablet access for policy reading and attestation

**Differentiating features**
- AI-assisted policy summaries (launched Q4 2025): NAVEX One generates plain-language summaries of complex policy documents to improve employee comprehension
- NAVEX One Compliance Assistant: a conversational AI interface that allows employees to ask natural-language questions and receive answers sourced from the policy library, with document citations
- Integration into the broader NAVEX One GRC platform (ethics hotline, training, case management) for unified compliance management

**UX patterns**
- Employee-facing portal with clean navigation: "My policies to read", "Overdue attestations", "Policy search"
- Admin dashboard: policy lifecycle pipeline, overdue attestation heat maps by department, policy gap analysis
- Automated email and in-app reminders to employees with pending attestations

**Integration points**
- Active Directory / LDAP and SSO (SAML 2.0) for employee roster synchronisation
- HRIS integration (Workday, SAP SuccessFactors) for role and department mapping
- NAVEX One platform modules (training, incident management, third-party risk)
- REST API for custom integrations

**Known gaps**
- Regulatory change-to-policy automation is not end-to-end; regulatory monitoring is manual or requires a separate tool
- Attestation analysis is reported rather than predictive; anomaly detection on attestation behaviour is limited
- Pricing is enterprise-only; inaccessible to organisations below roughly 500 employees without significant budget
- AI features as of 2025 are summaries and Q&A only; no generative policy drafting from regulatory input

**Licence / IP notes**
- Fully proprietary SaaS; owned by Madison Dearborn Partners (private equity, acquired 2018)
- Data processed in NAVEX-managed cloud infrastructure; US and EU data residency options available

---

### Riskonnect Policy Management

**Core features**
- Policy authoring, distribution, attestation, and retirement lifecycle management within a unified GRC platform
- Policy-to-control framework mapping: links policies to ISO 27001, NIST, SOX, and other frameworks
- Risk-to-policy traceability: connect identified risks to the policies designed to mitigate them
- 2,700+ enterprise customer base with deep financial services and healthcare vertical experience
- Integration with Riskonnect's ERM, TPRM, and internal audit modules for a single risk view

**Differentiating features**
- Tightest native integration between policy management and broader enterprise risk management of any platform in this category
- Policy gap analysis: identifies where organisational risks lack a corresponding documented policy

**Known gaps**
- Enterprise-only; no mid-market or self-serve tier
- AI capabilities less developed than NAVEX or newer entrants
- Implementation complexity comparable to NAVEX

**Licence / IP notes**
- Fully proprietary SaaS

---

### Eramba

**Core features**
- Policy management module: create, version, distribute, and track acknowledgement of policies
- Control framework mapping: built-in libraries for ISO 27001, PCI DSS, SOC 2, NIST SP 800-53, GDPR
- Risk management: risk register, risk treatment, and residual risk tracking
- Audit management: internal audit planning, evidence collection, and finding remediation
- Exception management: track approved exceptions to policies with expiry and re-approval workflows
- Community edition is fully self-hosted with no usage limits

**Differentiating features**
- The only mature open-source GRC platform covering policy management alongside risk and audit management
- Decade-plus track record (founded 2013); active GitHub community and regular releases
- Self-hosted deployment allows organisations with strict data residency or classified-data requirements to maintain full control

**UX patterns**
- Traditional enterprise application UX: tabular views, form-based data entry, dashboard widgets
- Less polished than modern SaaS entrants but functionally comprehensive for its target (GRC practitioners)

**Integration points**
- LDAP / Active Directory for user management
- Email-based notification system for attestations and reminders
- REST API in enterprise edition; community edition has limited API surface
- Jira and ticketing system integration in enterprise edition

**Known gaps**
- No AI-powered features (policy drafting, Q&A, regulatory change monitoring) as of 2026
- Community edition support is community-forum only; enterprise support requires paid subscription
- UX requires modernisation to compete with commercial SaaS for non-technical users
- Mobile experience limited

**Licence / IP notes**
- Community edition: AGPL v3 (open source); any modifications to the application must be released under the same licence if distributed
- Enterprise edition: commercial licence layered on top of the open-source core; consulting and support fees apply
- No known patents

---

### Compliance.ai (now part of Archer)

**Core features**
- Regulatory change management: monitors 2,000+ regulatory sources across 99+ jurisdictions in real time
- AI-powered categorisation and parsing of regulatory content into structured obligations
- Unified regulatory library with version history and change tracking
- Automated task assignment when a new regulatory obligation is identified
- Certified audit reports with automatic evidence capture
- Obligation-to-policy traceability: maps regulatory requirements to internal policies

**Differentiating features**
- Expert-in-the-loop ML: regulatory changes are processed by AI and validated by human regulatory experts before alerting, reducing false-positive burden on compliance teams
- Horizon scanning at scale: monitors regulatory sources across all major global jurisdictions simultaneously — a workflow that is manual for most organisations

**Known gaps**
- Policy authoring and attestation are not native to Compliance.ai; it is a regulatory intelligence and obligation-mapping layer, not a full policy lifecycle tool
- Now embedded within Archer (RSA spin-off); enterprise-only pricing

**Licence / IP notes**
- Fully proprietary SaaS

---

### Sprinto

**Core features**
- Security and compliance automation targeting SOC 2, ISO 27001, HIPAA, GDPR, and PCI DSS
- Policy template library with pre-built security policy templates mapped to control frameworks
- Employee attestation workflows with automated reminders
- Evidence collection automation: pulls audit evidence from connected cloud systems (AWS, GCP, Azure, GitHub, Jira)
- Vendor risk assessment questionnaires

**Differentiating features**
- Developer-friendly design: integrates directly with CI/CD pipelines and cloud infrastructure for automated evidence collection
- Fastest time-to-certification in the market for SOC 2 and ISO 27001 (many customers complete first audit in 4–8 weeks)

**Known gaps**
- Policy management is a secondary feature; primary value is automated evidence collection for security audits
- Not suitable for complex enterprise policy libraries beyond security frameworks
- Limited regulatory change monitoring

**Licence / IP notes**
- Fully proprietary SaaS

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Policy document authoring with rich-text editor, templates, and version control
- Multi-stage review and approval workflow with configurable routing
- Employee distribution with role and department targeting
- Attestation tracking: individual acknowledgement records with timestamp, version reference, and audit export
- Automated reminders for overdue attestations with escalation to managers
- Full-text policy search
- Audit-ready reporting for regulators and internal audit teams

### Differentiating Features
- AI-assisted policy Q&A ("Ask your policy") with source citations from the policy library
- Regulatory change monitoring: automated scanning of regulatory feeds with mapping to affected internal policies
- Policy-to-control framework mapping (ISO 27001, NIST, SOX, GDPR, EU AI Act, DORA)
- Attestation anomaly detection: flagging employees who complete attestations implausibly quickly, departments with unusually high exception rates, or correlations between non-attestation and incident data
- Generative policy drafting: producing a structured first-draft policy update from a new regulatory provision
- AI Act and AI governance policy documentation: managing AI system registers, impact assessments, and usage policies as a distinct policy category

### Underserved Areas / Opportunities
- End-to-end regulatory change-to-policy automation: no tool fully closes the loop from "new regulation published" to "updated policy distributed and attested"
- Natural-language policy search that understands intent, not just keywords
- Attestation quality analytics: turning checkbox compliance into genuine risk signal
- Open-source policy manager with a pluggable LLM backend and an open control framework mapping library
- AI governance policy management as a native category (EU AI Act, NIST AI RMF, DORA)

### AI-Augmentation Candidates
- LLM-powered regulatory feed monitoring with change-to-policy impact analysis
- Generative policy drafting from regulatory or internal risk inputs
- Conversational "Ask your policy" interface with citation-backed answers
- Attestation pattern analysis and anomaly scoring
- Automated control framework gap analysis when new regulations are enacted

## Legal & IP Summary

NAVEX PolicyTech and Riskonnect are fully proprietary; both are private-equity-backed platforms with no open-source components. Eramba is the only established open-source option, licensed under AGPL v3 for the community edition. The AGPL licence has a strong copyleft requirement: any organisation that modifies and deploys Eramba as a network service must release its modifications under AGPL. This is a critical licence consideration for any open-source project building on Eramba's codebase. ISO 37301:2021 (Compliance Management Systems) is a publicly available standard that can freely inform system design without IP restrictions. NIST SP 800-53, NIST AI RMF, and COSO frameworks are US government publications in the public domain. The EU AI Act text is a public legislative instrument. No known patent filings specifically covering AI-driven policy attestation analytics have been identified among these vendors.

## Recommended Feature Scope

**Must-have (MVP)**
- Policy document authoring with rich-text editor, template library, and version control (major + minor versions with change notes)
- Multi-stage review and approval workflow with configurable routing, role assignment, and email notifications
- Employee distribution with targeting by role, department, location, and custom attribute
- Attestation tracking with individual timestamp records, version pinning, and CSV / PDF audit export
- Automated reminder escalation for overdue attestations (configurable schedule, manager escalation)
- Full-text search across the live policy library

**Should-have (v1.1)**
- Control framework mapping library: ISO 27001, NIST SP 800-53, SOC 2, GDPR, and EU AI Act control sets linkable to individual policies
- AI-powered "Ask your policy" interface: employees submit natural-language questions; system returns answers sourced from and cited to specific policy sections
- Regulatory change alert integration: subscribe to regulatory feeds (e.g., EUR-Lex, Federal Register); flag which policies may be affected by a new publication
- Exception management workflow: track policy exceptions with approver, justification, expiry date, and re-approval reminder
- Pluggable LLM backend for AI features (support OpenAI, Anthropic, and self-hosted models)

**Nice-to-have (backlog)**
- Generative policy drafting: input a regulatory provision or risk description; system generates a structured draft policy for human review
- Attestation anomaly detection: flag statistically unusual attestation patterns (completion time, department outliers, correlation with incident data)
- AI governance policy category: native support for EU AI Act Article 9 risk management documentation, AI system registers, and NIST AI RMF profiles
- Multi-language policy distribution with AI-assisted translation
- Policy effectiveness scoring: correlate attestation completeness and exception rates with incident and audit finding data

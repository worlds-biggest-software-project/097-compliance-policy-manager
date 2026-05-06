# Compliance Policy Manager

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source platform for the full policy lifecycle — authoring, distribution, attestation, and version control — built for organisations that cannot, or will not, hand their compliance data to enterprise SaaS vendors.

Compliance Policy Manager is a self-hostable system for compliance, legal, and security teams who need to draft policies, distribute them to the right employees, capture attestation evidence, and prove control coverage to auditors. It targets the gap between expensive enterprise GRC suites (NAVEX PolicyTech, Riskonnect) and lightweight SMB tools (SweetProcess, Doctract) by combining a modern policy lifecycle with AI capabilities — regulatory change monitoring, conversational policy Q&A, attestation anomaly detection — that incumbents have only partially shipped.

---

## Why Compliance Policy Manager?

- The market leaders (NAVEX PolicyTech, Riskonnect) are enterprise-only with custom contracts in the five-to-six figure range and lengthy sales cycles, leaving organisations below ~500 employees without a serious option.
- Eramba is the only mature open-source GRC platform, but as of 2026 it has no AI-powered features for policy drafting, Q&A, or regulatory change monitoring, and its UX has not kept pace with modern SaaS.
- No incumbent closes the loop end-to-end from "new regulation published" to "updated policy drafted, distributed, and attested" — regulatory monitoring is typically a separate paid layer (e.g. Compliance.ai / Archer).
- Government agencies, NGOs, universities, and privacy-sensitive enterprises cannot send policy data to commercial SaaS vendors and need a self-hostable tool with pluggable LLM backends.
- New regulations — the EU AI Act (2025) and DORA — create policy documentation categories (AI system registers, ICT risk management policies) that existing platforms were not built to manage.

---

## Key Features

### Policy Lifecycle

- Rich-text policy authoring with a template library and major/minor version control with change notes.
- Multi-stage review and approval workflow with configurable routing, role assignment, and email notifications.
- Automatic archiving of superseded policy versions with full version history.
- Exception management workflow: record approver, justification, expiry date, and re-approval reminders.

### Distribution & Attestation

- Targeted distribution by role, department, location, and custom employee attribute.
- Attestation tracking with individual timestamp records and version pinning, exportable to CSV and PDF for auditors.
- Configurable automated reminders for overdue attestations, with manager escalation.
- Full-text search across the live policy library.

### Control Framework Mapping

- Built-in mapping libraries for ISO 27001, NIST SP 800-53, SOC 2, GDPR, and the EU AI Act control sets.
- Policy-to-control traceability: link individual policies to the framework controls they satisfy.
- Audit-ready reporting showing who has read and attested to which version of which policy.

### AI-Assisted Compliance

- "Ask your policy" natural-language interface that returns answers cited to specific policy sections.
- Regulatory change alert integration that subscribes to feeds (e.g. EUR-Lex, Federal Register) and flags which policies may be affected.
- Generative policy drafting from a regulatory provision or risk description, producing a structured first draft for human review.
- Attestation anomaly detection: flags implausibly fast completions, departments with high exception rates, and correlations with incident data.

### AI Governance & Emerging Regulation

- Native support for AI governance documentation: AI system registers, EU AI Act Article 9 risk assessments, and NIST AI RMF profiles managed as a distinct policy category.
- DORA-aligned ICT risk management policy templates for financial services use cases.

---

## AI-Native Advantage

Where incumbents have bolted on AI summaries (NAVEX, Q4 2025) or moved regulatory monitoring into a separate product (Compliance.ai / Archer), Compliance Policy Manager treats AI as load-bearing infrastructure across the policy lifecycle. A regulatory-change agent translates new provisions into draft policy diffs mapped to affected control frameworks, compressing a weeks-long manual process into hours. A conversational "Ask your policy" interface answers employee questions with source citations, reducing routine load on legal and compliance teams. Attestation anomaly detection turns acknowledgement data — today a checkbox exercise — into a genuine risk signal.

---

## Tech Stack & Deployment

- Self-hosted deployment as the primary mode, suitable for organisations with strict data residency or classified-data requirements; a managed cloud option is a future possibility.
- Pluggable LLM backend supporting OpenAI, Anthropic, and self-hosted models, so AI features work for organisations that cannot send policy data to third-party APIs.
- Standards-aligned design grounded in ISO 37301:2021 (Compliance Management Systems), with control framework libraries for ISO 27001, NIST SP 800-53, COSO (SOX), GDPR, the EU AI Act, and DORA.
- Integration surface for Active Directory / LDAP, SSO (SAML 2.0), and HRIS systems for employee roster and attribute synchronisation, plus a REST API for custom workflows.

---

## Market Context

The Policy Management Software market was valued at $1.62B in 2024 and is projected to reach $6.07B by 2033 at a 15.8% CAGR (SkyQuestt); the broader Compliance Management Software market was $34.99B in 2025, projected to reach $70.69B by 2032 at 10.5% CAGR (Research and Markets). Pricing spans from ~$99/month for SMB tools (SweetProcess) and $500–$25K/year for growth-stage products (Doctract, Sprinto) up to $50K–$500K+/year for enterprise platforms (NAVEX PolicyTech, Riskonnect). Primary buyers are Chief Compliance Officers in regulated enterprises, IT/security compliance managers pursuing SOC 2 and ISO 27001, mid-market HR and operations leaders, and budget-constrained open-source adopters in government, NGOs, and academia.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context. Note: Eramba's community edition is AGPL v3, which carries strong copyleft obligations for any derivative network service — a relevant consideration if any Eramba-derived code is incorporated.

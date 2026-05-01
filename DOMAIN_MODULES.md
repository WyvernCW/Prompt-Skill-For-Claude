# Domain Modules

## Overview
Pluggable domain context that injects specialized constraints, terminology, and best practices into prompts.

## fintech
### Regulatory
PCI-DSS, SOX, GDPR financial data, KYC/AML, PSD2, Basel III.
### Constraints
Transaction integrity, audit trails, encryption at rest + in transit, idempotency keys, reconciliation windows.
### Terminology
Ledger, reconciliation, settlement, clearing, custody, NAV, AUM, drawdown, alpha, beta, Sharpe ratio.
### Best Practices
- Double-entry accounting for all transactions.
- Event sourcing for audit trails.
- Idempotency on all payment operations.
- Circuit breakers for external market data.
- Rate limiting on trading endpoints.

## medical
### Regulatory
HIPAA, FDA 21 CFR Part 11, GDPR health data, HITECH, DICOM.
### Constraints
PHI protection, audit logging, data retention (7 years min), consent management, de-identification.
### Terminology
EHR, EMR, HL7 FHIR, ICD-10, CPT, SNOMED CT, LOINC, clinical decision support, CDS hooks.
### Best Practices
- De-identification before analytics.
- Role-based access to PHI.
- Immutable audit logs.
- Interoperability via FHIR APIs.
- Patient safety checks on all clinical calculations.

## legal
### Regulatory
Attorney-client privilege, GDPR, e-discovery rules (FRCP), legal hold, confidentiality.
### Constraints
Chain of custody, version control, tamper-proofing, redaction, privilege log.
### Terminology
Discovery, brief, precedent, jurisdiction, statute of limitations, deposition, motion, brief, docket.
### Best Practices
- Bates numbering on all produced documents.
- Metadata scrubbing before sharing.
- Privilege log for withheld documents.
- Immutable version history.
- Automated legal hold triggers.

## gaming
### Constraints
Frame budget (16.67ms for 60fps), input latency (<20ms), netcode, asset streaming, memory budget.
### Terminology
LOD, draw call, tick rate, hitbox, matchmaking, MMR, ELO, gacha, F2P, P2W, season pass.
### Best Practices
- Deterministic simulation for multiplayer.
- Client-side prediction + server reconciliation.
- Asset streaming for open worlds.
- Object pooling for particle systems.
- Telemetry for balance tuning.

## ecommerce
### Constraints
Cart abandonment optimization, payment flow (<3 clicks), inventory sync, tax calculation, fraud detection.
### Terminology
SKU, conversion funnel, AOV, churn, LTV, cohort analysis, RFM, abandoned cart, upsell, cross-sell.
### Best Practices
- Guest checkout option.
- Abandoned cart recovery emails.
- Dynamic pricing with A/B testing.
- Real-time inventory sync.
- PCI-compliant payment handling.

## security
### Constraints
Zero-trust, least privilege, defense in depth, threat modeling, secure defaults.
### Terminology
CVE, CVSS, OWASP, MITRE ATT&CK, SIEM, SOC2, ISO 27001, pen test, red team, blue team.
### Best Practices
- Input validation on all entry points.
- Output encoding for all rendered content.
- Secure defaults (deny all, allow explicitly).
- Comprehensive logging (who, what, when, where).
- Regular dependency scanning.

## edu
### Regulatory
FERPA, COPPA, WCAG 2.1 AA, Section 508.
### Constraints
Multi-tenancy, grade privacy, accessibility, content moderation.
### Terminology
LMS, SIS, LTI, SCORM, xAPI, competency-based, formative assessment, summative assessment, rubric.
### Best Practices
- Universal Design for Learning (UDL).
- Progress tracking with granular analytics.
- Gamification with meaningful rewards.
- Accessibility-first content creation.
- Parent/guardian portal for K-12.

## creative
### Constraints
Copyright compliance, licensing attribution, fair use, color profiles, export formats.
### Terminology
CMYK, Pantone, RGB, HEX, kerning, leading, tracking, composition, color theory, golden ratio, rule of thirds.
### Best Practices
- Asset management with version control.
- Color profile consistency (sRGB for web, CMYK for print).
- Attribution tracking for licensed assets.
- Non-destructive editing workflows.
- Export presets for multiple platforms.

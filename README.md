# Mental Health Platform

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source mental health platform that unifies therapy session management, measurement-based care, and stepped-care routing under a HIPAA- and 42 CFR Part 2-compliant data model.

The Mental Health Platform is an integrated clinical and member-facing system for behavioural health practices, employer benefits programmes, and safety-net providers. It combines scheduling, telehealth, clinical documentation, validated outcome measurement, and AI-assisted care routing in one platform — addressing the fragmentation between consumer teletherapy, clinician EHRs, and employer benefits incumbents that dominate the market today.

---

## Why Mental Health Platform?

- **Incumbents are siloed and expensive.** Lyra Health and Spring Health charge $3–$8 PEPM and target only mid-to-large employers, leaving SMBs, FQHCs, and community mental health centres without affordable AI-native tooling.
- **Consumer teletherapy lacks clinical rigour.** BetterHelp and Talkspace operate at scale but offer no native measurement-based care or outcomes tracking, and BetterHelp's 2023 FTC settlement ($7.8M) underscores a persistent privacy and quality gap.
- **Clinician EHRs lag on AI.** SimplePractice and TherapyNotes lead practice management for solo and small-group practices but have no AI documentation features as of the research date.
- **Compliance is shifting.** The 42 CFR Part 2 Final Rule (enforcement from 16 February 2026) imposes stricter SUD-record consent requirements that most platforms have not yet fully implemented.
- **Primary care integration is missing.** Existing platforms are largely disconnected from primary care EHRs, blocking true integrated behavioural health despite CMS interoperability rules pushing FHIR R4 adoption.

---

## Key Features

### Clinical Workflow & Documentation

- Structured progress notes, treatment plans, and intake assessments with ICD-10-CM diagnostic coding
- HIPAA-compliant data architecture with elevated protection for psychotherapy notes (45 CFR § 164.524)
- 42 CFR Part 2-compliant SUD record handling with separate consent workflows
- Group practice supervision with co-signature workflow for supervised clinicians
- Specialty templates for psychiatry, psychology, LCSW, LMFT, and addiction counselling

### Scheduling, Telehealth & Member Portal

- Self-service online booking with automated SMS and email appointment reminders
- HIPAA-compliant integrated telehealth video sessions
- Client/member portal for scheduling, intake forms, secure messaging, and document signing
- Asynchronous messaging between scheduled sessions
- Crisis screening protocol with documented escalation pathway

### Measurement-Based Care & Outcomes

- Validated outcome measure administration: PHQ-9, GAD-7, PCL-5, and C-SSRS
- Automated assessment scheduling at clinically optimal intervals with deterioration alerts
- Outcome trend visualisations showing client progress trajectory
- Treatment planning linked to outcome measures with visual progress tracking
- Aggregate, de-identified employer analytics dashboard with HEDIS-aligned reporting

### Billing & Interoperability

- 837P professional claims submission and 835 ERA payment posting
- HL7 FHIR R4 data exchange with primary care EHRs and health plan systems
- HRIS integration (Workday, ADP, SAP SuccessFactors) for employer eligibility
- SSO/SAML enterprise identity management
- ERA auto-posting and insurance payment reconciliation

### AI-Assisted Care

- Ambient session documentation with transcription and AI-drafted progress note sections for clinician review
- Stepped-care routing using ML on assessment data (self-guided → coaching → therapy → psychiatry)
- Predictive deterioration detection from PHQ-9, GAD-7, and engagement signals
- Between-session AI therapeutic support delivering CBT exercises, mood check-ins, and crisis screening
- LLM-assisted evidence-based modality recommendation (CBT, DBT, ACT) based on diagnosis and history

---

## AI-Native Advantage

AI moves this platform beyond what incumbent EHRs and benefits platforms offer today. Precision stepped-care routing matches members to the right level of care using ML on assessments, comorbidities, and prior treatment response, instead of generic referral. Ambient documentation captures sessions and drafts structured notes, reducing clinician documentation burden. Predictive analytics on outcome-measure trends and engagement signals flag patients at elevated risk of crisis or dropout days before a clinical signal would otherwise surface, enabling proactive outreach.

---

## Tech Stack & Deployment

The platform is designed for both cloud-hosted SaaS and self-hosted deployments suitable for community mental health centres and FQHCs that require local data residency. Interoperability is built on **HL7 FHIR R4** for EHR and payer data exchange, with standard **837P / 835** transactions for claims and remittance. Validated public-domain instruments (PHQ-9, GAD-7) are implemented natively; diagnostic coding uses ICD-10-CM rather than copyrighted DSM-5-TR text. Telehealth is delivered through an embedded HIPAA-compliant video module rather than a third-party app.

---

## Market Context

The global digital mental health market was $33B in 2025 with an 18.6% CAGR, projected to reach $153B by 2034 (GlobeNewswire; Towards Healthcare); the mental health software segment alone is $6.1B in 2025, growing at 11.7% CAGR. Incumbent pricing spans $3–$8 PEPM for employer benefits (Lyra, Spring Health), $60–$110/week for consumer teletherapy (BetterHelp, Talkspace), and $29–$199/clinician/month for practice management (SimplePractice, Blueprint). Primary buyers include HR directors at mid-to-large employers, health-plan behavioural health VPs, independent therapists and group practices, and FQHCs and community mental health centres.

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

Licence to be determined. See [discussion](#) for context.

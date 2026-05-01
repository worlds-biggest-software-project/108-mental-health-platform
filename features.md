# Mental Health Platform — Feature & Functionality Survey

> Candidate #108 · Researched: 2026-05-01

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Lyra Health | Commercial SaaS (B2B employer) | Proprietary (private, $5.58B valuation) | lyrahealth.com |
| Spring Health | Commercial SaaS (B2B employer) | Proprietary (private, $3.3B valuation) | springhealth.com |
| BetterHelp (Teladoc Health) | Commercial SaaS (B2C / B2B) | Proprietary (Teladoc Health, NYSE: TDOC) | betterhelp.com |
| Talkspace | Commercial SaaS (B2C / B2B) | Proprietary (NASDAQ: TALK) | talkspace.com |
| SimplePractice | Commercial SaaS (clinician-facing) | Proprietary (private) | simplepractice.com |
| TherapyNotes | Commercial SaaS (clinician-facing) | Proprietary (private) | therapynotes.com |
| Osmind | Commercial SaaS (specialty psychiatry) | Proprietary (private) | osmind.org |
| Blueprint (Therapy Brands) | Commercial SaaS (clinician-facing) | Proprietary (Therapy Brands, PE-backed) | blueprint.ai |
| Eleos Health | Commercial SaaS (AI documentation) | Proprietary (private) | eleos.health |
| Woebot Health | Commercial SaaS (AI therapeutic chatbot) | Proprietary (private) | woebothealth.com |

## Feature Analysis by Solution

### Lyra Health

**Core features**
- Employer-sponsored mental health benefits platform with EAP replacement positioning
- AI-powered member assessment and stepped care matching (self-help → coaching → therapy → medication management)
- Network of 4,000+ vetted therapists and coaches with credentialing and outcomes monitoring
- Individual therapy, couples therapy, family therapy, and child therapy services
- Video, phone, and in-person therapy modalities
- Medication management with psychiatric providers
- Measurement-based care: PHQ-9, GAD-7 administered and trended within the platform
- Employer analytics dashboard: aggregate utilisation, engagement, and ROI metrics (de-identified)

**Differentiating features**
- Proprietary ML assessment model routes members to the right care level, reducing under- and over-treatment
- Outcomes-based provider payments (providers paid based on demonstrated member improvement)
- Lyra Renew residential programme for severe mental health and SUD
- Comprehensive family support including children (ages 2+) and adolescents
- Published peer-reviewed outcomes data showing clinical improvement rates

**UX patterns**
- Member-facing app with self-guided content, mood tracking, and session scheduling
- Employer portal for HR/benefits administrators with aggregate analytics
- Clinician portal for session notes, outcome measurement administration, and scheduling

**Integration points**
- HRIS integration (Workday, ADP, SAP SuccessFactors) for eligibility
- SSO/SAML for employer identity management
- HL7 FHIR R4 for payer and EHR data exchange (emerging)
- Claims submission via standard 837P professional claims

**Known gaps**
- Premium pricing restricts adoption to mid-to-large employers; SMB market underserved
- Network quality varies by geography; rural coverage is limited
- Limited support for serious mental illness (SMI) and complex psychiatric presentations

**Licence / IP notes**
- Fully proprietary; Lyra Health Inc. (private company, Menlo Park CA)
- No open-source components

---

### Spring Health

**Core features**
- Employer mental health benefits with EAP, coaching, therapy, and medication management
- Precision mental health: ML-based member assessment using standardised screening battery
- Network of 10,000+ providers including therapists, psychiatrists, and coaches
- Digital CBT exercises and self-guided wellness content
- Same-week appointment availability guarantee
- Care navigator support: human guides assist members in selecting and accessing services
- Measurement-based care with regular PHQ-9, GAD-7, and PC-PTSD-5 administration
- Group therapy and workshops

**Differentiating features**
- Precision mental health model using ML to personalise treatment type and modality recommendations
- Same-week appointment guarantee backed by network size and scheduling algorithms
- Spring Health Compass: AI-assisted treatment recommendations for clinicians based on member profile and evidence base
- Peer-reviewed clinical outcomes data; 79% of members show clinically significant improvement
- Expanded family and adolescent support

**UX patterns**
- Member onboarding assessment flow leading to personalised care recommendation
- Provider-matching interface with ratings, specialties, and earliest availability
- Employer admin dashboard with HEDIS-aligned reporting

**Integration points**
- HRIS and payroll system integrations for eligibility
- SSO/SAML enterprise identity
- EHR data feeds for integrated health plan programmes
- FHIR R4 for interoperability with health plan systems

**Known gaps**
- Rural network coverage gaps, similar to Lyra
- Serious psychiatric complexity (inpatient step-down, intensive outpatient) less developed
- Pricing model complexity for smaller employers

**Licence / IP notes**
- Fully proprietary; Spring Health Inc. (private, Series E $300M)

---

### BetterHelp (Teladoc Health)

**Core features**
- Largest online therapy marketplace with 30,000+ licensed therapists
- Text, video, phone, and live chat session modalities
- Asynchronous messaging between scheduled sessions
- Therapist matching based on presenting issues, preferences, and demographics
- Worksheets and journaling tools between sessions
- Group therapy sessions (Groupinars)
- Self-guided wellness content

**Differentiating features**
- Largest therapist network globally; broadest geographic and specialty coverage
- Asynchronous text-based therapy as a primary modality (not just a supplement)
- Consumer brand recognition driving organic member acquisition
- Lower access barrier than traditional therapy: starts at $60/week

**UX patterns**
- Simple consumer signup and matching flow (complete in under 10 minutes)
- Mobile-first application with messaging as the default session mode
- Therapist switch option available at any time without explanation required

**Integration points**
- Employer contracts via Teladoc Health enterprise sales
- Limited EHR integration (consumer-facing platform primarily)
- Insurance claim submission for BetterHelp for Employers programmes

**Known gaps**
- No native measurement-based care or outcomes tracking (a significant clinical quality gap)
- No medication management or psychiatric prescribing
- Quality control across 30,000 therapists is a persistent reputational challenge
- FTC settlement (2023) related to privacy practices ($7.8M); reputational and compliance risk

**Licence / IP notes**
- Proprietary; BetterHelp Inc., a subsidiary of Teladoc Health (NYSE: TDOC)

---

### Talkspace

**Core features**
- Online therapy and psychiatry via video, text, and audio
- Employer, health plan, and consumer channels
- Medication prescribing by psychiatric NPs and MDs
- Therapist messaging (asynchronous) and live video sessions
- Couples and teen therapy
- Talkspace for Business employer benefits programme

**Differentiating features**
- Integrated therapy and psychiatry in one platform (medication + therapy)
- Health plan partnerships enabling insurance-covered access (Cigna, Optum, etc.)
- Psychiatry prescribing available same-platform with coordinated care between therapist and prescriber

**UX patterns**
- Messaging-first interface for asynchronous therapy
- Medication management portal with prescription refill requests
- Teen-specific interface with parental access controls

**Integration points**
- Health plan billing and claims integration (837P professional claims)
- Employer SSO and eligibility integration
- Limited EHR connectivity

**Known gaps**
- Limited measurement-based care implementation
- Post-SPAC financial challenges have affected product investment
- Therapist engagement and retention issues reported

**Licence / IP notes**
- Proprietary; Talkspace Inc. (NASDAQ: TALK)

---

### SimplePractice

**Core features**
- Practice management and EHR for solo and group mental health practices
- Scheduling: online booking, automated appointment reminders
- Telehealth: integrated HIPAA-compliant video sessions
- Clinical documentation: progress notes, treatment plans, intake forms
- Billing: insurance claim submission (837P), payment processing, ERA posting
- Client portal for scheduling, document signing, and telehealth access
- HIPAA-compliant messaging with clients
- Measurement-based care: PHQ-9, GAD-7, PCL-5 administration and trending

**Differentiating features**
- Most widely adopted practice management platform for solo and small group mental health practices
- End-to-end practice operations in one system: scheduling, notes, billing, telehealth
- Client portal with self-service appointment booking and digital intake forms
- SimplePractice Telehealth: embedded video sessions without third-party app required

**UX patterns**
- Clean, modern interface designed for clinicians without IT support
- Calendar-centric scheduling with drag-and-drop appointment management
- Mobile app for clinician access between sessions

**Integration points**
- Surescripts for electronic prescription (limited)
- Standard 837P claims to all major payers
- Calendar sync (Google Calendar, iCal)
- Wiley Practice Planners for treatment plan templates

**Known gaps**
- Not designed for large group practices or health system behavioural health integration
- No AI documentation assistance (as of research date)
- Limited population-level analytics for group practice performance

**Licence / IP notes**
- Proprietary; SimplePractice LLC (private company)

---

### TherapyNotes

**Core features**
- EHR and practice management for mental health and behavioural health clinicians
- Scheduling with online booking and appointment reminders
- Clinical documentation: progress notes, treatment plans, initial assessments
- Integrated billing and claims management (837P)
- Telehealth module (TherapyNotes TeleHealth)
- Measurement-based care tools: PHQ-9, GAD-7, PCL-5
- Patient portal for scheduling and document access
- Group practice billing and multi-clinician management

**Differentiating features**
- Strong billing features including ERA auto-posting and insurance payment reconciliation
- Group practice management with per-clinician permissions and billing aggregation
- Specialised templates for psychiatry, psychology, LCSW, LMFT, and addiction counselling

**UX patterns**
- Note-template-driven documentation with guided sections for mental status examination
- Progress note locking and co-signature workflow for supervised clinicians
- Billing dashboard with outstanding claims and denial tracking

**Integration points**
- Standard 837P and 835 ERA for insurance billing
- Telehealth video via integrated TherapyNotes module
- State immunisation and reporting connections (limited)

**Known gaps**
- Less polished UI than SimplePractice
- No AI documentation features
- Limited FHIR interoperability for health system integration

**Licence / IP notes**
- Proprietary; TherapyNotes LLC (private company)

---

### Osmind

**Core features**
- Specialised EHR for ketamine infusion, TMS, esketamine, and emerging psychiatry practices
- Treatment session documentation with modality-specific templates (IV ketamine, TMS protocol tracking)
- Measurement-based care: PHQ-9, GAD-7, MADRS, Columbia Suicide Severity Rating Scale (C-SSRS)
- Patient outcomes analytics across treatment modalities
- Scheduling and prior authorisation documentation for emerging treatments
- Patient-facing app for symptom journaling and assessment completion

**Differentiating features**
- Only purpose-built EHR for ketamine and TMS practices; competitors use generic mental health EHRs
- Integrated outcomes registry enabling benchmarking across Osmind network practices
- C-SSRS administration built in natively (required for ketamine programmes)
- Patient outcomes research publication partnerships using de-identified Osmind network data

**UX patterns**
- Infusion session flow documentation with vital signs integration
- Automated patient assessment scheduling at defined treatment milestones
- Outcomes dashboard showing treatment response curves for individual patients

**Integration points**
- HL7 FHIR for EHR data exchange
- Standard billing (837P claims)
- Pharmacy integration for ketamine compounding documentation
- Insurance prior authorisation documentation workflow

**Known gaps**
- Narrowly focused on emerging psychiatric treatments; not suitable for general mental health practice
- Limited telehealth capability
- Small market segment; growth dependent on ketamine and TMS market expansion

**Licence / IP notes**
- Proprietary; Osmind Inc. (private company, San Francisco)

---

### Blueprint (Therapy Brands)

**Core features**
- Clinical workflow automation for behavioural health practices
- Measurement-based care engine: automated assessment administration (PHQ-9, GAD-7, PCL-5, SRS, ORS)
- AI-generated session documentation: automated progress note drafts from session transcription
- Treatment planning with outcome-linked goal tracking
- Client portal for assessment completion and appointment scheduling
- Billing integration with standard 837P claims
- Group therapy workflow management

**Differentiating features**
- AI-generated progress notes from session audio transcription reduces documentation time significantly
- Comprehensive measurement-based care automation: right assessment, at right interval, automatically administered
- Treatment planning linked to outcome measures with visual progress tracking
- Largest behavioural health technology company (Therapy Brands consolidates Blueprint, TheraNest, ICANotes, and others)

**UX patterns**
- AI documentation assistant embedded in session workflow: transcribes and drafts notes in real time
- Assessment result visualisations showing client progress trajectory
- Template library for evidence-based treatment protocols (CBT, DBT, ACT)

**Integration points**
- HL7 FHIR R4 for health system connectivity
- Standard 837P billing
- Calendar integrations
- Telehealth module

**Known gaps**
- AI note quality depends on audio quality and session structure; requires clinician review before finalising
- Multiple legacy Therapy Brands products being consolidated; user experience varies by product line
- Post-PE acquisition integration complexity

**Licence / IP notes**
- Proprietary; Therapy Brands LLC (PE-backed, Warburg Pincus)
- No open-source components

---

### Eleos Health

**Core features**
- AI-powered clinical documentation for behavioural health providers
- Session audio transcription and AI-generated progress note drafts
- Measurement-based care administration integrated with documentation workflow
- Treatment plan auto-population from session content
- Quality metrics dashboard for supervisors: note completion rates, MBC compliance, session content analysis
- Integration with existing EHR systems as a documentation layer

**Differentiating features**
- Focused purely on AI documentation and quality improvement — works as an add-on to existing EHRs
- Designed for community mental health centres (CMHCs) and FQHCs, not just private practices
- Supervisor analytics: session content themes, adherence to evidence-based treatment delivery
- Ambient documentation: clinician does not need to take notes during session; AI captures and structures

**UX patterns**
- Ambient recording consent and activation at session start
- Post-session review screen: AI-drafted note sections with accept/edit controls
- Quality dashboard for clinical supervisors with session-level analytics

**Integration points**
- EHR connectors: Epic, Oracle Health, Netsmart, Credible (CMHC-focused)
- HL7 FHIR R4 for data exchange
- Assessment platform connectors for MBC data flow

**Known gaps**
- Requires existing EHR; does not replace a full practice management system
- Audio recording consent complexity in states with two-party consent requirements
- AI note accuracy varies by session structure and ambient noise

**Licence / IP notes**
- Proprietary; Eleos Health Inc. (private company)

---

### Woebot Health

**Core features**
- AI-powered conversational therapeutic chatbot delivering CBT-based interventions
- Mood tracking and daily check-ins via conversational interface
- Evidence-based skill delivery: CBT thought records, behavioural activation, mindfulness
- Crisis screening with human escalation pathways
- Employer and health plan deployment for population-level wellness
- Clinician dashboard for monitoring engaged patient populations

**Differentiating features**
- Pioneer in evidence-based AI conversational therapy; multiple RCTs published on efficacy
- 24/7 availability between scheduled therapy sessions extends therapeutic support continuously
- FDA Breakthrough Device Designation (2021) for specific mental health indications — among first AI therapy products to receive this
- Low-intensity, scalable intervention for mild-to-moderate depression and anxiety

**UX patterns**
- Conversational chat interface (mobile app) with structured CBT exercises delivered through dialogue
- Daily mood check-in with mood trend visualization
- Skill library for self-guided exercises between conversations

**Integration points**
- Employer and health plan API for eligibility and utilisation reporting
- EHR data export for clinician visibility (limited)
- Crisis escalation pathways to human crisis lines

**Known gaps**
- Not a replacement for human therapy; appropriate only for mild-to-moderate presentations
- FDA regulatory pathway for AI therapeutic software is still evolving; commercial scaling depends on regulatory clarity
- Limited integration with clinical EHR and practice management workflows

**Licence / IP notes**
- Proprietary; Woebot Health Inc. (private company)
- No open-source components; AI model is proprietary

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- HIPAA-compliant data storage with elevated protection for psychotherapy notes (45 CFR § 164.524) and 42 CFR Part 2 SUD records (enforced from February 2026)
- Scheduling with automated appointment reminders (SMS, email)
- HIPAA-compliant telehealth video sessions
- Clinical documentation: progress notes, treatment plans, intake assessments
- Insurance billing: 837P professional claims submission, ERA payment posting
- Patient/member portal for scheduling, intake forms, and document access
- Validated outcome measure administration: PHQ-9, GAD-7 (table stakes for any clinical credibility)
- Crisis screening and escalation pathway documentation

### Differentiating Features
- AI-powered precision matching to the right care level using ML on assessment data (Lyra, Spring Health)
- AI ambient documentation: session transcription and automated progress note drafting (Blueprint, Eleos)
- Outcomes-based provider payment model tied to demonstrated member improvement (Lyra)
- 24/7 AI conversational therapeutic support between sessions (Woebot)
- Integrated medication management with psychiatric prescribing on the same platform (Talkspace)
- Specialty-specific EHR for emerging psychiatric treatments: ketamine, TMS, esketamine (Osmind)
- Employer analytics dashboard with HEDIS-aligned aggregate utilisation metrics (Lyra, Spring Health)
- FDA Breakthrough Device Designation for AI therapeutic software (Woebot)

### Underserved Areas / Opportunities
- Seamless primary care to behavioural health transition with shared clinical record (most platforms are siloed from primary care EHRs)
- Affordable full-featured mental health platform for FQHCs, CMHCs, and safety-net providers (most AI features are priced for commercial employers or private practices)
- Predictive crisis identification from passive session data and PHQ-9 trends before the crisis event
- 42 CFR Part 2-compliant SUD module integrated with mental health workflow (enforcement begins February 2026; most platforms not yet fully compliant)
- Group practice supervision tools with AI-assisted quality monitoring of session adherence to evidence-based protocols
- Interoperability with primary care EHRs via HL7 FHIR R4 for true integrated behavioural health

### AI-Augmentation Candidates
- Precision stepped-care routing: ML model on assessment battery predicts optimal care level and modality
- Ambient session documentation: real-time transcription with AI-generated structured progress note draft
- Predictive deterioration detection: ML trend analysis on PHQ-9, GAD-7, session sentiment to flag high-risk patients
- Between-session AI therapeutic support: CBT exercises, mood check-ins, and crisis screening via conversational AI
- Automated MBC administration: AI-triggered assessment at clinically optimal intervals with alert on deterioration
- AI treatment recommendation: LLM-assisted evidence-based modality selection (CBT vs. DBT vs. ACT) based on diagnosis, patient history, and preferences

## Legal & IP Summary

| Tool | Licence Type | Embedding Risk |
|------|-------------|----------------|
| Lyra Health | Proprietary (private) | Cannot embed; commercial licence required |
| Spring Health | Proprietary (private) | Cannot embed; commercial licence required |
| BetterHelp / Teladoc | Proprietary (NYSE: TDOC) | Cannot embed; commercial licence required; FTC privacy settlement history — additional reputational due diligence advised |
| Talkspace | Proprietary (NASDAQ: TALK) | Cannot embed; commercial licence required |
| SimplePractice | Proprietary (private) | Cannot embed; commercial licence required |
| TherapyNotes | Proprietary (private) | Cannot embed; commercial licence required |
| Osmind | Proprietary (private) | Cannot embed; commercial licence required |
| Blueprint / Therapy Brands | Proprietary (PE-backed) | Cannot embed; commercial licence required |
| Eleos Health | Proprietary (private) | Cannot embed; commercial licence required |
| Woebot Health | Proprietary (private) | Cannot embed; AI model proprietary; FDA regulatory status requires monitoring |

No GPL or AGPL components are identified in the primary competitor set. The PHQ-9 and GAD-7 validated instruments are in the public domain (developed by Pfizer and Spitzer et al. respectively) and can be freely implemented. The DSM-5-TR is copyrighted by the American Psychiatric Association; diagnostic coding implementation should use ICD-10-CM codes (public domain in the U.S.) rather than DSM verbatim text. 42 CFR Part 2 creates a significant compliance obligation (effective February 2026) that any SUD-adjacent mental health platform must address in its data architecture and consent workflows.

## Recommended Feature Scope

**Must-have (MVP)**:
- HIPAA-compliant clinical data architecture with elevated psychotherapy note protection (45 CFR § 164.524) and 42 CFR Part 2-compliant SUD record handling from launch
- Scheduling with automated SMS/email appointment reminders and self-service online booking
- HIPAA-compliant integrated telehealth video sessions
- Clinical documentation: structured progress notes, treatment plans, intake assessments with ICD-10-CM diagnostic coding
- Validated outcome measure administration and trending: PHQ-9, GAD-7 at minimum; PCL-5 and C-SSRS as configurable additions
- Insurance billing: 837P professional claims submission and 835 ERA payment posting
- Client/member portal: scheduling, intake forms, secure messaging, document signing
- Crisis screening protocol with documented escalation pathway

**Should-have (v1.1)**:
- AI ambient documentation: session audio transcription with AI-drafted progress note sections for clinician review and approval
- Measurement-based care automation: AI-triggered assessment delivery at optimal clinical intervals with deterioration alerts to clinician
- Stepped care routing: ML-based assessment and care level recommendation (self-guided → coaching → therapy → psychiatry)
- Employer analytics dashboard with de-identified aggregate utilisation and outcomes metrics
- Group practice management: multi-clinician scheduling, billing aggregation, supervision workflow with co-signature
- HL7 FHIR R4 integration for data exchange with primary care EHRs and health plan systems

**Nice-to-have (backlog)**:
- Predictive crisis and deterioration detection using passive engagement signals and outcome measure trends
- Between-session AI therapeutic support: CBT-based conversational AI with crisis escalation integrated with the care team
- AI treatment modality recommendation using evidence-based matching of diagnosis, history, and patient preferences
- Specialty psychiatry module for emerging treatments (ketamine, TMS, esketamine) with protocol-specific documentation templates
- Consumer-facing mental health app with mood tracking and self-guided wellness content (separate from clinical platform)

# Mental Health Platform

> Candidate #108 · Researched: 2026-05-01

## Existing Products and Software Packages

| Name | Description | Model | Pricing |
|------|-------------|-------|---------|
| Lyra Health | AI-powered employer mental health benefits platform; therapy, coaching, medication management, and family support; uses ML-driven assessments to match members to appropriate care | B2B SaaS (employer-sponsored) | Per-employee-per-month (PEPM); typically $3–$8 PEPM |
| Spring Health | Employer behavioral health benefits; precision mental health using ML-based assessments; EAP, coaching, therapy, medication management; partners with 4,500+ therapists | B2B SaaS (employer-sponsored) | Custom PEPM pricing |
| BetterHelp (Teladoc Health) | Largest online therapy marketplace; connects members to licensed therapists via text, video, and phone; consumer and employer-facing | B2C / B2B | $60–$100/week consumer; custom employer contracts |
| Talkspace | Online therapy and psychiatry; employer, payer, and consumer channels; video, text, and audio sessions; medication prescribing | B2C / B2B | $69–$109/week consumer; custom enterprise |
| Headspace Health (merged with Ginger) | Combined mindfulness and behavioral health coaching platform; text-based coaching, self-guided content, and therapy for employers | B2B SaaS | Custom PEPM |
| Calm for Business | Mindfulness and mental wellness app with employer wellness tier; sleep content, guided meditations, stress tools | B2B SaaS | ~$15–$20/employee/year |
| Blueprint (formerly Therapy Brands) | Clinical workflow platform for therapists and behavioral health practices; treatment planning, measurement-based care, billing, scheduling | SaaS | $49–$199/clinician/month |
| SimplePractice | Practice management and EHR for solo and group mental health practices; scheduling, telehealth, billing, treatment notes | SaaS | $29–$99/month per clinician |
| Osmind | Specialized EHR for ketamine, TMS, and emerging psychiatry practices; measurement-based care, patient outcomes tracking | SaaS | Custom pricing |
| Quartet Health (now part of Evernorth) | Collaborative care platform connecting PCPs to behavioral health providers; referral management, outcomes tracking | B2B / Payer-facing | Custom enterprise pricing |

## Relevant Industry Standards or Protocols

| Standard | Relevance |
|----------|-----------|
| HIPAA Privacy and Security Rules (45 CFR Parts 160, 164) | Core compliance framework for all mental health platforms handling PHI; psychotherapy notes receive heightened protection under 45 CFR § 164.524 and require separate authorization |
| 42 CFR Part 2 (Confidentiality of SUD Records) | Federal regulation protecting substance use disorder treatment records; Final Rule effective April 16, 2024 (enforcement from February 16, 2026) requires separate patient consent for SUD counseling notes; applies to mental health platforms treating co-occurring SUD |
| 45 CFR § 164.524 (HIPAA Psychotherapy Notes) | Psychotherapy notes maintained separately from the medical record and used solely by the treating clinician receive elevated protection; mental health platforms must distinguish these from progress notes |
| Promoting Interoperability (PI) / Meaningful Use | CMS incentive program promoting EHR adoption including behavioral health EHRs; requires CCDA-based transitions of care and patient electronic access |
| HL7 FHIR R4 | API-based data exchange standard; increasingly required for mental health platform interoperability with EHRs and payer systems under CMS interoperability rules |
| PHQ-9 / GAD-7 / PCL-5 (Validated Measurement Tools) | Standardized assessment instruments for depression, anxiety, and PTSD; not regulatory standards but clinically required for measurement-based care and outcomes reporting |
| DSM-5-TR (APA Diagnostic Criteria) | Diagnostic and Statistical Manual of Mental Disorders, Fifth Edition Text Revision; governs diagnostic coding and clinical criteria used in treatment planning modules |
| CPT Codes for Telehealth (98970–98972, 99441–99443) | Billing codes relevant to synchronous and asynchronous telemental health services; platform billing modules must support these and state-specific telehealth parity laws |

## Available Research Materials

| Citation | Type |
|----------|------|
| Torous, J. et al. (2021). "Digital mental health and COVID-19: using technology today to accelerate the curve on access and quality tomorrow." *JMIR Mental Health*, 8(3), e26568. | Commentary |
| Linardon, J. et al. (2020). "The efficacy of app-supported smartphone interventions for mental health problems: a meta-analysis of randomized controlled trials." *World Psychiatry*, 19(3), 325–336. | Meta-analysis |
| Mohr, D.C. et al. (2017). "Three problems with current digital mental health research... and three things we can do about them." *Psychiatric Services*, 68(5), 427–429. | Commentary |
| Andersson, G. & Titov, N. (2014). "Advantages and limitations of Internet-based interventions for common mental health problems." *World Psychiatry*, 13(1), 4–11. | Review article |
| Hollis, C. et al. (2024). "The evolving field of digital mental health: current evidence and implementation issues for smartphone apps, generative artificial intelligence, and virtual reality." *PMC12079407*. | Review article |
| Fortney, J.C. et al. (2024). "Impacts of Telehealth Adoption on the Quality of Care for Individuals With Serious Mental Illness: Retrospective Observational Analysis of Veterans Affairs Administrative Data." *JMIR Mental Health*, 11, e56886. | Retrospective study |
| Reinholt Dunster-Page, C. et al. (2024). "Predictors of Engagement in Multiple Modalities of Digital Mental Health Treatments: Longitudinal Study." *Journal of Medical Internet Research*, 26, e48696. | Longitudinal study |
| Topooco, N. et al. (2018). "Attitudes towards digital treatment for depression: a European stakeholder survey." *Internet Interventions*, 8, 1–9. | Survey study |
| Miner, A.S. et al. (2016). "Smartphone-based conversational agents and responses to questions about mental health, interpersonal violence, and physical health." *JAMA Internal Medicine*, 176(5), 619–625. | Empirical study |

## Market Research

**Market Size:**
- Global digital mental health market: $33 billion in 2025, growing at 18.6% CAGR to reach $153 billion by 2034 (GlobeNewswire; Towards Healthcare)
- Mental health software specifically: $6.1 billion in 2025, projected at $18.4 billion by 2035, CAGR 11.7% (Towards Healthcare)
- Mental health technology (platforms + devices): $15.2 billion in 2024, projected $31 billion by 2030, CAGR 12.6% (Yahoo Finance)

**Pricing Landscape:**

| Segment | Typical Pricing |
|---------|----------------|
| Employer-sponsored EAP/benefits (Lyra, Spring Health) | $3–$8 PEPM; 6–10 sessions covered per employee per year |
| Consumer teletherapy (BetterHelp, Talkspace) | $60–$110/week; subscription model |
| Clinician practice management (SimplePractice, Blueprint) | $29–$199/clinician/month |
| Enterprise / payer platform (Quartet, Optum Behavioral) | Custom contract; typically PMPM (per-member-per-month) |
| Wellness / mindfulness apps (Calm for Business) | $10–$25/employee/year |

**Key Buyer Personas:**
- HR Directors and Chief People Officers at mid-to-large employers
- Health plan medical directors and behavioral health VPs
- Independent therapists and group behavioral health practices
- Federally Qualified Health Centers (FQHCs) and community mental health centers
- Health systems building integrated behavioral health programs

**Notable Funding / Acquisitions:**
- Lyra Health: $235M Series F at $5.58B valuation (2021); total funding $900M+
- Spring Health: $300M Series E at $3.3B valuation (2024); total funding $600M+
- Headspace merged with Ginger in 2021 at ~$3B combined valuation; subsequently restructured
- Teladoc Health acquired BetterHelp parent (Lifeline Health) for $1.5B (2021)
- Talkspace went public via SPAC at $1.4B (2021); share price declined significantly post-SPAC
- Quartet Health acquired by Evernorth (Cigna subsidiary) in 2022

## AI-Native Opportunity

- **Precision matching and stepped care routing:** AI can analyze member assessments, symptom trajectories, comorbidities, and previous treatment responses to route individuals to exactly the right level of care (app-based self-help vs. coaching vs. therapy vs. psychiatry) instead of generic referral, reducing time-to-appropriate-treatment and avoiding under- or over-treatment
- **Between-session AI therapeutic support:** Conversational AI can provide evidence-based CBT exercises, mood check-ins, and crisis screening between scheduled sessions, addressing the fundamental limitation of weekly 50-minute therapy by extending support to 24/7 availability
- **Predictive crisis identification:** Passive sensing data (typing patterns, session notes sentiment, PHQ-9 trends) combined with ML can identify patients at elevated risk of crisis or dropout days before a clinical signal surfaces, enabling proactive outreach
- **Automated measurement-based care:** AI can administer validated assessments (PHQ-9, GAD-7) at optimal intervals, trend scores over time, alert clinicians to deterioration, and auto-populate treatment plan progress notes, reducing clinician documentation burden
- **Personalized treatment recommendation:** LLMs trained on clinical literature and outcomes data can suggest evidence-based treatment modalities (CBT vs. ACT vs. DBT vs. medication), accounting for diagnosis, patient preferences, and prior treatment history in a way that individual clinicians rarely have time to execute

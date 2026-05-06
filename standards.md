# Standards & API Reference

> Project: Mental Health Platform · Generated: 2026-05-06

## Industry Standards & Specifications

### US Federal Regulatory Frameworks

**HIPAA Privacy and Security Rules (45 CFR Parts 160 and 164)**
- URL: https://www.hhs.gov/hipaa/index.html
- The foundational US privacy and security framework for all entities handling Protected Health Information (PHI). Mental health platforms must implement administrative, physical, and technical safeguards. Psychotherapy notes maintained separately from the general medical record (45 CFR § 164.524) receive heightened protection: they require a separate written authorisation for disclosure and are excluded from the general right of access. Any platform storing session transcripts, AI-generated progress notes, or therapist process notes must implement this distinction at the data model level.

**42 CFR Part 2 — Confidentiality of Substance Use Disorder Patient Records**
- URL: https://www.ecfr.gov/current/title-42/chapter-I/subchapter-A/part-2 and https://www.hhs.gov/hipaa/part-2/index.html
- Federal regulations protecting SUD treatment records with protections stricter than HIPAA. The 2024 Final Rule (effective April 16, 2024; civil enforcement by HHS OCR began February 16, 2026) harmonises Part 2 with HIPAA, allowing a single patient consent for all future treatment, payment, and healthcare operations (TPO) disclosures — a significant change that simplifies integrated care workflows. Criminal penalties remain for non-TPO disclosures. Any mental health platform treating or documenting co-occurring SUD conditions must implement a separate data classification and consent workflow for Part 2 records; this is now actively enforced.

**TEFCA — Trusted Exchange Framework and Common Agreement**
- URL: https://www.healthit.gov/topic/interoperability/policy/trusted-exchange-framework-and-common-agreement-tefca and https://rce.sequoiaproject.org/tefca/
- The ONC-led national interoperability framework establishing a common floor for health information exchange (HIE) between Qualified Health Information Networks (QHINs). QHIN-to-QHIN FHIR exchange is being piloted in 2025 with Stage 3 implementation targeted for 2026. Over 21,000 organisations are live on TEFCA. Mental health platforms seeking to participate in national health information exchange — particularly for care transitions from primary care, hospitals, or specialist referrals — should design for TEFCA-compliant FHIR exchange. TEFCA's expanded exchange purposes (treatment, payment, operations, public health) are directly relevant to behavioural health data sharing.

**USCDI+ Behavioral Health Dataset**
- URL: https://build.fhir.org/ig/HL7/us-behavioral-health-profiles/index.html
- The United States Core Data for Interoperability Plus Behavioral Health (USCDI+ BH) dataset, developed by ONC/ASTP and SAMHSA as part of the Behavioral Health Information Technology (BHIT) Initiative, defines the standardised data elements for behavioural health information exchange across US healthcare systems. It extends USCDI with behavioural-health-specific classes including mental health clinical notes, SUD treatment history, validated screening instruments (PHQ-9, GAD-7, PCL-5), and care team member roles. Any mental health EHR targeting interoperability with health systems or payers should align its data model to USCDI+ BH elements.

---

### HL7 Standards

**HL7 FHIR R4 (Fast Healthcare Interoperability Resources, Release 4)**
- URL: https://www.hl7.org/fhir/overview.html
- The current production standard for healthcare data APIs. FHIR R4 is built on REST, JSON/XML, and OAuth 2.0, making it accessible to modern web developers. CMS interoperability rules mandate FHIR R4 for patient data access APIs. Key FHIR resources for a mental health platform include: `Patient`, `Practitioner`, `Appointment`, `Encounter`, `ClinicalImpression`, `Observation` (for PHQ-9/GAD-7 scores), `Condition` (ICD-10-CM diagnosis codes), `CarePlan`, `MedicationRequest`, `Consent`, and `DocumentReference` (for psychotherapy notes and session recordings). The FHIR Consent resource is the primary mechanism for representing 42 CFR Part 2 patient consent at the API level.

**HL7 US Behavioral Health Profiles Implementation Guide v0.1.0**
- URL: https://build.fhir.org/ig/HL7/us-behavioral-health-profiles/index.html and https://www.fhir.org/guides/astp/bhp/
- An HL7 FHIR Implementation Guide funded by SAMHSA as part of the BHIT Initiative, developed by Next Level Health Innovations and Lantana Consulting Group. It provides FHIR profiles crosswalked to USCDI+ BH data elements, including the Mental Health Clinical Notes profile for psychotherapy note exchange. This is the emerging canonical FHIR profile set for US behavioural health data exchange and should be the basis for FHIR API design in a mental health platform.

**HL7 Cross-Paradigm Implementation Guide: Behavioral Health Data Exchange, Release 1**
- URL: https://www.hl7.org/implement/standards/product_brief.cfm?product_id=462
- An earlier HL7 implementation guide covering CDA (Clinical Document Architecture) and other HL7 messaging paradigms for behavioural health data exchange. Useful for legacy integration with older EHR systems that have not yet adopted FHIR R4.

**HL7 Version 3 Domain Analysis Model: Behavioral Health Record, Release 2**
- URL: https://www.hl7.org/implement/standards/product_brief.cfm?product_id=307
- The HL7 domain analysis model defining the conceptual structure of a behavioural health record. Provides the canonical vocabulary and relationship model for mental health concepts including diagnoses, treatments, care plans, and outcomes — relevant for data model design.

**HL7 CDA R2 (Clinical Document Architecture, Release 2) / C-CDA**
- URL: https://www.hl7.org/implement/standards/product_brief.cfm?product_id=7
- The structured document standard used for care summaries and transitions of care (Continuity of Care Documents, Discharge Summaries). Required for Promoting Interoperability / Meaningful Use compliance and still widely used for hospital-to-practice data exchange. A mental health EHR receiving referrals from hospitals should be able to ingest C-CDA documents and extract the relevant behavioural health data elements.

---

### ISO Standards

**ISO/EN 13606 — Electronic Health Record Communication (2019 revision)**
- URL: http://www.en13606.org/information.html and https://www.iso.org/standard/52823.html
- The international standard for EHR data exchange, providing a dual-model approach (reference model plus archetypes) for semantic interoperability. ISO 13606:2019 includes Part 5 on interface specification. More widely adopted in European healthcare than in the US, but relevant for mental health platforms targeting international markets.

**ISO 18308:2011 — Requirements for an Electronic Health Record Architecture**
- URL: https://www.iso.org/standard/52823.html
- Defines the architecture requirements for EHR systems, including security, privacy, and data integrity requirements. Relevant as a framework for the technical architecture design of a mental health EHR.

**ISO 27001 / ISO 27799 — Information Security Management in Healthcare**
- URL: https://www.iso.org/isoiec-27001-information-security.html
- ISO 27001 is the baseline information security management standard. ISO 27799 extends ISO 27001 with healthcare-specific guidance. Mental health platforms handling psychotherapy notes and SUD records are prime targets for information security certification under these standards, particularly for enterprise and health plan sales that require vendor security attestations.

---

### W3C & IETF Standards

**SMART App Launch Framework v2.2.0 (HL7/SMART Health IT)**
- URL: https://build.fhir.org/ig/HL7/smart-app-launch/ and https://docs.smarthealthit.org/
- SMART (Substitutable Medical Applications and Reusable Technologies) is the standard framework for launching and authorising clinical applications against FHIR APIs. It layers OAuth 2.0 and OpenID Connect with healthcare-specific launch contexts and scopes (e.g., `patient/Observation.rs`, `user/CarePlan.cruds`). SMART App Launch v2.2.0 supports EHR launch (launched from within an EHR), standalone launch, and backend services (machine-to-machine, no user in the loop). Any third-party application integrating with a mental health EHR — such as an AI documentation tool or an employer analytics dashboard — should use SMART on FHIR for authorisation.

**OAuth 2.0 (RFC 6749) and OpenID Connect 1.0**
- URL: https://datatracker.ietf.org/doc/html/rfc6749 (OAuth 2.0) and https://openid.net/specs/openid-connect-core-1_0.html (OIDC)
- The foundational authorisation and authentication standards underlying SMART on FHIR, SSO/SAML federation with employer HRIS systems, and patient portal identity management. FHIR APIs should implement OAuth 2.0 with PKCE for public clients. Enterprise deployments must support SAML 2.0 for HRIS SSO (Workday, ADP, SAP SuccessFactors) alongside OpenID Connect.

**HEART (Health Relationship Trust) Profile for FHIR OAuth 2.0 Scopes**
- URL: https://openid.net/specs/openid-heart-fhir-oauth2-1_0.html
- An OpenID Foundation working group specification defining interoperable patient-directed data exchange using FHIR, OAuth 2.0, OpenID Connect, and UMA (User-Managed Access). HEART is specifically designed for patient consent-driven access — directly applicable to the patient consent model required for sharing behavioural health records across care settings.

**RFC 7231 — Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content**
- URL: https://datatracker.ietf.org/doc/html/rfc7231
- The baseline standard for RESTful API design. FHIR R4 REST APIs must conform to HTTP/1.1 semantics.

**RFC 8288 — Web Linking**
- URL: https://datatracker.ietf.org/doc/html/rfc8288
- Standard for web link headers used in FHIR pagination (Bundle navigation links) and SMART discovery (.well-known endpoints).

---

### Data Model & Terminology Standards

**SNOMED CT (Systematized Nomenclature of Medicine — Clinical Terms)**
- URL: https://www.snomed.org/ and https://pmc.ncbi.nlm.nih.gov/articles/PMC6115234/
- The world's largest clinical terminology, covering diagnoses, clinical findings, procedures, and observable entities. SNOMED CT covers mental health conditions (e.g., depressive episode, generalised anxiety disorder, PTSD) and maps to ICD-10 for billing. Used as the value set for FHIR Condition codes in USCDI-compliant systems. Note that research has identified significant gaps in SNOMED CT coverage of psychological assessment instruments, particularly for less common validated screening tools.

**LOINC (Logical Observation Identifiers, Names, and Codes)**
- URL: https://loinc.org/ and https://loinc.org/45420-7 (Mental Health History)
- The international standard for clinical and laboratory observations, including survey instruments. LOINC's SURVEY.MLTHLTH class covers commonly used mental health assessment instruments. LOINC codes are required for FHIR Observation resources representing PHQ-9 (LOINC 44249-1), GAD-7 (LOINC 69737-5), and PCL-5 (LOINC 97722-2) scores. The PHQ-9 and GAD-7 instruments themselves are in the public domain and can be freely implemented.

**ICD-10-CM Diagnosis Codes**
- URL: https://www.cms.gov/medicare/coding-billing/icd-10-codes and https://elitemedfinancials.com/mental-health-billing-codes/
- The US standard for diagnosis coding in clinical documentation and insurance billing. Mental health platforms must support ICD-10-CM F-codes (F01–F99 Mental, Behavioural, and Neurodevelopmental Disorders) for diagnosis documentation. DSM-5-TR diagnostic criteria map to ICD-10-CM codes; platforms should implement ICD-10-CM codes (public domain) rather than DSM-5-TR text (copyrighted by the APA). Z-codes (e.g., Z13.31 for depression screening) are also required for preventive and screening encounters.

**CPT Codes for Mental Health and Telehealth Services**
- URL: https://elitemedfinancials.com/mental-health-cpt-codes/ and https://connectedmind.me/blog/cpt-codes-mental-health-screening-guide
- AMA Current Procedural Terminology (CPT) codes are required for insurance claims. Key mental health CPT codes include: 90791 (psychiatric diagnostic evaluation, no medical services), 90792 (psychiatric diagnostic evaluation with medical services), 90832/90834/90837 (psychotherapy 30/45/60 min), 90838 (60-minute psychotherapy add-on with E/M), 99202–99215 (E/M codes for psychiatrists), 96127/96130/96136/96138 (psychological testing). Telehealth modifiers: -95 (synchronous audio-video), -93 or FQ (audio-only), POS 10 (patient at home). As of January 2026, CMS has approved mental health screening/testing codes 96127, 96130, 96136, and 96138 for telemedicine use through December 31, 2026.

**RxNorm**
- URL: https://www.nlm.nih.gov/research/umls/rxnorm/
- The NLM standard for clinical drug nomenclature, required for FHIR MedicationRequest resources in platforms supporting psychiatric prescribing or medication management. Maps to NDC codes for pharmacy dispensing.

**OpenAPI Specification 3.1**
- URL: https://spec.openapis.org/oas/v3.1.0
- The de facto standard for documenting REST APIs, including FHIR server capability statements. Any mental health platform exposing a partner or developer API should publish an OpenAPI 3.1 specification.

---

### Security & Compliance Standards

**NIST SP 800-53 Revision 5.2 — Security and Privacy Controls for Information Systems**
- URL: https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final
- The comprehensive catalogue of security and privacy controls applicable to information systems. Rev 5.2 (2025) added controls addressing software resiliency, developer testing, and software integrity validation. Healthcare organisations subject to HIPAA can map 800-53 controls to the HIPAA Security Rule, and this framework is increasingly required by enterprise health plan and employer clients in vendor security assessments.

**NIST SP 800-228 — Guidelines for API Security in Cloud-Native Systems**
- URL: https://equixly.com/blog/2025/11/17/nist-sp-800-228/
- Guidelines for securing APIs in cloud-native systems, relevant for any FHIR-based mental health platform API. Covers API authentication, authorisation, rate limiting, logging, and input validation in regulated environments.

**OWASP Application Security Verification Standard (ASVS)**
- URL: https://owasp.org/www-project-application-security-verification-standard/
- A comprehensive framework for web application security testing and verification. OWASP ASVS demonstrates alignment with HIPAA security requirements and is increasingly referenced in healthcare procurement. The OWASP Mobile Application Security Verification Standard (MASVS) and Mobile Security Testing Guide (MASTG) apply to patient-facing mobile apps on iOS and Android.

**ONC API Privacy & Security Considerations**
- URL: https://www.healthit.gov/sites/default/files/privacy-security-api.pdf
- ONC guidance specifically addressing privacy and security considerations for healthcare APIs, covering key-management, access controls, audit logging, and breach notification requirements for FHIR-based APIs. Directly applicable to any mental health platform building a FHIR API for data exchange.

---

### EU / International Regulatory Standards

**GDPR — General Data Protection Regulation (EU 2016/679)**
- URL: https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32016R0679 and https://secureprivacy.ai/blog/mental-health-app-data-privacy-hipaa-gdpr-compliance
- Applies to any mental health platform processing data of EU residents, regardless of where the platform is headquartered. Mental health records are "special category" personal data under Article 9, requiring explicit consent, Data Protection Impact Assessments (DPIAs), privacy by design, and a Data Protection Officer (DPO) if processing at scale. Penalties reach €20 million or 4% of global annual revenue. Extraterritorial application is particularly relevant for platforms marketed internationally.

**EU AI Act (Regulation 2024/1689)**
- URL: https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai and https://artificialintelligenceact.eu/article/6/
- The EU's AI regulatory framework, with compliance obligations for high-risk AI systems taking effect August 2026. Mental health AI systems (precision diagnosis support, crisis detection, AI treatment recommendations) may be classified as high-risk under Annex III (AI systems intended for use in healthcare). Compliance obligations for high-risk systems include: risk management system, conformity assessment, registration in the EU AI Act database, CE marking, and mandatory human oversight. AI features deployed in EU markets must be designed with these requirements from the outset.

---

## Similar Products — Developer Documentation & APIs

### Elation Health EHR

- **Description:** Cloud-based primary care EHR with strong behavioral health integration capabilities. Widely used by primary care practices that co-manage patients with behavioral health conditions. Their API is used for building applications that interface with patient records, care teams, and appointments.
- **API Documentation:** https://docs.elationhealth.com/reference/api-overview
- **Developer Platform:** https://www.elationhealth.com/developer-platform/
- **Developer Sandbox:** https://www.elationhealth.com/contact-us/sandbox/
- **GitHub:** https://github.com/elationemr
- **Standards:** RESTful API (JSON), FHIR-first design, OpenAPI
- **Authentication:** OAuth 2.0, SMART on FHIR
- **Notes:** Elation offers a fully open, documented developer platform with a sandbox environment — a model to emulate for any mental health EHR building a partner ecosystem. Their FHIR-first approach is particularly relevant.

### SimplePractice (Enterprise API)

- **Description:** The most widely adopted practice management platform for solo and small group mental health practices, serving over 225,000 practitioners. Their Enterprise API enables health plans and employers to connect provider availability and scheduling for member access.
- **API Documentation:** https://www.simplepractice.com/press/simplepractice-enterprise-launches-api/ (Enterprise partnership; no public developer portal)
- **Health Plans API:** https://www.simplepractice.com/health-plans/
- **Standards:** REST/JSON (presumed); details not publicly disclosed
- **Authentication:** Enterprise partnership agreements; SSO/SAML for health plan members
- **Notes:** SimplePractice's API is available via enterprise/health plan partnership, not a public developer program. The primary integration use case is payer-facilitated scheduling access to the SimplePractice provider network.

### TherapyNotes

- **Description:** A full-featured behavioral health EHR serving solo and group practices, with strong billing and clinical documentation capabilities. As of 2026, TherapyNotes does not expose a native REST API; third-party integration is facilitated through partners.
- **Native API:** Not available (no public API)
- **Third-Party Integration:** Supergood (unofficial API wrapper): https://docs.supergood.ai/therapynotes-api-2/
- **Integration Platforms:** Keragon (https://www.keragon.com/integrations/therapynotes), Redox, Mulesoft
- **Notes:** The absence of a native API is a significant limitation and competitive gap. A mental health platform offering an open FHIR API would differentiate strongly against TherapyNotes for practices seeking interoperability.

### Blueprint (Therapy Brands)

- **Description:** AI-powered clinical workflow platform for behavioral health practices, combining an EHR with AI documentation assistance (session transcription and automated progress note generation), measurement-based care, and treatment planning.
- **API Documentation:** https://www.blueprint.ai/platform/ehr (product overview; no public developer portal identified)
- **EHR Features:** https://www.blueprint.ai/platform/ehr
- **Standards:** HL7 FHIR R4 (for health system connectivity), standard 837P billing
- **Authentication:** HIPAA-compliant; SSO for enterprise deployments
- **Notes:** Blueprint's API documentation is not publicly available; integration is through enterprise sales. Their FHIR R4 implementation for health system connectivity is an important reference point.

### Eleos Health (AI Documentation Layer)

- **Description:** AI-powered clinical documentation platform for behavioral health providers, operating as an add-on layer to existing EHRs. Designed specifically for community mental health centers (CMHCs) and FQHCs. Notably, Eleos uses a browser extension approach rather than a traditional API, making it EHR-agnostic without requiring EHR vendor API partnerships.
- **Documentation:** https://eleos.health/documentation/
- **Integration Approach:** Browser extension overlay on web-based EHRs (no API integration required for basic deployment)
- **EHR Connectors:** Epic, Oracle Health, Netsmart, Credible (FHIR-based deeper integrations)
- **Standards:** HL7 FHIR R4 for EHR data exchange integrations
- **Authentication:** Enterprise SSO for clinical staff; HIPAA BAA required
- **Notes:** The browser extension approach is architecturally novel — it solves the EHR integration problem without requiring API partnerships. A mental health platform building an AI documentation module should consider this as an alternative to full EHR API integration for faster deployment.

### Woebot Health (Enterprise AI Chatbot)

- **Description:** AI-powered conversational therapeutic chatbot delivering evidence-based CBT interventions. As of June 2025, the consumer app was shut down; Woebot operates exclusively in the enterprise B2B model, integrating with health plans, employers, and provider organisations. Multiple published RCTs exist for efficacy.
- **API Documentation:** Not publicly available (enterprise partnerships only)
- **Platform Documentation:** https://woebothealth.com/ (enterprise contact required)
- **Standards:** EMR system integration available via enterprise agreements; specific standards not disclosed
- **Authentication:** Enterprise SSO; health plan eligibility API integration
- **Notes:** Woebot's FDA Breakthrough Device Designation (2021) and pivot to pure enterprise in 2025 establish a model for how AI therapeutic software is commercialised. Their API is not public; integration requires enterprise partnership. A mental health platform building between-session AI support should monitor Woebot Health's FDA regulatory pathway as a precedent.

### Osmind EHR (Specialty Psychiatry)

- **Description:** Purpose-built EHR for interventional and emerging psychiatry practices (ketamine, TMS, esketamine, psychedelic medicine). Serves 800+ independent psychiatric practices with specialty-specific documentation templates, C-SSRS administration, and outcomes benchmarking across the Osmind network.
- **API Documentation:** No public developer API identified
- **Platform:** https://www.osmind.org/
- **Standards:** Standard 837P billing; HIPAA-compliant telehealth
- **Authentication:** Clinical staff authentication; HIPAA BAA with practices
- **Notes:** Osmind's narrow specialisation and absence of a public API means that practices using Osmind operate in an isolated data environment. A mental health platform building specialty psychiatry modules should consider FHIR R4 as the interoperability bridge.

### Teladoc Health / BetterHelp (Wellbound Enterprise Platform)

- **Description:** Teladoc Health launched Wellbound in late 2025, integrating BetterHelp's online therapy network with Teladoc's broader virtual care platform into a unified EAP replacement product for employers. Available to plan sponsors with member access from January 2026.
- **Enterprise API Documentation:** Not publicly available
- **Developer Resources:** Enterprise integration via Teladoc Health partnerships
- **Standards:** SSO/SAML for employer identity federation; insurance claims integration (837P)
- **Authentication:** Single sign-on for member access across BetterHelp and Teladoc services
- **Notes:** The Wellbound launch represents Teladoc's strategy to consolidate fragmented EAP, therapy, and virtual care into a single platform. Their enterprise integration is partnership-based. No public developer API is available.

### AWS HealthLake / Google Cloud Healthcare API (Cloud Health Data Platforms)

- **Description:** Managed cloud services providing FHIR R4 data stores with built-in SMART on FHIR authorisation, de-identification, and analytics. Relevant as infrastructure options for a mental health platform storing and querying FHIR-formatted clinical data at scale.
- **AWS HealthLake SMART on FHIR:** https://docs.aws.amazon.com/healthlake/latest/devguide/reference-smart-on-fhir-oauth-scopes.html
- **Google Cloud Healthcare API SMART on FHIR:** https://docs.cloud.google.com/healthcare-api/docs/smart-on-fhir
- **Standards:** FHIR R4, SMART App Launch v2, OAuth 2.0 scopes
- **Authentication:** SMART on FHIR OAuth 2.0
- **Notes:** Both platforms provide managed FHIR infrastructure with compliant authentication. Using a managed FHIR store (AWS HealthLake or Google Cloud Healthcare API) avoids building FHIR server infrastructure from scratch and provides a HIPAA-eligible, SOC 2-attested data layer for a mental health platform.

---

## Notes

**Areas with evolving or incomplete standards coverage:**

1. **AI-generated clinical documentation:** No established standard governs AI-generated progress notes, session transcriptions, or automated treatment recommendations. The clinical and regulatory status of AI-generated documentation (particularly whether AI-drafted notes constitute the clinician's legal medical record entry once signed) is being actively addressed by state medical boards and CMS. Platform builders should design for mandatory clinician review and attestation before finalising any AI-generated note.

2. **42 CFR Part 2 FHIR implementation:** Implementing the Part 2 consent model in FHIR (using the Consent resource with appropriate policy references and restriction codes) is not yet standardised in a published HL7 Implementation Guide. The FHIR Consent resource supports the technical representation, but platform teams should monitor the ASTP/ONC USCDI+ BH work for emerging guidance on standard FHIR Consent profiles for Part 2 records.

3. **Validated assessment instruments in FHIR:** LOINC covers the most common instruments (PHQ-9, GAD-7, PCL-5, C-SSRS) but has significant gaps for less common validated instruments. Platforms building comprehensive measurement-based care modules should expect to implement custom FHIR Observation profiles for instruments not yet fully codified in LOINC.

4. **EU AI Act mental health classification:** It is not yet definitively resolved whether AI clinical decision support systems in mental health (e.g., stepped-care routing models, crisis prediction) will be classified as high-risk under Annex III of the EU AI Act. Platform teams targeting EU markets should obtain legal review of their AI features against the August 2026 compliance deadline.

5. **TEFCA behavioural health exchange:** TEFCA's current Technical Framework does not yet include explicit guidance for behavioural health data exchange, particularly the handling of 42 CFR Part 2-protected records within QHIN-mediated exchange. SAMHSA and ONC are expected to address this gap as FHIR exchange (Stage 3) is implemented in 2026.

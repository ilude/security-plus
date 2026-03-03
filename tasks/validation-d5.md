# Domain 5 Glossary Validation Report

**Date**: 2026-03-03
**Validated against**: CompTIA Security+ SY0-701 Exam Objectives (Version 5.0)
**Sources used**:
- [Official CompTIA SY0-701 Exam Objectives PDF](https://assets.ctfassets.net/82ripq7fjls2/6TYWUym0Nudqa8nGEnegjG/0f9b974d3b1837fe85ab8e6553f4d623/CompTIA-Security-Plus-SY0-701-Exam-Objectives.pdf)
- [Professor Messer SY0-701 Course](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/sy0-701-comptia-security-plus-course/)
- [Proftia SY0-701 Study Guide](https://proftia.com/resources/securityplus-objectives.html)
- [InfoSecTrain Domain 5 Breakdown](https://www.infosectrain.com/blog/comptia-security-domain-5-security-program-management/)
- [CertStudyHub Objective 5.4](https://certstudyhub.com/blog/security-plus/objective-5-4-summarize-elements-effective-security-compliance/)
- [Pearson IT Certification - Risk Management](https://www.pearsonitcertification.com/articles/article.aspx?p=3197451)

---

## Official Domain 5 Objective Structure (Reference)

### 5.1 — Summarize elements of effective security governance
- Guidelines
- Policies: AUP, Information security policies, Business continuity, Disaster recovery, Incident response, SDLC, Change management
- Standards: Password, Access control, Physical security, Encryption
- Procedures: Change management, Onboarding/offboarding, Playbooks
- External considerations: Regulatory, Legal, Industry, Local/regional, National, Global
- Monitoring and revision
- Types of governance structures: Boards, Committees
- Government entities
- Centralized/decentralized
- Roles and responsibilities for systems and data: Owners, Controllers, Processors, Custodians/stewards

### 5.2 — Explain elements of the risk management process
- Risk identification
- Risk assessment: Ad hoc, Recurring, One-time, Continuous
- Risk analysis: Qualitative, Quantitative, SLE, ALE, ARO, Probability, Likelihood, Exposure factor, Impact
- Risk register: Key risk indicators, Risk owners, Risk threshold
- Risk tolerance
- Risk appetite: Expansionary, Conservative, Neutral
- Risk management strategies: Transfer, Accept (Exemption/Exception), Avoid, Mitigate
- Risk reporting
- Business impact analysis: RTO, RPO, MTTR, MTBF

### 5.3 — Explain the processes associated with third-party risk assessment and management
- Vendor assessment: Penetration testing, Right-to-audit clause, Evidence of internal audits, Independent assessments, Supply chain analysis
- Vendor selection: Due diligence, Conflict of interest
- Agreement types: SLA, MOA, MOU, MSA, WO/SOW, NDA, BPA
- Vendor monitoring
- Questionnaires
- Rules of engagement

### 5.4 — Summarize elements of effective security compliance
- Compliance reporting: Internal, External
- Consequences of non-compliance: Fines, Sanctions, Reputational damage, Loss of license, Contractual impacts
- Compliance monitoring: Due diligence/care, Attestation and acknowledgement, Internal and external, Automation
- Privacy: Legal implications (Local/regional, National, Global), Data subject, Controller vs. processor, Ownership, Data inventory and retention, Right to be forgotten

### 5.5 — Explain types and purposes of audits and assessments
- Attestation
- Internal: Compliance, Audit committee, Self-assessments
- External: Regulatory, Examinations, Assessment, Independent third-party audit
- Penetration testing: Physical, Offensive, Defensive, Integrated, Known environment, Partially known environment, Unknown environment, Reconnaissance (Passive/Active)

### 5.6 — Given a scenario, implement security awareness practices
- Phishing: Campaigns, Recognizing a phishing attempt, Responding to reported suspicious messages
- Anomalous behavior recognition: Risky, Unexpected, Unintentional
- User guidance and training: Policy/handbooks, Situational awareness, Insider threat, Password management, Removable media and cables, Social engineering, Operational security, Hybrid/remote work environments
- Reporting and monitoring: Initial, Recurring
- Development
- Execution

---

## Section 42: Security Governance — Validation

### Document Hierarchy (Policy/Standard/Procedure/Guideline)

| Item | Status | Notes |
|------|--------|-------|
| Policy (definition, mandatory) | **VALID** | 5.1 — Policies |
| Standard (definition, measurable) | **VALID** | 5.1 — Standards |
| Procedure (step-by-step) | **VALID** | 5.1 — Procedures |
| Guideline (recommendations, not mandatory) | **VALID** | 5.1 — Guidelines |
| Decision rules table | **VALID** | Useful exam-prep content mapping to official items |

### Key Policy Types

| Item | Status | Notes |
|------|--------|-------|
| Information security policy | **VALID** | 5.1 — Policies |
| Acceptable Use Policy (AUP) | **VALID** | 5.1 — Policies |
| Business continuity policy | **VALID** | 5.1 — Policies |
| Disaster recovery policy | **VALID** | 5.1 — Policies |
| Incident response policy | **VALID** | 5.1 — Policies |
| SDLC policy | **VALID** | 5.1 — Policies |
| Change management policy | **VALID** | 5.1 — Policies |

### Key Standards

| Item | Status | Notes |
|------|--------|-------|
| Password standards | **VALID** | 5.1 — Standards |
| Access control standards | **VALID** | 5.1 — Standards |
| Physical security standards | **VALID** | 5.1 — Standards |
| Encryption standards | **VALID** | 5.1 — Standards |

### Key Procedures

| Item | Status | Notes |
|------|--------|-------|
| Onboarding | **VALID** | 5.1 — Procedures (Onboarding/offboarding) |
| Offboarding | **VALID** | 5.1 — Procedures (Onboarding/offboarding) |
| Change management procedure | **VALID** | 5.1 — Procedures (Change management) |
| Playbook | **VALID** | 5.1 — Procedures (Playbooks) |
| CAB (Change Advisory Board) mention | **INFERRED** | Not explicitly listed but standard change management terminology; widely tested |

### External Considerations

| Item | Status | Notes |
|------|--------|-------|
| Regulatory (GDPR, HIPAA, PCI DSS, SOX) | **VALID** | 5.1 — External considerations (Regulatory) |
| Legal (e-discovery, legal hold) | **VALID** | 5.1 — External considerations (Legal) |
| Industry (NERC CIP, SWIFT CSP) | **VALID** | 5.1 — External considerations (Industry) |
| Local/regional (CCPA) | **VALID** | 5.1 — External considerations (Local/regional) |
| National (FISMA, UK Cyber Essentials) | **VALID** | 5.1 — External considerations (National) |
| Global (EAR, ITAR) | **VALID** | 5.1 — External considerations (Global) |

### Policy Monitoring and Revision

| Item | Status | Notes |
|------|--------|-------|
| Policy lifecycle | **INFERRED** | 5.1 — Monitoring and revision. The lifecycle concept is not an explicit sub-bullet, but the official objective "monitoring and revision" clearly implies ongoing lifecycle management |
| Periodic review | **INFERRED** | Same reasoning as above |
| Revision triggers | **INFERRED** | Same reasoning as above |

### Governance Structures

| Item | Status | Notes |
|------|--------|-------|
| Board of directors | **VALID** | 5.1 — Governance structures (Boards) |
| Security committee | **VALID** | 5.1 — Governance structures (Committees) |
| Government entities | **VALID** | 5.1 — Government entities |
| Centralized governance | **VALID** | 5.1 — Centralized/decentralized |
| Decentralized governance | **VALID** | 5.1 — Centralized/decentralized |

### MISSING FROM SECTION 42

| Official Objective Item | Status | Notes |
|------------------------|--------|-------|
| Roles and responsibilities (Owners, Controllers, Processors, Custodians/stewards) | **MISSING FROM CONTENT** | 5.1 explicitly lists "Roles and responsibilities for systems and data" with sub-bullets: Owners, Controllers, Processors, Custodians/stewards. This is NOT covered in Section 42. **Must be added.** |

---

## Section 43: Risk Management Expanded — Validation

### Risk Identification Methods

| Item | Status | Notes |
|------|--------|-------|
| Brainstorming | **QUESTIONABLE** | Not explicitly listed as a sub-bullet under 5.2. The official objective says only "Risk identification" as a top-level bullet with no sub-items. Brainstorming is a valid method but goes beyond what the exam explicitly lists. |
| Interviews | **QUESTIONABLE** | Same as above |
| Historical data | **QUESTIONABLE** | Same as above |
| Threat modeling | **QUESTIONABLE** | Same as above — threat modeling is more commonly tested under Domain 2/3 |

### Risk Assessment Types

| Item | Status | Notes |
|------|--------|-------|
| Ad hoc | **VALID** | 5.2 — Risk assessment |
| Recurring | **VALID** | 5.2 — Risk assessment |
| One-time | **VALID** | 5.2 — Risk assessment |
| Continuous | **VALID** | 5.2 — Risk assessment |

### Risk Tracking Tools

| Item | Status | Notes |
|------|--------|-------|
| Risk register | **VALID** | 5.2 — Risk register |
| Risk matrix | **INFERRED** | Not an explicit sub-bullet but a standard risk analysis visualization tool; widely tested |
| Risk heat map | **INFERRED** | Same as risk matrix — commonly tested visual tool |
| KRI (Key Risk Indicator) | **VALID** | 5.2 — Risk register (Key risk indicators) |

### Risk Appetite vs Risk Tolerance

| Item | Status | Notes |
|------|--------|-------|
| Risk appetite | **VALID** | 5.2 — Risk appetite |
| Risk tolerance | **VALID** | 5.2 — Risk tolerance |
| Risk threshold | **VALID** | 5.2 — Risk register (Risk threshold) |
| Expansionary | **VALID** | 5.2 — Risk appetite |
| Conservative | **VALID** | 5.2 — Risk appetite |
| Neutral | **VALID** | 5.2 — Risk appetite |

### Risk Management Strategies

| Item | Status | Notes |
|------|--------|-------|
| Transfer | **VALID** | 5.2 — Risk management strategies |
| Accept | **VALID** | 5.2 — Risk management strategies |
| Avoid | **VALID** | 5.2 — Risk management strategies |
| Mitigate | **VALID** | 5.2 — Risk management strategies |
| Exemption vs Exception | **VALID** | 5.2 — Accept (Exemption/Exception) |

### Risk Reporting

| Item | Status | Notes |
|------|--------|-------|
| Risk reporting | **VALID** | 5.2 — Risk reporting |
| Risk dashboard | **INFERRED** | Not explicitly listed but a reasonable elaboration of risk reporting |

### Risk Analysis

| Item | Status | Notes |
|------|--------|-------|
| Qualitative | **VALID** | 5.2 — Risk analysis |
| Quantitative | **VALID** | 5.2 — Risk analysis |

### MISSING FROM SECTION 43

| Official Objective Item | Status | Notes |
|------------------------|--------|-------|
| SLE (Single Loss Expectancy) | **MISSING FROM CONTENT** | 5.2 explicitly lists SLE under Risk analysis. The glossary mentions it only in the risk strategy decision rules. **Needs a dedicated entry with formula: SLE = AV x EF** |
| ALE (Annualized Loss Expectancy) | **MISSING FROM CONTENT** | 5.2 explicitly lists ALE. **Needs a dedicated entry with formula: ALE = SLE x ARO** |
| ARO (Annualized Rate of Occurrence) | **MISSING FROM CONTENT** | 5.2 explicitly lists ARO. **Needs a dedicated entry with definition** |
| Probability | **MISSING FROM CONTENT** | 5.2 — Risk analysis sub-bullet |
| Likelihood | **MISSING FROM CONTENT** | 5.2 — Risk analysis sub-bullet |
| Exposure factor | **MISSING FROM CONTENT** | 5.2 — Risk analysis sub-bullet. **Needs definition: percentage of asset value lost when a threat occurs** |
| Impact | **MISSING FROM CONTENT** | 5.2 — Risk analysis sub-bullet |
| Risk owners | **MISSING FROM CONTENT** | Mentioned briefly in risk register table text, but not a standalone glossary entry. 5.2 explicitly lists it under Risk register. |
| Business impact analysis (BIA) | **MISSING FROM CONTENT** | 5.2 explicitly lists BIA with sub-items RTO, RPO, MTTR, MTBF. These are completely absent from the Domain 5 glossary. **Critical gap — must be added.** |
| RTO (Recovery Time Objective) | **MISSING FROM CONTENT** | 5.2 — BIA sub-item |
| RPO (Recovery Point Objective) | **MISSING FROM CONTENT** | 5.2 — BIA sub-item |
| MTTR (Mean Time to Repair) | **MISSING FROM CONTENT** | 5.2 — BIA sub-item |
| MTBF (Mean Time Between Failures) | **MISSING FROM CONTENT** | 5.2 — BIA sub-item |

---

## Section 44: Third-Party Risk Management Expanded — Validation

### Vendor Assessment Methods

| Item | Status | Notes |
|------|--------|-------|
| Penetration testing of vendor | **VALID** | 5.3 — Vendor assessment |
| Right-to-audit clause | **VALID** | 5.3 — Vendor assessment |
| Evidence of internal audits | **VALID** | 5.3 — Vendor assessment |
| Independent assessments | **VALID** | 5.3 — Vendor assessment |
| Supply chain analysis | **VALID** | 5.3 — Vendor assessment |
| Security questionnaire | **VALID** | 5.3 — Questionnaires |

### Rules of Engagement

| Item | Status | Notes |
|------|--------|-------|
| Rules of engagement | **VALID** | 5.3 — Rules of engagement |
| Scope | **INFERRED** | Standard component of RoE |
| Authorized activities | **INFERRED** | Standard component of RoE |

### Vendor Monitoring

| Item | Status | Notes |
|------|--------|-------|
| Ongoing monitoring | **VALID** | 5.3 — Vendor monitoring |
| Performance metrics | **INFERRED** | Reasonable elaboration of vendor monitoring |
| Compliance verification | **INFERRED** | Reasonable elaboration of vendor monitoring |

### Vendor Selection

| Item | Status | Notes |
|------|--------|-------|
| Due diligence | **VALID** | 5.3 — Vendor selection |
| Conflict of interest | **VALID** | 5.3 — Vendor selection |
| Minimum security requirements | **INFERRED** | Not explicitly listed but commonly discussed in vendor selection context |

### Supply Chain Risks

| Item | Status | Notes |
|------|--------|-------|
| Hardware providers (tampered components) | **INFERRED** | Supply chain analysis is listed; specific risk categories are reasonable elaborations |
| Software providers (SolarWinds-style) | **INFERRED** | Same reasoning |
| MSPs | **INFERRED** | Same reasoning |

### Agreement Types

| Item | Status | Notes |
|------|--------|-------|
| SLA | **MISSING FROM CONTENT** | 5.3 explicitly lists SLA under Agreement types. The glossary mentions SLA in passing but has NO dedicated agreement types section. **Critical gap — all 7 agreement types must be added.** |
| MOA | **MISSING FROM CONTENT** | 5.3 — Agreement types |
| MOU | **MISSING FROM CONTENT** | 5.3 — Agreement types |
| MSA | **MISSING FROM CONTENT** | 5.3 — Agreement types |
| WO/SOW | **MISSING FROM CONTENT** | 5.3 — Agreement types |
| NDA | **MISSING FROM CONTENT** | 5.3 — Agreement types |
| BPA | **MISSING FROM CONTENT** | 5.3 — Agreement types |

---

## Section 45: Security Compliance — Validation

### Compliance Monitoring

| Item | Status | Notes |
|------|--------|-------|
| Due diligence | **VALID** | 5.4 — Compliance monitoring |
| Due care | **VALID** | 5.4 — Compliance monitoring |
| Attestation | **VALID** | 5.4 — Compliance monitoring |
| Acknowledgement | **VALID** | 5.4 — Compliance monitoring (Attestation and acknowledgement) |
| Internal monitoring | **VALID** | 5.4 — Compliance monitoring (Internal and external) |
| External monitoring | **VALID** | 5.4 — Compliance monitoring (Internal and external) |
| Compliance automation | **VALID** | 5.4 — Compliance monitoring (Automation) |

### Privacy Compliance

| Item | Status | Notes |
|------|--------|-------|
| Data subject | **VALID** | 5.4 — Privacy |
| Data inventory | **VALID** | 5.4 — Privacy (Data inventory and retention) |
| Data retention | **VALID** | 5.4 — Privacy (Data inventory and retention) |
| Right to be forgotten | **VALID** | 5.4 — Privacy |

### Compliance Reporting

| Item | Status | Notes |
|------|--------|-------|
| Internal reporting | **VALID** | 5.4 — Compliance reporting (Internal) |
| External reporting | **VALID** | 5.4 — Compliance reporting (External) |

### Consequences of Non-Compliance

| Item | Status | Notes |
|------|--------|-------|
| Fines | **VALID** | 5.4 — Consequences of non-compliance |
| Sanctions | **VALID** | 5.4 — Consequences of non-compliance |
| Reputational damage | **VALID** | 5.4 — Consequences of non-compliance |
| Loss of license | **VALID** | 5.4 — Consequences of non-compliance |
| Contractual impacts | **VALID** | 5.4 — Consequences of non-compliance |

### MISSING FROM SECTION 45

| Official Objective Item | Status | Notes |
|------------------------|--------|-------|
| Controller vs. processor | **MISSING FROM CONTENT** | 5.4 — Privacy explicitly lists "Controller vs. processor." While Section 42 mentions controllers/processors in the governance roles context (5.1), Section 45 does NOT cover the privacy-specific distinction under 5.4. These are different contexts: 5.1 = data governance roles, 5.4 = privacy compliance implications. **Should add the privacy compliance angle.** |
| Ownership | **MISSING FROM CONTENT** | 5.4 — Privacy explicitly lists "Ownership." Not covered in the compliance section. |
| Legal implications (Local/regional, National, Global) | **MISSING FROM CONTENT** | 5.4 — Privacy explicitly lists legal implications with geographic scope sub-items. While external considerations are covered under 5.1 in Section 42, the 5.4 privacy-specific legal implications are not addressed in Section 45. |

---

## Section 46: Audits and Assessments — Validation

### Attestation

| Item | Status | Notes |
|------|--------|-------|
| Attestation | **VALID** | 5.5 — Attestation |

### Internal Audits

| Item | Status | Notes |
|------|--------|-------|
| Compliance audit (internal) | **VALID** | 5.5 — Internal (Compliance) |
| Audit committee | **VALID** | 5.5 — Internal (Audit committee) |
| Self-assessment | **VALID** | 5.5 — Internal (Self-assessments) |

### External Audits

| Item | Status | Notes |
|------|--------|-------|
| Regulatory audit | **VALID** | 5.5 — External (Regulatory) |
| Examination | **VALID** | 5.5 — External (Examinations) |
| Assessment | **VALID** | 5.5 — External (Assessment) |
| Independent third-party audit | **VALID** | 5.5 — External (Independent third-party audit) |

### Penetration Testing

| Item | Status | Notes |
|------|--------|-------|
| Physical penetration testing | **VALID** | 5.5 — Penetration testing (Physical) |
| Offensive (red team) | **VALID** | 5.5 — Penetration testing (Offensive) |
| Defensive (blue team) | **VALID** | 5.5 — Penetration testing (Defensive) |
| Integrated (purple team) | **VALID** | 5.5 — Penetration testing (Integrated) |
| Known environment | **VALID** | 5.5 — Penetration testing |
| Partially known environment | **VALID** | 5.5 — Penetration testing |
| Unknown environment | **VALID** | 5.5 — Penetration testing |
| Passive reconnaissance | **VALID** | 5.5 — Reconnaissance (Passive) |
| Active reconnaissance | **VALID** | 5.5 — Reconnaissance (Active) |
| Terminology change note (white/gray/black box) | **VALID** | Useful exam-prep context; the exam uses new terms |

### Section 46 — No Missing Items

Section 46 achieves complete coverage of objective 5.5.

---

## Section 47: Security Awareness Practices — Validation

### Phishing Campaigns

| Item | Status | Notes |
|------|--------|-------|
| Simulated phishing campaign | **VALID** | 5.6 — Phishing (Campaigns) |
| Click rate | **INFERRED** | Standard metric for phishing campaigns; not explicitly listed |
| Reporting rate | **INFERRED** | Standard metric; not explicitly listed |
| Responding to reported messages | **VALID** | 5.6 — Phishing (Responding to reported suspicious messages) |

### Anomalous Behavior Recognition

| Item | Status | Notes |
|------|--------|-------|
| Risky behavior | **VALID** | 5.6 — Anomalous behavior recognition (Risky) |
| Unexpected behavior | **VALID** | 5.6 — Anomalous behavior recognition (Unexpected) |
| Unintentional behavior | **VALID** | 5.6 — Anomalous behavior recognition (Unintentional) |

### User Training Topics

| Item | Status | Notes |
|------|--------|-------|
| Policy and handbooks | **VALID** | 5.6 — User guidance and training (Policy/handbooks) |
| Situational awareness | **VALID** | 5.6 — User guidance and training |
| Insider threat awareness | **VALID** | 5.6 — User guidance and training (Insider threat) |
| Password management | **VALID** | 5.6 — User guidance and training |
| Removable media and cables | **VALID** | 5.6 — User guidance and training |
| Social engineering recognition | **VALID** | 5.6 — User guidance and training (Social engineering) |
| OPSEC | **VALID** | 5.6 — User guidance and training (Operational security) |
| Hybrid and remote work | **VALID** | 5.6 — User guidance and training (Hybrid/remote work environments) |

### Reporting and Monitoring

| Item | Status | Notes |
|------|--------|-------|
| Clear reporting channels | **INFERRED** | 5.6 lists "Reporting and monitoring" with "Initial" and "Recurring" sub-items. The glossary elaborates on reporting channels which is implied but not the exact sub-bullet structure. |
| Metrics tracking | **INFERRED** | Not an explicit sub-item but reasonable elaboration |
| Improvement tracking | **INFERRED** | Same reasoning |

### Program Development

| Item | Status | Notes |
|------|--------|-------|
| Role-based training | **INFERRED** | Not explicitly listed; reasonable elaboration of "Development" |
| Training frequency | **INFERRED** | Same reasoning |
| Gamification | **QUESTIONABLE** | Not listed in the official objectives. May be too specific/out of scope for the exam. |
| Executive buy-in | **INFERRED** | Not explicitly listed but commonly tested concept |

### MISSING FROM SECTION 47

| Official Objective Item | Status | Notes |
|------------------------|--------|-------|
| Recognizing a phishing attempt | **MISSING FROM CONTENT** | 5.6 explicitly lists "Recognizing a phishing attempt" as a sub-bullet under Phishing. The glossary covers campaigns and responding but does NOT cover recognition indicators (what makes an email look phishy). **Should add.** |
| Reporting and monitoring — Initial vs Recurring | **MISSING FROM CONTENT** | 5.6 explicitly lists "Initial" and "Recurring" as sub-items under Reporting and monitoring. The glossary does not distinguish between initial reporting and recurring reporting. **Should add these as distinct concepts.** |
| Execution | **MISSING FROM CONTENT** | 5.6 explicitly lists "Execution" as a top-level bullet. The glossary has "Program Development" but no separate "Execution" section. **Should add.** |

---

## Summary

### Coverage Statistics

| Section | Valid | Inferred | Questionable | Missing |
|---------|-------|----------|-------------|---------|
| 42 — Security Governance | 21 | 4 | 0 | 1 |
| 43 — Risk Management | 14 | 3 | 4 | 12 |
| 44 — Third-Party Risk | 10 | 7 | 0 | 7 |
| 45 — Security Compliance | 12 | 0 | 0 | 3 |
| 46 — Audits and Assessments | 12 | 0 | 0 | 0 |
| 47 — Security Awareness | 12 | 6 | 1 | 3 |
| **TOTAL** | **81** | **20** | **5** | **26** |

### Critical Gaps (Must Fix)

These items are **explicitly listed** in the official exam objectives but are completely absent from the glossary:

1. **5.1 — Roles and responsibilities for systems and data** (Owners, Controllers, Processors, Custodians/stewards) — Missing from Section 42. This is a standalone top-level bullet with 4 sub-items.

2. **5.2 — Quantitative risk analysis formulas** (SLE, ALE, ARO, Exposure factor) — Missing from Section 43. These are explicitly listed sub-bullets and are high-frequency exam questions. The formulas SLE = AV x EF and ALE = SLE x ARO must be included.

3. **5.2 — Risk analysis sub-items** (Probability, Likelihood, Impact) — Missing from Section 43.

4. **5.2 — Business Impact Analysis** (RTO, RPO, MTTR, MTBF) — Completely missing from Section 43. This is an explicit top-level bullet under 5.2 with 4 sub-items. These are among the most commonly tested items on the exam.

5. **5.3 — Agreement types** (SLA, MOA, MOU, MSA, WO/SOW, NDA, BPA) — Missing from Section 44. This is a top-level bullet under 5.3 with 7 sub-items. These are heavily tested on the exam.

6. **5.4 — Privacy sub-items** (Controller vs. processor [compliance context], Ownership, Legal implications with geographic scope) — Missing from Section 45.

7. **5.6 — Recognizing a phishing attempt** — Missing from Section 47. Explicit sub-bullet.

8. **5.6 — Reporting: Initial vs Recurring** — Missing from Section 47. Explicit sub-items.

9. **5.6 — Execution** — Missing from Section 47. Explicit top-level bullet.

### Questionable Items (Consider Removing or Flagging)

These items are not explicitly in the objectives and may lead to studying non-testable content:

1. **Risk identification methods** (Brainstorming, Interviews, Historical data, Threat modeling) in Section 43 — The official objectives list only "Risk identification" with no sub-items. These methods are valid but go beyond what the exam explicitly calls for.

2. **Gamification** in Section 47 — Not listed in the official objectives under 5.6.

### Verdict

The glossary provides excellent **depth** on the topics it covers, with strong decision-rule tables and exam-oriented explanations. However, it has significant **breadth gaps** — several complete objective sub-sections are missing entirely (agreement types, BIA metrics, quantitative formulas, data roles). These are high-frequency exam topics. The glossary should not be considered complete for Domain 5 study until the 26 missing items identified above are added.

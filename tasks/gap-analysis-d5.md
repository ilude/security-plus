# Domain 5 Gap Analysis — Security Program Management and Oversight (20%)

Coverage assessment of study materials (glossary.md, concept-walkthrough.md, notes.md) against official SY0-701 Domain 5 exam objectives.

**Legend**: COVERED | PARTIAL | MISSING

---

## 5.1 — Summarize Elements of Effective Security Governance

### Guidelines
- **MISSING** — No coverage of security guidelines as a governance document type. The distinction between guidelines (recommendations, not mandatory) vs. policies/standards/procedures is not addressed.

### Policies
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Acceptable Use Policy (AUP) | **PARTIAL** | Glossary defines AUP in one line. Missing: enforcement mechanisms, typical contents, onboarding context. |
| Information security policies | **MISSING** | No coverage of overarching infosec policy structure or what it contains. |
| Business continuity | **PARTIAL** | Glossary covers BCP definition and BCP vs DRP distinction. Missing: policy document aspects — what a BC policy mandates vs. what the plan contains. |
| Disaster recovery | **PARTIAL** | Glossary covers DRP definition. Same gap as BC — policy vs. plan distinction not addressed. |
| Incident response | **PARTIAL** | Glossary covers IR steps well. Missing: IR as a governance policy document (who approves, escalation authority, communication plan). |
| Software development lifecycle (SDLC) | **MISSING** | No coverage of SDLC as a governance policy. Shift-left mentioned only as an exam term. No secure SDLC lifecycle phases. |
| Change management | **MISSING** | Not covered as a governance policy. No content on change advisory boards, approval workflows, rollback procedures, or documentation requirements. |

### Standards
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Password standards | **MISSING** | No coverage of password policy standards (length, complexity, history, expiration). |
| Access control standards | **PARTIAL** | Glossary covers access control models (MAC/DAC/RBAC/ABAC) well. Missing: organizational access control standards as governance documents. |
| Physical security standards | **MISSING** | No coverage of physical security standards (badge access, visitor logs, mantraps, surveillance). |
| Encryption standards | **PARTIAL** | Glossary covers crypto algorithms thoroughly. Missing: organizational encryption standards as governance documents (data-at-rest policy, TLS requirements). |

### Procedures
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Change management procedures | **MISSING** | No coverage. See change management under Policies above. |
| Onboarding/offboarding | **MISSING** | Not covered. SCIM addresses automated deprovisioning but onboarding/offboarding procedures as governance documents are absent. |
| Playbooks | **MISSING** | SOAR playbooks mentioned in glossary but not playbooks as IR governance procedure documents. |

### External Considerations
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Regulatory | **PARTIAL** | GDPR, HIPAA, PCI DSS, SOX, FISMA listed in glossary. Missing: the concept of regulatory considerations as a governance input. |
| Legal | **MISSING** | No coverage of legal considerations (jurisdiction, liability, e-discovery, legal hold as governance input). Legal hold mentioned only under forensics. |
| Industry | **MISSING** | No coverage of industry-specific standards as governance considerations. |
| Local/regional | **MISSING** | Not addressed. |
| National | **MISSING** | Not addressed as a distinct category. |
| Global | **MISSING** | Not addressed. Import/export controls not covered. |

### Monitoring and Revision
- **MISSING** — No coverage of policy lifecycle, periodic review, revision triggers, or governance monitoring processes.

### Types of Governance Structures
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Boards | **MISSING** | Not covered. |
| Committees | **MISSING** | Not covered. |
| Government entities | **MISSING** | Not covered. |
| Centralized/decentralized | **MISSING** | Not covered. |

### Roles and Responsibilities for Systems and Data
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Owners | **COVERED** | Glossary covers data owner role well ("business executive, decides classification"). |
| Controllers | **COVERED** | Glossary covers data controller (GDPR) with decision rules. |
| Processors | **COVERED** | Glossary covers data processor (GDPR). |
| Custodians/stewards | **COVERED** | Glossary covers both with clear distinctions. |

### 5.1 Summary
- **COVERED**: 4 sub-topics (data roles)
- **PARTIAL**: 6 sub-topics
- **MISSING**: 16 sub-topics
- **Biggest gaps**: Governance structures, external considerations, policy lifecycle, procedures, standards as governance documents

---

## 5.2 — Explain Elements of the Risk Management Process

### Risk Identification
- **MISSING** — No coverage of risk identification methods (brainstorming, interviews, historical data, threat modeling as identification input).

### Risk Assessment
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Ad hoc | **MISSING** | Not covered. |
| Recurring | **MISSING** | Not covered. |
| One-time | **MISSING** | Not covered. |
| Continuous | **MISSING** | Not covered. |

### Risk Analysis
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Qualitative | **COVERED** | Glossary explains qualitative = subjective ratings (high/medium/low), risk matrices, expert judgment. |
| Quantitative | **COVERED** | Glossary covers formulas: SLE = AV x EF, ALE = SLE x ARO, Risk = Likelihood x Impact. |
| SLE (Single Loss Expectancy) | **COVERED** | Defined with formula in glossary. |
| ALE (Annualized Loss Expectancy) | **COVERED** | Defined with formula in glossary. |
| ARO (Annualized Rate of Occurrence) | **COVERED** | Defined in glossary. |
| Probability | **MISSING** | Not explicitly covered as a distinct risk analysis concept. |
| Likelihood | **PARTIAL** | Appears in "Risk = Likelihood x Impact" formula but not explained independently. |
| Exposure Factor | **COVERED** | Defined in glossary ("percentage of asset value lost"). |
| Impact | **PARTIAL** | Appears in risk formula but not elaborated (financial, operational, reputational impact categories). |

### Risk Register, Risk Matrix, Risk Heat Map
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Risk register | **MISSING** | Not covered. No mention of key risk indicators, risk owners, or risk threshold. |
| Risk matrix | **MISSING** | Mentioned only in passing ("risk matrices") under qualitative analysis. Not explained as a tool. |
| Risk heat map | **MISSING** | Not covered. |

### Risk Tolerance / Risk Appetite
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Risk tolerance | **MISSING** | Not covered as a concept. |
| Risk appetite | **MISSING** | Not covered. |
| Expansionary | **MISSING** | Not covered. |
| Conservative | **MISSING** | Not covered. |
| Neutral | **MISSING** | Not covered. |

### Risk Management Strategies
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Transfer | **PARTIAL** | Mentioned in search results context but not explicitly covered in study files. |
| Accept (exemption, exception) | **MISSING** | Not covered. Exemption vs exception distinction absent. |
| Avoid | **MISSING** | Not explicitly covered in study materials. |
| Mitigate | **MISSING** | Not explicitly covered as a named strategy. |

### Risk Reporting
- **MISSING** — Not covered.

### Business Impact Analysis (BIA)
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| BIA concept | **COVERED** | Glossary defines BIA as "identifies critical business functions and impact of disruption. Prerequisite for BCP/DRP." |
| RTO | **COVERED** | Well defined in glossary with decision rules. |
| RPO | **COVERED** | Well defined in glossary with decision rules. |
| MTTR | **COVERED** | Defined in glossary. |
| MTBF | **COVERED** | Defined in glossary with MTTF distinction. |

### 5.2 Summary
- **COVERED**: 10 sub-topics (quantitative formulas, BIA metrics)
- **PARTIAL**: 3 sub-topics
- **MISSING**: 16 sub-topics
- **Biggest gaps**: Risk assessment types (ad hoc/recurring/one-time/continuous), risk register/matrix/heat map, risk appetite/tolerance, risk management strategies (transfer/accept/avoid/mitigate), risk reporting

---

## 5.3 — Third-Party Risk Assessment and Management

### Vendor Assessment
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Penetration testing (of vendors) | **MISSING** | Pen testing covered under 5.5 but not in vendor assessment context. |
| Right-to-audit clause | **MISSING** | Not covered. |
| Evidence of internal audits | **MISSING** | Not covered. |
| Independent assessments | **MISSING** | Not covered. |
| Supply chain analysis | **MISSING** | Not covered. |

### Vendor Monitoring
- **MISSING** — Not covered.

### Vendor Selection (Due Diligence, Conflict of Interest)
- **MISSING** — Not covered.

### Questionnaires
- **MISSING** — Not covered (security questionnaires for vendor risk assessment).

### Rules of Engagement
- **MISSING** — Not covered in vendor context.

### Supply Chain Risks
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Hardware providers | **MISSING** | Not covered. |
| Software providers | **PARTIAL** | SBOM and SCA mentioned in glossary (software supply chain scanning) but not framed as third-party risk. |
| Managed service providers | **PARTIAL** | MSSP defined in glossary but not covered as a supply chain risk. |

### Minimum Security Requirements
- **MISSING** — Not covered.

### Service Level Agreements (SLA)
- **COVERED** — Glossary defines SLA well. Concept walkthrough covers agreement ordering (NDA > MSA > SOW > SLA).

### Agreement Types (supporting 5.3)
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| SLA | **COVERED** | Defined in glossary. |
| MOU | **COVERED** | Covered in glossary and concept walkthrough with decision rules. |
| MSA | **COVERED** | Thoroughly covered in concept walkthrough. |
| SOW | **COVERED** | Covered in concept walkthrough. |
| NDA | **COVERED** | Covered in glossary. |
| BPA | **COVERED** | Covered in glossary and concept walkthrough. |
| BAA | **COVERED** | Covered in glossary (HIPAA context). |

### 5.3 Summary
- **COVERED**: 7 sub-topics (agreement types)
- **PARTIAL**: 2 sub-topics
- **MISSING**: 10 sub-topics
- **Biggest gaps**: Vendor assessment methods (right-to-audit, independent assessments), vendor monitoring, supply chain risk categories, questionnaires, rules of engagement, minimum security requirements

---

## 5.4 — Summarize Elements of Effective Security Compliance

### Compliance Monitoring
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Due diligence/due care | **MISSING** | Not covered. No distinction between due diligence (research before) and due care (ongoing responsibility). |
| Attestation and acknowledgement | **MISSING** | Not covered in compliance monitoring context. |
| Internal monitoring | **MISSING** | Not covered. |
| External monitoring | **MISSING** | Not covered. |
| Automation | **MISSING** | Not covered in compliance context. |

### Privacy
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Legal implications (local/regional/national/global) | **PARTIAL** | GDPR, HIPAA mentioned. Missing: the framework of local vs regional vs national vs global privacy law hierarchy. |
| Data subject | **MISSING** | Not defined. |
| Controller vs processor | **COVERED** | Glossary covers this distinction clearly. |
| Ownership | **COVERED** | Data owner/custodian/steward roles covered. |
| Data inventory and retention | **MISSING** | RoPA mentioned in glossary but data inventory and retention policies not covered as compliance topics. |
| Right to be forgotten | **PARTIAL** | GDPR "right to erasure" mentioned in one line. Not elaborated. |

### Compliance Reporting
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Internal reporting | **MISSING** | Not covered. |
| External reporting | **MISSING** | Not covered. |

### Consequences of Non-Compliance
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Fines | **MISSING** | Not covered. |
| Sanctions | **MISSING** | Not covered. |
| Reputational damage | **MISSING** | Not covered. |
| Loss of license | **MISSING** | Not covered. |
| Contractual impacts | **MISSING** | Not covered. |

### 5.4 Summary
- **COVERED**: 2 sub-topics
- **PARTIAL**: 2 sub-topics
- **MISSING**: 14 sub-topics
- **Biggest gaps**: Compliance monitoring (all aspects), consequences of non-compliance (all aspects), compliance reporting, due diligence/due care, privacy details

---

## 5.5 — Explain Types and Purposes of Audits and Assessments

### Attestation
- **PARTIAL** — SOC Type I/II covered in glossary (point-in-time vs over-period). Missing: attestation as a broader audit concept (formal declaration of compliance).

### Internal Audits
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Compliance | **MISSING** | Internal compliance audits not covered. |
| Audit committee | **MISSING** | Not covered. |
| Self-assessments | **MISSING** | Not covered. |

### External Audits
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Regulatory | **PARTIAL** | Regulatory frameworks listed (GDPR, HIPAA, PCI DSS) but regulatory audits as a process not covered. |
| Examinations | **MISSING** | Not covered. |
| Assessment | **MISSING** | Not covered as a distinct audit type. |
| Independent third-party audit | **PARTIAL** | SOC 2 Type II mentioned. Not framed as "independent third-party audit" concept. |

### Penetration Testing
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Physical | **MISSING** | Physical penetration testing not covered. |
| Offensive | **MISSING** | Not covered. |
| Defensive | **MISSING** | Not covered. |
| Integrated | **MISSING** | Not covered. |
| Known environment | **MISSING** | Not covered. SY0-701 replaced "white box/black box/gray box" with known/partially known/unknown. |
| Partially known environment | **MISSING** | Not covered. |
| Unknown environment | **MISSING** | Not covered. |
| Reconnaissance — passive | **MISSING** | Not covered. |
| Reconnaissance — active | **MISSING** | Not covered. |

### 5.5 Summary
- **COVERED**: 0 sub-topics
- **PARTIAL**: 3 sub-topics
- **MISSING**: 12 sub-topics
- **Biggest gaps**: Entire penetration testing section (all 9 sub-topics), internal audit types, external audit types. This is the weakest objective in the study materials.

---

## 5.6 — Security Awareness Practices

### Phishing
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Campaigns (simulated phishing) | **MISSING** | Not covered. |
| Recognizing a phishing attempt | **MISSING** | Not covered. |
| Responding to reported suspicious messages | **MISSING** | Not covered. |

### Anomalous Behavior Recognition
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Risky behavior | **MISSING** | Not covered. |
| Unexpected behavior | **MISSING** | Not covered. |
| Unintentional behavior | **MISSING** | Not covered. |

### User Guidance and Training
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Policy/handbooks | **MISSING** | Not covered. |
| Situational awareness | **MISSING** | Not covered. |
| Insider threat | **MISSING** | UEBA mentions insider threat detection (technical control) but not insider threat awareness training. |
| Password management | **MISSING** | Not covered as a user training topic. |
| Removable media and cables | **MISSING** | Not covered. |
| Social engineering | **MISSING** | BEC defined in glossary but social engineering awareness training not covered. |
| Operational security | **MISSING** | Not covered. |
| Hybrid/remote work environments | **MISSING** | Not covered. |

### Reporting and Monitoring
- **MISSING** — Security awareness program reporting and monitoring not covered.

### Development and Execution of Security Awareness Programs
- **MISSING** — Not covered.

### 5.6 Summary
- **COVERED**: 0 sub-topics
- **PARTIAL**: 0 sub-topics
- **MISSING**: 14 sub-topics
- **Biggest gap**: This entire objective is absent from the study materials.

---

## Overall Domain 5 Summary

| Objective | Covered | Partial | Missing | Total | Coverage % |
|-----------|---------|---------|---------|-------|-----------|
| 5.1 Security Governance | 4 | 6 | 16 | 26 | 15% |
| 5.2 Risk Management | 10 | 3 | 16 | 29 | 34% |
| 5.3 Third-Party Risk | 7 | 2 | 10 | 19 | 37% |
| 5.4 Security Compliance | 2 | 2 | 14 | 18 | 11% |
| 5.5 Audits and Assessments | 0 | 3 | 12 | 15 | 0% |
| 5.6 Security Awareness | 0 | 0 | 14 | 14 | 0% |
| **TOTAL** | **23** | **16** | **82** | **121** | **19%** |

### Top Priority Gaps (highest exam impact)

1. **5.5 Penetration testing types** — Known/partially known/unknown environments, offensive/defensive/integrated, passive/active recon. Zero coverage. High exam frequency.
2. **5.6 Security awareness practices (entire objective)** — Phishing campaigns, anomalous behavior recognition, user training topics. Zero coverage.
3. **5.2 Risk appetite/tolerance** — Expansionary, conservative, neutral. Common exam topic. Zero coverage.
4. **5.2 Risk register/matrix/heat map** — Key risk indicators, risk owners, risk threshold. Zero coverage.
5. **5.2 Risk management strategies** — Transfer, accept (exemption vs exception), avoid, mitigate. Exam staple. Zero coverage.
6. **5.4 Consequences of non-compliance** — Fines, sanctions, reputational damage, loss of license, contractual impacts. Zero coverage.
7. **5.1 Governance structures** — Boards, committees, centralized/decentralized. Zero coverage.
8. **5.1 Change management** — As both a policy and a procedure. Zero coverage.
9. **5.3 Vendor assessment methods** — Right-to-audit, independent assessments, supply chain analysis. Zero coverage.
10. **5.4 Due diligence vs due care** — Classic exam question pair. Zero coverage.

### What IS Well Covered

- Quantitative risk formulas (SLE, ALE, ARO, EF)
- BIA metrics (RTO, RPO, MTTR, MTBF)
- Data governance roles (owner, custodian, steward, controller, processor)
- Agreement types (SLA, MSA, SOW, MOU, NDA, BPA, BAA)
- Regulatory frameworks at a definitional level (GDPR, HIPAA, PCI DSS, SOX)

### Recommendation

Domain 5 study materials are heavily weighted toward definitions and acronyms but lack the governance, process, and management concepts that the exam actually tests. The materials cover "what things are called" but not "how security programs work." Priority should be given to 5.5 and 5.6 (zero coverage), followed by the process-oriented gaps in 5.1, 5.2, and 5.4.

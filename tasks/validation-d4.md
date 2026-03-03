# Domain 4 Glossary Validation Report

**Date**: 2026-03-03
**Validated against**: CompTIA Security+ SY0-701 Exam Objectives (Version 5.0/6.0)
**Sources used**:
- [Official CompTIA SY0-701 Exam Objectives PDF](https://assets.ctfassets.net/82ripq7fjls2/6TYWUym0Nudqa8nGEnegjG/0f9b974d3b1837fe85ab8e6553f4d623/CompTIA-Security-Plus-SY0-701-Exam-Objectives.pdf)
- [CTO-Help SY0-701 Section 4 Objectives](https://www.cto-help.com/secplus/ExamObjectivesSec4.html)
- [Professor Messer SY0-701 Course](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/sy0-701-comptia-security-plus-course/)
- [Proftia SY0-701 Study Guide](https://proftia.com/resources/securityplus-objectives.html)
- [StudyLib SY0-701 Exam Objectives](https://studylib.net/doc/28061337/security--sy0-701-exam-objectives--5.0-)

---

## Official Domain 4 Objective Structure (Reference)

For clarity, the complete official objective tree is listed here for cross-referencing:

### 4.1 — Given a scenario, apply common security techniques to computing resources
- Secure baselines: Establish, Deploy, Maintain
- Hardening targets: Mobile devices, Workstations, Switches, Routers, Cloud infrastructure, Servers, ICS/SCADA, Embedded systems, RTOS, IoT devices
- Wireless devices — Installation considerations: Site surveys, Heat maps
- Mobile solutions: MDM, Deployment models (BYOD, COPE, CYOD), Connection methods (Cellular, Wi-Fi, Bluetooth)
- Wireless security settings: WPA3, AAA/RADIUS, Cryptographic protocols, Authentication protocols
- Application security: Input validation, Secure cookies, Static code analysis, Code signing
- Sandboxing
- Monitoring

### 4.2 — Explain the security implications of proper hardware, software, and data asset management
- Acquisition/procurement process
- Assignment/accounting: Ownership, Classification
- Monitoring/asset tracking: Inventory, Enumeration
- Disposal/decommissioning: Sanitization, Destruction, Certification, Data retention

### 4.3 — Explain various activities associated with vulnerability management
- Identification methods: Vulnerability scan, Application security (Static analysis, Dynamic analysis, Package monitoring), Threat feed (OSINT, Proprietary/third-party, Information-sharing organization, Dark web), Penetration testing, Responsible disclosure program (Bug bounty program), System/process audit
- Analysis: Confirmation (False positive, False negative), Prioritize, CVSS, CVE, Vulnerability classification, Exposure factor, Environmental variables, Industry/organizational impact, Risk tolerance
- Vulnerability response and remediation: Patching, Insurance, Segmentation, Compensating controls, Exceptions and exemptions
- Validation of remediation: Rescanning, Audit, Verification
- Reporting

### 4.4 — Explain security alerting and monitoring concepts and tools
- Monitoring computing resources: Systems, Applications, Infrastructure
- Activities: Log aggregation, Alerting, Scanning, Reporting, Archiving, Alert response and remediation/validation (Quarantine, Alert tuning)
- Tools: SCAP, Benchmarks, Agents/agentless, SIEM, Antivirus, DLP, SNMP traps, NetFlow, Vulnerability scanners

### 4.5 — Given a scenario, modify enterprise capabilities to enhance security
- Firewall: Rules, Access lists, Ports/protocols, Screened subnets
- IDS/IPS: Trends, Signatures
- Web filter: Agent-based, Centralized proxy, URL scanning, Content categorization, Block rules, Reputation
- Operating system security: Group Policy, SELinux
- Implementation of secure protocols: Protocol selection, Port selection, Transport method
- DNS filtering
- Email security: DMARC, DKIM, SPF, Gateway
- File integrity monitoring
- DLP
- Network access control (NAC)
- Endpoint detection and response (EDR) / Extended detection and response (XDR)
- User behavior analytics

### 4.6 — Given a scenario, implement and maintain identity and access management
- Provisioning/de-provisioning user accounts
- Permission assignments and implications
- Identity proofing
- Federation
- Single sign-on (SSO): LDAP, OAuth, SAML
- Interoperability
- Attestation
- Access controls: Mandatory, Discretionary, Role-based, Rule-based, Attribute-based, Time-of-day restrictions, Least privilege
- Multifactor authentication: Implementations (Biometrics, Hard/soft authentication tokens, Security keys), Factors (Something you know, Something you have, Something you are, Somewhere you are)
- Password concepts: Password best practices (Length, Complexity, Reuse, Expiration, Age), Password managers, Passwordless
- Privileged access management tools: Just-in-time permissions, Password vaulting, Ephemeral credentials

### 4.7 — Explain the importance of automation and orchestration related to secure operations
- Use cases: User provisioning, Resource provisioning, Guard rails, Security groups, Ticket creation, Escalation, Enabling/disabling services and access, Continuous integration and testing, Integrations and APIs
- Benefits: Efficiency/time saving, Enforcing baselines, Standard infrastructure configurations, Scaling in a secure manner, Employee retention, Reaction time, Workforce multiplier
- Other considerations: Complexity, Cost, Single point of failure, Technical debt, Ongoing supportability

### 4.8 — Explain appropriate incident response activities
- Process: Preparation, Detection, Analysis, Containment, Eradication, Recovery, Lessons learned
- Training
- Testing: Tabletop exercise, Simulation
- Root cause analysis
- Threat hunting
- Digital forensics: Legal hold, Chain of custody, Acquisition, Reporting, Preservation, E-discovery

### 4.9 — Given a scenario, use data sources to support an investigation
- Log data: Firewall logs, Application logs, Endpoint logs, OS-specific security logs, IPS/IDS logs, Network logs, Metadata
- Data sources: Vulnerability scans, Automated reports, Dashboards, Packet captures

---

## Section-by-Section Validation

### Section 32: Email Security

| Item | Status | Notes |
|---|---|---|
| SPF (Sender Policy Framework) | **VALID** | Explicitly listed under 4.5 — Email security |
| DKIM (DomainKeys Identified Mail) | **VALID** | Explicitly listed under 4.5 — Email security |
| DMARC (Domain-based Message Authentication, Reporting, and Conformance) | **VALID** | Explicitly listed under 4.5 — Email security |
| Email gateway (Secure Email Gateway) | **VALID** | Explicitly listed under 4.5 — Email security as "Gateway" |
| SPF vs DKIM vs DMARC decision rules | **VALID** | Useful exam-day differentiation for the 4.5 objective |

**Verdict**: All items map directly to **Objective 4.5** (Email security sub-bullets). Fully valid.

---

### Section 33: Asset Management

| Item | Status | Notes |
|---|---|---|
| Acquisition/procurement | **VALID** | Explicitly listed under 4.2 |
| Asset tagging | **INFERRED** | Not explicitly named in objectives, but clearly implied by "Monitoring/asset tracking — Inventory." Tagging is the mechanism for tracking. |
| CMDB (Configuration Management Database) | **INFERRED** | Not explicitly listed. However, it is directly implied by "Monitoring/asset tracking — Inventory, Enumeration." CMDB is the standard tool for this. Reasonable inclusion but candidates should note the term itself may not appear on the exam. |
| Lifecycle tracking (Asset Lifecycle Management) | **INFERRED** | Not a named sub-bullet, but the 4.2 objective structure (acquisition → assignment → monitoring → disposal) IS the lifecycle. Reasonable conceptual inclusion. |
| Data sanitization | **VALID** | Maps to 4.2 — Disposal/decommissioning — Sanitization |
| Overwrite/wipe | **VALID** | Standard method under Sanitization. Professor Messer and all major study guides cover this under 4.2. |
| Degaussing | **VALID** | Standard method under Sanitization/Destruction. Covered by all major study sources under 4.2. |
| Cryptographic erase | **VALID** | Standard method under Sanitization. Covered by all major study sources under 4.2. |
| Physical destruction | **VALID** | Maps to 4.2 — Disposal/decommissioning — Destruction |
| Certificate of destruction | **VALID** | Maps to 4.2 — Disposal/decommissioning — Certification |
| Data retention policy | **VALID** | Explicitly listed under 4.2 — Data retention |
| Legal hold | **VALID** | Explicitly listed under 4.8 — Digital forensics — Legal hold. Also relevant to 4.2 data retention context. |
| Sanitization method decision rules | **VALID** | Directly supports the 4.2 scenario-adjacent knowledge |

**Verdict**: Core items map to **Objective 4.2**. Asset tagging, CMDB, and lifecycle tracking are inferred but reasonable. No questionable items.

---

### Section 34: Common Ports and Secure Protocols

| Item | Status | Notes |
|---|---|---|
| FTP/SFTP/FTPS and ports | **VALID** | Maps to 4.5 — Implementation of secure protocols (Protocol selection, Port selection) |
| SSH (port 22) | **VALID** | 4.5 — secure protocol replacement |
| Telnet → SSH | **VALID** | 4.5 — Protocol selection |
| SMTP/SMTPS (25/587) | **VALID** | 4.5 — Email security + secure protocols |
| DNS/DoT/DoH (53/853/443) | **VALID** | 4.5 — DNS filtering + secure protocols |
| HTTP/HTTPS (80/443) | **VALID** | 4.5 — Protocol selection |
| POP3/POP3S (110/995) | **VALID** | 4.5 — secure protocols |
| IMAP/IMAPS (143/993) | **VALID** | 4.5 — secure protocols |
| SNMP/SNMPv3 (161/162) | **VALID** | 4.4 — SNMP traps; 4.5 — secure protocols |
| LDAP/LDAPS (389/636) | **VALID** | 4.6 — SSO/LDAP; 4.5 — secure protocols |
| RDP (3389) | **VALID** | 4.5 — Port selection, transport method |
| Syslog/Syslog over TLS (514/6514) | **VALID** | 4.9 — log data; 4.5 — secure protocols |
| Kerberos (88) | **VALID** | 4.6 — authentication protocol |
| RADIUS (1812/1813) | **VALID** | 4.1 — AAA/RADIUS; 4.6 — authentication |
| TACACS+ (49) | **VALID** | Standard AAA protocol tested alongside RADIUS |
| NetBIOS (137-139) | **QUESTIONABLE** | Not explicitly listed in any SY0-701 objective. Legacy protocol knowledge. Low likelihood of appearing on the exam but not harmful to know. |
| SMB (445) | **QUESTIONABLE** | Not explicitly listed in objectives. Common knowledge but not a named sub-bullet. |
| SQL Server (1433) | **QUESTIONABLE** | Not explicitly listed. General port knowledge but not in the objectives. |
| MySQL (3306) | **QUESTIONABLE** | Not explicitly listed. General port knowledge but not in the objectives. |

**Verdict**: Majority maps to **Objectives 4.5 and 4.6**. NetBIOS, SMB, SQL Server, and MySQL ports are general networking knowledge not explicitly in SY0-701 objectives. They are unlikely to be tested directly, though they are not wrong to include as supplementary reference. The glossary should note these are supplementary.

---

### Section 35: Mobile Device Management

| Item | Status | Notes |
|---|---|---|
| MDM (Mobile Device Management) | **VALID** | Explicitly listed under 4.1 — Mobile solutions |
| Remote wipe | **INFERRED** | Not explicitly named as a sub-bullet, but universally covered as a core MDM capability under 4.1. All study guides include it. High exam probability. |
| Geofencing | **INFERRED** | Not explicitly named as a sub-bullet, but a standard MDM feature covered by all study guides under 4.1. |
| Containerization (mobile) | **INFERRED** | Not explicitly named as a sub-bullet, but a standard MDM feature covered by all study guides under 4.1. |
| BYOD | **VALID** | Explicitly listed under 4.1 — Deployment models |
| COPE | **VALID** | Explicitly listed under 4.1 — Deployment models |
| CYOD | **VALID** | Explicitly listed under 4.1 — Deployment models |
| Corporate-owned | **INFERRED** | Not explicitly listed as a named option (only BYOD, COPE, CYOD are listed), but implied as the default alternative. |
| Cellular connection | **VALID** | Explicitly listed under 4.1 — Connection methods |
| Wi-Fi connection | **VALID** | Explicitly listed under 4.1 — Connection methods |
| Bluetooth connection | **VALID** | Explicitly listed under 4.1 — Connection methods |
| MDM capabilities table (screen lock, encryption, app management, camera disable) | **INFERRED** | These are standard MDM enforcement capabilities implied by 4.1 but not individually listed. Study guides universally cover them. |
| Bluejacking, bluesnarfing, bluesniffing | **QUESTIONABLE** | These Bluetooth attack terms are NOT listed under Domain 4 objectives. They may appear under Domain 2 (Threats/Vulnerabilities) but are not Domain 4 scope. Their inclusion in a Domain 4 glossary is misplaced — they belong in Domain 2 if anywhere. |
| SS7 vulnerabilities | **QUESTIONABLE** | Not listed in any SY0-701 objective. Too granular for Security+ exam scope. |

**Verdict**: Core MDM items map to **Objective 4.1**. Remote wipe, geofencing, containerization, and MDM capabilities are well-established inferred topics. Bluetooth attacks (bluejacking/bluesnarfing/bluesniffing) and SS7 are out of scope for Domain 4 — these are threat/attack topics (Domain 2) and may be too detailed for SY0-701 in general.

---

### Section 36: Automation and Orchestration

| Item | Status | Notes |
|---|---|---|
| Automation (Security Automation) | **VALID** | Core concept of 4.7 |
| Orchestration (Security Orchestration) | **VALID** | Core concept of 4.7 |
| Guard rails | **VALID** | Explicitly listed under 4.7 — Use cases |
| Runbook | **INFERRED** | Not explicitly listed in 4.7 sub-bullets, but commonly tested concept in automation/orchestration context. Study guides cover it. |
| Playbook (Security Playbook) | **INFERRED** | Not explicitly listed in 4.7 sub-bullets, but universally covered as a SOAR component. Very likely to be tested. |
| User provisioning/deprovisioning | **VALID** | Explicitly listed under 4.7 — Use cases |
| Resource provisioning | **VALID** | Explicitly listed under 4.7 — Use cases |
| Security group management | **VALID** | Explicitly listed under 4.7 — Use cases (Security groups) |
| Ticket creation | **VALID** | Explicitly listed under 4.7 — Use cases |
| Escalation | **VALID** | Explicitly listed under 4.7 — Use cases |
| Enabling/disabling services and access | **VALID** | Explicitly listed under 4.7 — Use cases |
| CI/CD security testing | **VALID** | Explicitly listed under 4.7 — Use cases (Continuous integration and testing) |
| API integrations | **VALID** | Explicitly listed under 4.7 — Use cases (Integrations and APIs) |
| Efficiency/time saving | **VALID** | Explicitly listed under 4.7 — Benefits |
| Enforcing baselines | **VALID** | Explicitly listed under 4.7 — Benefits |
| Standard infrastructure configs | **VALID** | Explicitly listed under 4.7 — Benefits |
| Scaling securely | **VALID** | Explicitly listed under 4.7 — Benefits |
| Reaction time | **VALID** | Explicitly listed under 4.7 — Benefits |
| Workforce multiplier | **VALID** | Explicitly listed under 4.7 — Benefits |
| Employee retention | **VALID** | Explicitly listed under 4.7 — Benefits |
| SOAR definition | **VALID** | SOAR is covered under 4.4 (Tools) and is the platform that implements 4.7 concepts |

**Verdict**: Excellent coverage. Nearly all items map directly to **Objective 4.7** sub-bullets. Runbook and playbook are inferred but highly exam-relevant.

**MISSING from this section**: The official objectives list "Other considerations" under 4.7: **Complexity, Cost, Single point of failure, Technical debt, Ongoing supportability**. These are NOT covered in the glossary content and SHOULD be.

---

### Section 37: Investigation Data Sources

| Item | Status | Notes |
|---|---|---|
| Firewall logs | **VALID** | Explicitly listed under 4.9 — Log data |
| Application logs | **VALID** | Explicitly listed under 4.9 — Log data |
| Endpoint logs | **VALID** | Explicitly listed under 4.9 — Log data |
| Windows Event Log (+ event IDs) | **VALID** | Maps to 4.9 — OS-specific security logs. Event ID detail is study-aid depth, appropriate for exam prep. |
| Syslog | **VALID** | Standard log transport, maps to 4.9 — Log data |
| journald | **INFERRED** | Not explicitly listed but falls under OS-specific security logs (Linux). Reasonable inclusion. |
| IPS/IDS logs | **VALID** | Explicitly listed under 4.9 — Log data |
| Network logs | **VALID** | Explicitly listed under 4.9 — Log data |
| pcap (Packet Capture) | **VALID** | Maps to 4.9 — Data sources — Packet captures |
| NetFlow | **VALID** | Explicitly listed under 4.4 — Tools. Also relevant to 4.9 as a network log/data source. |
| sFlow | **INFERRED** | Not explicitly listed but is a NetFlow variant. Reasonable inclusion as supplementary. |
| IPFIX | **INFERRED** | Not explicitly listed but is the IETF standard version of NetFlow. Reasonable inclusion as supplementary. |
| SNMP traps | **VALID** | Explicitly listed under 4.4 — Tools |
| Email headers | **INFERRED** | Not explicitly listed under 4.9 but falls under Metadata. Reasonable for email investigation context. |
| File metadata | **VALID** | Maps to 4.9 — Log data — Metadata |
| Vulnerability scan results | **VALID** | Explicitly listed under 4.9 — Data sources — Vulnerability scans |
| Dashboard | **VALID** | Explicitly listed under 4.9 — Data sources — Dashboards |
| Automated reports | **VALID** | Explicitly listed under 4.9 — Data sources — Automated reports |

**Verdict**: Excellent coverage of **Objective 4.9**. journald, sFlow, IPFIX, and email headers are inferred but reasonable supplementary material.

---

### Section 38: Web Filtering

| Item | Status | Notes |
|---|---|---|
| Agent-based filtering | **VALID** | Explicitly listed under 4.5 — Web filter — Agent-based |
| Centralized proxy | **VALID** | Explicitly listed under 4.5 — Web filter — Centralized proxy |
| URL scanning | **VALID** | Explicitly listed under 4.5 — Web filter — URL scanning |
| Content categorization | **VALID** | Explicitly listed under 4.5 — Web filter — Content categorization |
| Block rules | **VALID** | Explicitly listed under 4.5 — Web filter — Block rules |
| Reputation-based filtering | **VALID** | Explicitly listed under 4.5 — Web filter — Reputation |
| DNS filtering | **VALID** | Explicitly listed under 4.5 as a standalone sub-bullet |
| SWG (Secure Web Gateway) mention | **INFERRED** | Not explicitly listed in objectives but is the product category encompassing these features. Brief mention is appropriate context. |

**Verdict**: Perfect match to **Objective 4.5** Web filter sub-bullets. Every named sub-bullet is covered. SWG mention is appropriate context.

---

### Section 39: Vulnerability Management Expanded

| Item | Status | Notes |
|---|---|---|
| Known-environment pen test (white box) | **VALID** | Maps to 4.3 — Penetration testing |
| Partially known environment (gray box) | **VALID** | Maps to 4.3 — Penetration testing |
| Unknown-environment pen test (black box) | **VALID** | Maps to 4.3 — Penetration testing |
| Bug bounty program | **VALID** | Explicitly listed under 4.3 — Responsible disclosure program — Bug bounty program |
| True positive | **VALID** | Maps to 4.3 — Analysis — Confirmation |
| False positive | **VALID** | Explicitly listed under 4.3 — Analysis — Confirmation — False positive |
| True negative | **INFERRED** | Not explicitly listed but is the logical complement to false positive/negative. Expected exam knowledge. |
| False negative | **VALID** | Explicitly listed under 4.3 — Analysis — Confirmation — False negative |
| Compensating control | **VALID** | Explicitly listed under 4.3 — Vulnerability response and remediation — Compensating controls |
| Exception | **VALID** | Explicitly listed under 4.3 — Exceptions and exemptions |
| Exemption | **VALID** | Explicitly listed under 4.3 — Exceptions and exemptions |
| Cyber insurance | **VALID** | Explicitly listed under 4.3 — Insurance |
| Rescanning | **VALID** | Explicitly listed under 4.3 — Validation of remediation — Rescanning |
| SY0-701 terminology note (known/partially known/unknown) | **VALID** | Important exam-day guidance |

**Verdict**: Excellent match to **Objective 4.3**. All items are either explicitly listed or closely inferred.

**MISSING from this section**: Several 4.3 items are NOT covered:
- **CVSS (Common Vulnerability Scoring System)** — explicitly listed, not in this glossary section
- **CVE (Common Vulnerabilities and Exposures)** — explicitly listed, not covered
- **Vulnerability classification** — explicitly listed, not covered
- **Exposure factor** — explicitly listed, not covered
- **Environmental variables** — explicitly listed, not covered
- **Industry/organizational impact** — explicitly listed, not covered
- **Risk tolerance** — explicitly listed, not covered
- **Segmentation** (as a remediation strategy) — explicitly listed, not covered in this section
- **Package monitoring** — explicitly listed under Application security, not covered
- **Threat feeds (OSINT, Proprietary/third-party, Information-sharing organization, Dark web)** — explicitly listed, not covered
- **System/process audit** — explicitly listed, not covered
- **Static analysis / Dynamic analysis** — explicitly listed under Application security, not covered in this section (though may be in other glossary sections)

NOTE: Some of these (CVSS, CVE, OSINT, static/dynamic analysis) may be covered in other glossary sections not under review here. The gap analysis should verify.

---

### Section 40: Incident Response Expanded

| Item | Status | Notes |
|---|---|---|
| Tabletop exercise | **VALID** | Explicitly listed under 4.8 — Testing |
| Simulation | **VALID** | Explicitly listed under 4.8 — Testing |
| Root cause analysis (RCA) | **VALID** | Explicitly listed under 4.8 |
| Internal reporting | **INFERRED** | Not explicitly listed as a sub-bullet, but "Reporting" is listed under 4.8 — Digital forensics. Internal vs. external distinction is standard study material. |
| External reporting | **INFERRED** | Same as above — implied by "Reporting" under 4.8. |
| Breach notification | **INFERRED** | Not explicitly listed in 4.8 sub-bullets. May be more relevant to Domain 5 (Security Program Management — compliance/legal). Including it here as context is acceptable but candidates should know it's not a named 4.8 item. |
| Stakeholder management | **INFERRED** | Not explicitly listed. General IR best practice. Reasonable supplementary content. |
| External reporting triggers table | **INFERRED** | Useful study content but goes beyond what's explicitly in the objectives. Not harmful. |

**Verdict**: Core items match **Objective 4.8**. Reporting breakdown (internal/external) and breach notification are inferred but standard study material. Stakeholder management is supplementary.

**MISSING from this section**: Several 4.8 items are NOT covered:
- **Preparation** (IR process phase) — explicitly listed, not in this section
- **Detection** — explicitly listed, not in this section
- **Analysis** — explicitly listed, not in this section
- **Containment** — explicitly listed, not in this section
- **Eradication** — explicitly listed, not in this section
- **Recovery** — explicitly listed, not in this section
- **Lessons learned** — explicitly listed, not in this section
- **Training** — explicitly listed, not in this section
- **Threat hunting** — explicitly listed, not in this section
- **Digital forensics sub-items**: Legal hold, Chain of custody, Acquisition, Preservation, E-discovery — explicitly listed, not in this section (Legal hold appears in section 33)

NOTE: These may be covered in the existing glossary (before these new additions). The gap analysis should confirm.

---

### Section 41: Monitoring Activities Expanded

| Item | Status | Notes |
|---|---|---|
| Alert tuning | **VALID** | Explicitly listed under 4.4 — Alert response and remediation/validation — Alert tuning |
| Quarantine | **VALID** | Explicitly listed under 4.4 — Alert response and remediation/validation — Quarantine |
| Archiving | **VALID** | Explicitly listed under 4.4 — Activities — Archiving |
| Signature-based AV | **VALID** | Maps to 4.4 — Tools — Antivirus |
| Heuristic AV | **VALID** | Maps to 4.4 — Tools — Antivirus (detection method detail) |
| Behavioral AV | **VALID** | Maps to 4.4 — Tools — Antivirus (detection method detail) |
| Scheduled reports | **INFERRED** | Not explicitly listed but falls under 4.4 — Activities — Reporting. Reasonable detail. |
| Ad-hoc reports | **INFERRED** | Same — implied by Reporting activity. |
| Compliance reporting | **INFERRED** | Same — implied by Reporting activity. May also relate to Domain 5. |

**Verdict**: Good coverage of **Objective 4.4** activities and tools. AV detection methods are appropriate depth for the Antivirus tool sub-bullet.

**MISSING from this section**: Several 4.4 items are NOT covered in this glossary section:
- **SCAP (Security Content Automation Protocol)** — explicitly listed under Tools
- **Benchmarks** — explicitly listed under Tools
- **Agents/agentless** (monitoring approaches) — explicitly listed under Tools
- **SIEM** — explicitly listed under Tools (may be in existing glossary)
- **DLP** — explicitly listed under Tools (may be in existing glossary)
- **Log aggregation** — explicitly listed under Activities
- **Alerting** — explicitly listed under Activities
- **Scanning** — explicitly listed under Activities
- **Monitoring computing resources: Systems, Applications, Infrastructure** — explicitly listed

NOTE: Some of these (SIEM, DLP) may be covered in other glossary sections.

---

## Summary: Items MISSING FROM CONTENT but in Official Objectives

These items are explicitly listed in the official SY0-701 Domain 4 objectives and were NOT found in the new glossary content (sections 32-41). They may exist in other glossary sections not under review.

### Critical Gaps (high exam weight, not covered anywhere in sections 32-41)

| Objective | Missing Item | Priority |
|---|---|---|
| **4.1** | Secure baselines (Establish, Deploy, Maintain) | HIGH — entire sub-section missing |
| **4.1** | Hardening targets (Mobile devices, Workstations, Switches, Routers, Cloud infrastructure, Servers, ICS/SCADA, Embedded systems, RTOS, IoT devices) | HIGH — entire sub-section missing |
| **4.1** | Wireless security settings (WPA3, AAA/RADIUS, Cryptographic protocols, Authentication protocols) | HIGH |
| **4.1** | Application security (Input validation, Secure cookies, Static code analysis, Code signing) | HIGH |
| **4.1** | Sandboxing | HIGH |
| **4.1** | Site surveys, Heat maps | MEDIUM |
| **4.3** | CVSS, CVE, Vulnerability classification | HIGH |
| **4.3** | Exposure factor, Environmental variables, Industry/organizational impact, Risk tolerance | MEDIUM |
| **4.3** | Package monitoring | MEDIUM |
| **4.3** | Threat feeds (OSINT, Proprietary/third-party, Information-sharing organization, Dark web) | HIGH |
| **4.3** | System/process audit | MEDIUM |
| **4.4** | SCAP (Security Content Automation Protocol) | HIGH |
| **4.4** | Benchmarks | HIGH |
| **4.4** | Agents/agentless monitoring | MEDIUM |
| **4.4** | Log aggregation | MEDIUM |
| **4.5** | Firewall (Rules, Access lists, Ports/protocols, Screened subnets) | HIGH — entire sub-section missing |
| **4.5** | IDS/IPS (Trends, Signatures) | HIGH |
| **4.5** | Operating system security (Group Policy, SELinux) | HIGH |
| **4.5** | File integrity monitoring | MEDIUM |
| **4.5** | NAC (Network access control) | MEDIUM |
| **4.5** | EDR/XDR | HIGH |
| **4.5** | User behavior analytics | MEDIUM |
| **4.6** | ALL of objective 4.6 (IAM) | **CRITICAL** — entire objective not in new sections |
| **4.7** | Other considerations (Complexity, Cost, Single point of failure, Technical debt, Ongoing supportability) | HIGH |
| **4.8** | IR process phases (Preparation, Detection, Analysis, Containment, Eradication, Recovery, Lessons learned) | HIGH (may be in existing glossary) |
| **4.8** | Threat hunting | HIGH |
| **4.8** | Digital forensics (Chain of custody, Acquisition, Preservation, E-discovery) | HIGH (may be in existing glossary) |

### Important Note

This glossary file is titled "Glossary **Additions** — New Sections 32-41" and states it covers "gaps identified in the Domain 4 gap analysis." This means the items listed as "MISSING" above are expected to already exist in the base glossary (sections 1-17 or elsewhere). **These missing items are only a true gap if they are also absent from the existing glossary.** The gap analysis file (`gap-analysis-d4.md`) should be consulted to determine which items were intentionally left to the existing content vs. which are genuine omissions.

---

## Questionable Items Summary

Items included in the glossary that may be out of scope or too detailed for the exam:

| Section | Item | Concern |
|---|---|---|
| 34 | NetBIOS (137-139) | Not in any SY0-701 objective |
| 34 | SMB (445) | Not in any SY0-701 objective |
| 34 | SQL Server (1433) | Not in any SY0-701 objective |
| 34 | MySQL (3306) | Not in any SY0-701 objective |
| 35 | Bluejacking, bluesnarfing, bluesniffing | Domain 2 topic (threats), not Domain 4 |
| 35 | SS7 vulnerabilities | Not in any SY0-701 objective; too granular |
| 40 | Breach notification with specific timelines (GDPR 72h, HIPAA 60d) | More Domain 5 (compliance/governance) than Domain 4 |
| 40 | External reporting triggers table (SEC, CISA specifics) | More Domain 5 scope |

These items are not wrong to know but should be deprioritized vs. items that are explicitly in the objectives.

---

## Overall Assessment

**Quality**: The new glossary sections are well-structured with clear definitions, decision rules, and exam-day differentiation tables. The format is excellent for rapid review.

**Accuracy**: All definitions and explanations checked are factually correct. No errors found in the technical content.

**Scope alignment**: The sections cover their targeted objectives well, but this is a supplementary addition (sections 32-41), not a comprehensive Domain 4 glossary. Many Domain 4 objectives are presumably covered in the existing base glossary. The few questionable items (NetBIOS, SMB, SQL/MySQL ports, Bluetooth attacks, SS7) should be marked as supplementary or moved to appropriate domains.

**Recommendation**: Cross-reference the "Critical Gaps" table above against the existing glossary to confirm full Domain 4 coverage. Add the missing 4.7 "Other considerations" items (Complexity, Cost, Single point of failure, Technical debt, Ongoing supportability) as these appear to be a genuine gap even accounting for existing content.

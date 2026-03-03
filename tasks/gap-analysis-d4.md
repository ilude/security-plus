# Domain 4: Security Operations — Gap Analysis

Coverage assessment of study materials (`glossary.md`, `concept-walkthrough.md`, `notes.md`) against official SY0-701 Domain 4 exam objectives.

**Legend:**
- **COVERED** — Topic appears in study materials with sufficient depth
- **PARTIAL** — Some aspects covered but key details missing
- **MISSING** — Not covered at all

---

## 4.1 Apply Common Security Techniques to Computing Resources

### Secure Baselines
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Establish secure baselines | **MISSING** | No mention of creating/documenting baseline configurations |
| Deploy secure baselines | **MISSING** | No coverage of baseline deployment processes |
| Maintain secure baselines | **MISSING** | No coverage of baseline drift detection or re-baselining |

### Hardening Targets
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Mobile devices | **MISSING** | No hardening guidance for mobile devices |
| Workstations | **MISSING** | No workstation hardening content |
| Switches | **MISSING** | No switch hardening (port security, disabling unused ports, DHCP snooping) |
| Routers | **MISSING** | No router hardening content |
| Cloud infrastructure | **PARTIAL** | CSPM concept covered in glossary/walkthrough (misconfiguration detection), but no hardening steps |
| Servers | **MISSING** | No server hardening content (disabling services, least functionality) |
| ICS/SCADA | **COVERED** | Glossary covers ICS/SCADA/DCS/PLC; walkthrough covers protection strategies (NIDS, segmentation, air gap) |
| Embedded systems | **MISSING** | No coverage of embedded system hardening constraints |
| RTOS (Real-Time Operating System) | **PARTIAL** | RTOS defined in glossary, mentioned in ICS walkthrough as hard to patch, but no hardening specifics |
| IoT devices | **PARTIAL** | IoT defined in glossary ("large attack surface, often unpatched") but no hardening techniques |

### Wireless Security
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| WPA3 (Wi-Fi Protected Access 3) | **COVERED** | Glossary covers WPA3 and SAE (Simultaneous Authentication of Equals) |
| AAA (Authentication, Authorization, Accounting) / RADIUS (Remote Authentication Dial-In User Service) | **COVERED** | Glossary covers AAA, RADIUS, TACACS+ with decision rules |
| Cryptographic protocols | **PARTIAL** | EAP-TLS and PEAP covered; missing WPA3-Enterprise, WPA3-SAE details for personal vs enterprise modes |
| Authentication protocols | **COVERED** | EAP-TLS, PEAP, RADIUS decision rules present |

### Mobile Solutions
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| MDM (Mobile Device Management) | **MISSING** | No coverage of MDM capabilities (remote wipe, geofencing, containerization, app management) |
| BYOD (Bring Your Own Device) | **MISSING** | No coverage of deployment models |
| COPE (Corporate-Owned, Personally Enabled) | **MISSING** | Not mentioned |
| CYOD (Choose Your Own Device) | **MISSING** | Not mentioned |
| Connection methods — cellular/Wi-Fi/Bluetooth | **MISSING** | No coverage of mobile connection security implications |

### Application Security
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Input validation | **PARTIAL** | SQLi and XSS covered in glossary (implying input validation as mitigation) but input validation not explicitly taught as a technique |
| Secure cookies | **MISSING** | No coverage of cookie security attributes (HttpOnly, Secure, SameSite) |
| Static code analysis (SAST) | **COVERED** | Glossary covers SAST with decision rules |
| Dynamic code analysis (DAST) | **COVERED** | Glossary covers DAST with decision rules |
| Code signing | **MISSING** | No coverage of code signing concepts |
| Sandboxing | **MISSING** | No coverage of application sandboxing |

### Asset Management
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| General asset management | **MISSING** | No asset management content in 4.1 context (see 4.2 for more) |

---

## 4.2 Security Implications of Asset Management

| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Acquisition/procurement | **MISSING** | No coverage of secure procurement processes, supply chain verification |
| Assignment/accounting | **MISSING** | No coverage of asset assignment tracking, ownership records |
| Monitoring/asset tracking | **MISSING** | No coverage of asset inventory tools, tracking lifecycle |
| Disposal/decommissioning | **MISSING** | No coverage |
| Sanitization methods (overwrite, degauss, crypto erase) | **MISSING** | Not mentioned anywhere |
| Physical destruction | **MISSING** | Not mentioned |
| Certification of destruction | **MISSING** | Not mentioned |
| Data retention policies | **MISSING** | Not mentioned in study materials |

**Overall 4.2 assessment: Entirely MISSING.** This is a significant gap — asset management lifecycle is testable and has no representation in current materials.

---

## 4.3 Vulnerability Management

### Identification Methods
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Vulnerability scanning | **PARTIAL** | SCAP, CVE, CVSS covered in glossary/walkthrough. Missing: credentialed vs non-credentialed scans, intrusive vs non-intrusive, scan frequency |
| Application security testing | **COVERED** | SAST, DAST, IAST, SCA all covered with decision rules |
| Threat feeds / open source intelligence (OSINT) | **PARTIAL** | STIX/TAXII covered for threat intel sharing. OSINT not explicitly covered as an identification method |
| Penetration testing — known environment | **MISSING** | No coverage (formerly "white box") |
| Penetration testing — partially known environment | **MISSING** | No coverage (formerly "gray box") |
| Penetration testing — unknown environment | **MISSING** | No coverage (formerly "black box") |
| Bug bounties | **MISSING** | Not mentioned |

### Analysis
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Confirmation (true/false positive) | **MISSING** | No coverage of validating scan results |
| Prioritizing vulnerabilities | **PARTIAL** | CVSS scoring covered but prioritization workflow not taught |
| CVSS (Common Vulnerability Scoring System) | **COVERED** | Defined in glossary with decision rules |
| CVE (Common Vulnerabilities and Exposures) | **COVERED** | Defined in glossary with decision rules |
| Vulnerability classification | **MISSING** | No coverage of classification categories |
| Exposure factor | **COVERED** | Defined in glossary under GRC section with formula (SLE = AV x EF) |
| Environmental variables | **MISSING** | No coverage of environmental CVSS scoring adjustments |
| Industry/organizational impact | **MISSING** | Not addressed |
| Risk tolerance | **MISSING** | Not explicitly covered as a vuln management consideration |

### Vulnerability Response and Remediation
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Patching | **MISSING** | No patch management process coverage |
| Insurance (cyber insurance) | **MISSING** | Not mentioned |
| Segmentation | **PARTIAL** | VLAN/network segmentation defined in glossary but not linked to vuln remediation |
| Compensating controls | **MISSING** | Concept not explicitly covered |
| Exceptions and exemptions | **MISSING** | No coverage of risk acceptance processes |

### Validation of Remediation
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Rescanning | **MISSING** | Not covered |
| Audit | **MISSING** | Not covered in vuln context |
| Verification | **MISSING** | Not covered |

---

## 4.4 Security Alerting and Monitoring

### Monitoring Computing Resources
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Systems monitoring | **PARTIAL** | EDR/HIDS mentioned but no systematic monitoring coverage |
| Applications monitoring | **MISSING** | No application-level monitoring content |
| Infrastructure monitoring | **PARTIAL** | IDS/IPS/NIDS covered for network monitoring |

### Activities
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Log aggregation | **COVERED** | SIEM defined as log aggregation/correlation tool |
| Alerting | **PARTIAL** | SIEM alerting mentioned; no coverage of alert thresholds, severity levels |
| Scanning | **PARTIAL** | Vulnerability scanning touched on; no continuous scanning coverage |
| Reporting | **MISSING** | No coverage of security reporting practices |
| Archiving | **MISSING** | No log archiving/retention coverage |
| Alert response and remediation/validation | **MISSING** | No alert response workflow |
| Quarantine | **MISSING** | No coverage of quarantine as a monitoring response |
| Alert tuning | **MISSING** | No coverage of tuning alerts to reduce false positives |

### Tools
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| SIEM (Security Information and Event Management) | **COVERED** | Well-covered in glossary with decision rules |
| SCAP (Security Content Automation Protocol) | **COVERED** | Covered in glossary and walkthrough |
| Antivirus | **MISSING** | Not covered as a standalone monitoring tool |
| DLP (Data Loss Prevention) | **COVERED** | Covered in glossary with network/endpoint/cloud variants |
| SNMP (Simple Network Management Protocol) traps | **MISSING** | Not mentioned anywhere |
| NetFlow | **MISSING** | Not covered (network traffic metadata analysis) |
| Vulnerability scanners | **PARTIAL** | SCAP framework covered but no specific scanner tool discussion |

---

## 4.5 Modify Enterprise Capabilities to Enhance Security

### Firewalls
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Rules | **PARTIAL** | Firewall defined in glossary decision rules but no rule configuration details |
| ACLs (Access Control Lists) | **PARTIAL** | ACL defined in glossary but not in firewall context |
| Ports and protocols | **MISSING** | No coverage of common ports or protocol filtering |
| Screened subnets (DMZ) | **COVERED** | DMZ/screened subnet covered in glossary with SY0-701 terminology note |

### IDS/IPS
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Trends | **MISSING** | No coverage of trend analysis in IDS/IPS |
| Signatures | **PARTIAL** | IPS described as using "signatures + anomaly detection" but no depth |

### Web Filter
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Agent-based | **MISSING** | Not covered |
| Centralized proxy | **MISSING** | Not covered (SWG is mentioned but not as web filtering proxy) |
| URL scanning | **MISSING** | Not covered |
| Content categorization | **MISSING** | Not covered |
| Block rules | **MISSING** | Not covered |
| Reputation | **MISSING** | Not covered |

### Operating System Security
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Group Policy | **MISSING** | Not mentioned |
| SELinux | **PARTIAL** | SELinux mentioned in glossary under MAC (Mandatory Access Control) but not as OS hardening |
| Updates/patches | **MISSING** | No OS patching process coverage |

### Other 4.5 Topics
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Secure protocols implementation | **MISSING** | No coverage of replacing insecure protocols (Telnet→SSH, HTTP→HTTPS, FTP→SFTP) |
| DNS filtering | **MISSING** | Not covered |
| Email security — DMARC (Domain-based Message Authentication, Reporting and Conformance) | **MISSING** | Not mentioned |
| Email security — DKIM (DomainKeys Identified Mail) | **MISSING** | Not mentioned |
| Email security — SPF (Sender Policy Framework) | **MISSING** | Not mentioned |
| Email gateways | **MISSING** | Not covered |
| FIM (File Integrity Monitoring) | **COVERED** | Defined in glossary |
| DLP (Data Loss Prevention) | **COVERED** | Covered in glossary |
| NAC (Network Access Control) | **COVERED** | Covered in glossary with posture check explanation |
| EDR (Endpoint Detection and Response) | **COVERED** | Covered in glossary with decision rules |
| XDR (Extended Detection and Response) | **COVERED** | Covered in glossary and walkthrough |
| UBA (User Behavior Analytics) | **COVERED** | UEBA covered in glossary and walkthrough |

---

## 4.6 Identity and Access Management

### Account Management
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Provisioning/deprovisioning | **COVERED** | SCIM covered for automated provisioning/deprovisioning; walkthrough covers orphaned accounts |
| Permission assignments and implications | **PARTIAL** | Access control models covered but permission assignment workflows (least privilege in practice, permission creep) not explicitly taught |
| Identity proofing | **MISSING** | No coverage of verifying identity before account creation |
| Federation | **PARTIAL** | SAML IdP→SP mentioned; federation as a concept not deeply covered |
| SSO (Single Sign-On) | **COVERED** | SSO defined; SAML, OAuth, OIDC covered with decision rules |
| Interoperability | **MISSING** | Not covered (cross-platform/cross-vendor IAM) |
| Attestation | **MISSING** | No coverage of periodic access review/attestation |

### Access Controls
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| MAC (Mandatory Access Control) | **COVERED** | Defined with SELinux example |
| DAC (Discretionary Access Control) | **COVERED** | Defined with chmod example |
| RBAC (Role-Based Access Control) | **COVERED** | Defined with AD groups example |
| Rule-based access control | **MISSING** | Not covered (distinct from RBAC — uses IF/THEN rules, e.g., firewall rules) |
| ABAC (Attribute-Based Access Control) | **COVERED** | Defined as most flexible with policy conditions |
| Time-of-day restrictions | **PARTIAL** | Mentioned as an ABAC attribute example but not as standalone concept |
| Least privilege | **MISSING** | Not explicitly defined as an access control principle |

### Multifactor Authentication
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| MFA implementations | **PARTIAL** | MFA defined; FIDO2 covered. Missing: push notifications, TOTP/HOTP, SMS codes, hardware tokens specifics |
| Something you know | **COVERED** | Listed as MFA factor |
| Something you have | **COVERED** | Listed as MFA factor |
| Something you are | **COVERED** | Listed as MFA factor |
| Somewhere you are | **COVERED** | Listed as MFA factor |

### Password Concepts
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Password best practices | **PARTIAL** | Key stretching (bcrypt, PBKDF2) and salting mentioned in exam terminology; missing: complexity requirements, length vs complexity, expiration policies, reuse prevention |
| Password managers | **MISSING** | Not covered |
| Passwordless authentication | **PARTIAL** | FIDO2 covered as passwordless standard; no broader passwordless discussion |

### Privileged Access Management
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| PAM (Privileged Access Management) | **COVERED** | Defined in glossary with credential vaulting, JIT (Just-in-Time) access, session recording |

---

## 4.7 Automation and Orchestration

### Use Cases
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| User provisioning | **PARTIAL** | SCIM covers automated provisioning but not in automation/orchestration context |
| Resource provisioning | **MISSING** | Not covered |
| Guard rails | **MISSING** | Not covered |
| Security groups | **MISSING** | Not covered (cloud security group automation) |
| Ticket creation | **MISSING** | Not covered |
| Escalation | **MISSING** | Not covered |
| Enabling/disabling services and access | **MISSING** | Not covered |
| CI/CD (Continuous Integration / Continuous Delivery) and testing | **PARTIAL** | CI/CD defined in glossary but not linked to security automation |
| Integrations and APIs (Application Programming Interfaces) | **PARTIAL** | API defined in glossary but not in automation context |

### Benefits
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Efficiency/time saving | **MISSING** | Not covered |
| Enforcing baselines | **MISSING** | Not covered |
| Standard infrastructure configurations | **MISSING** | Not covered |
| Scaling in a secure manner | **MISSING** | Not covered |
| Employee retention | **MISSING** | Not covered |
| Reaction time | **MISSING** | Not covered |
| Workforce multiplier | **MISSING** | Not covered |

**Overall 4.7 assessment: Almost entirely MISSING.** SOAR is defined in the glossary but the automation/orchestration objective is much broader than SOAR alone. Use cases and benefits are completely absent.

---

## 4.8 Incident Response

### Process
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Preparation | **COVERED** | IR steps listed in glossary |
| Detection | **COVERED** | Listed in IR steps |
| Analysis | **PARTIAL** | Detection/Identification listed; analysis as a distinct phase not emphasized |
| Containment | **COVERED** | Covered with "DO NOT power off" guidance |
| Eradication | **COVERED** | Covered in IR steps |
| Recovery | **COVERED** | Covered in IR steps |
| Lessons learned | **COVERED** | Covered in IR steps |

### Training
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Tabletop exercises | **MISSING** | Not covered |
| Simulation | **MISSING** | Not covered |
| Root cause analysis | **MISSING** | Not covered |

### Other 4.8 Topics
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Go live (cutover) | **MISSING** | Not covered |
| Alert rules of engagement | **MISSING** | Not covered |
| Reporting and communication | **MISSING** | Not covered (internal/external reporting, breach notification) |
| Stakeholder management | **MISSING** | Not covered |

---

## 4.9 Use Data Sources to Support an Investigation

### Log Data
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Firewall logs | **MISSING** | Not covered |
| Application logs | **MISSING** | Not covered |
| Endpoint logs | **MISSING** | Not covered |
| OS-specific security logs | **MISSING** | Not covered (Windows Event Log, syslog, journald) |
| IPS/IDS logs | **MISSING** | Not covered as investigation data source |
| Network logs | **MISSING** | Not covered |
| Metadata | **MISSING** | Not covered as investigation data source |

### Data Sources
| Sub-topic | Status | Notes |
|-----------|--------|-------|
| Vulnerability scans | **PARTIAL** | SCAP/CVE/CVSS covered but not framed as investigation data source |
| Automated reports | **MISSING** | Not covered |
| Dashboards | **MISSING** | Not covered |
| Packet captures | **MISSING** | Not covered |

**Overall 4.9 assessment: Almost entirely MISSING.** Forensic principles (order of volatility, chain of custody) are in the glossary, but the specific log types and data sources listed in this objective are absent.

---

## Summary: Coverage Heat Map

| Objective | Coverage | Priority |
|-----------|----------|----------|
| **4.1** Secure techniques for computing resources | **PARTIAL** — Wireless/crypto strong; baselines, hardening targets, mobile, app security weak | HIGH |
| **4.2** Asset management | **MISSING** — Entire objective absent | CRITICAL |
| **4.3** Vulnerability management | **PARTIAL** — CVE/CVSS/SCAP covered; pen testing, response/remediation, validation missing | HIGH |
| **4.4** Alerting and monitoring | **PARTIAL** — SIEM/DLP/SCAP covered; SNMP, NetFlow, alert tuning, archiving missing | HIGH |
| **4.5** Modify enterprise capabilities | **PARTIAL** — EDR/XDR/NAC/FIM/DLP strong; email security (DMARC/DKIM/SPF), web filtering, OS security, secure protocols entirely missing | CRITICAL |
| **4.6** IAM | **COVERED** — Best-covered objective; minor gaps in rule-based AC, identity proofing, attestation, password managers | MEDIUM |
| **4.7** Automation and orchestration | **MISSING** — SOAR defined but use cases and benefits entirely absent | CRITICAL |
| **4.8** Incident response | **PARTIAL** — Core IR process covered; training (tabletop, simulation), reporting, stakeholder management missing | MEDIUM |
| **4.9** Data sources for investigation | **MISSING** — Log types, packet captures, dashboards all absent | CRITICAL |

### Top Priority Gaps (Highest Exam Impact)

1. **Email security (DMARC/DKIM/SPF)** — Frequently tested, zero coverage
2. **Asset management lifecycle** (4.2) — Entire objective missing
3. **Automation use cases and benefits** (4.7) — Entire objective missing
4. **Investigation data sources and log types** (4.9) — Entire objective missing
5. **Penetration testing environments** (known/partially known/unknown) — Common exam question
6. **Secure baselines** (establish/deploy/maintain) — Foundation of 4.1
7. **MDM and mobile deployment models** (BYOD/COPE/CYOD) — Frequently tested
8. **Web filtering** (proxy, URL scanning, content categorization) — Entire sub-topic missing
9. **SNMP traps and NetFlow** — Common monitoring tool questions
10. **Common ports and secure protocol replacements** — Fundamental exam knowledge

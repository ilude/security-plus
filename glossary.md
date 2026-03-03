# Security+ SY0-701 — Complete Acronym Glossary

Organized by category. Decision rules for commonly confused groups appear in boxed sections after each group.

---

## 1. Security Operations & Monitoring

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **SIEM** | Security Information and Event Management | Aggregates and correlates logs from all sources. Generates alerts. Passive — analysts investigate. Compliance reporting. |
| **XDR** | Extended Detection and Response | Unified detection + automated response across endpoint, network, cloud, email. One platform. Active. |
| **SOAR** | Security Orchestration, Automation, and Response | Automates IR workflows via playbooks. Orchestrates multiple separate tools (firewall + AD + ticketing). |
| **UEBA** | User and Entity Behavior Analytics | ML baselines of normal behavior per user/entity. Flags deviations. Insider threat detection. |
| **EDR** | Endpoint Detection and Response | Monitors + detects + auto-responds on endpoints only. Agent-based. Isolate, kill process. |
| **HIDS** | Host-based Intrusion Detection System | Monitors + alerts on a single host. Passive. No response capability. Old school. |
| **NIDS** | Network-based Intrusion Detection System | Monitors + alerts on network traffic. Passive. Placed on span/mirror port or network tap. |
| **IDS** | Intrusion Detection System | Umbrella term for HIDS/NIDS. Detect and alert only. No blocking. |
| **IPS** | Intrusion Prevention System | Detect + automatically block attacks inline. Network layer. Signatures + anomaly detection. |
| **FIM** | File Integrity Monitoring | Detects unauthorized changes to critical files by comparing against known-good baseline. |
| **DLP** | Data Loss Prevention | Prevents unauthorized data exfiltration. Network DLP (email/web), Endpoint DLP (USB/print), Cloud DLP (SaaS). |
| **SOC** | Security Operations Center | The team/facility that monitors and responds to security events 24/7. |
| **MSSP** | Managed Security Service Provider | Outsourced 24/7 security monitoring. "Small company can't afford a SOC." |
| **NOC** | Network Operations Center | Monitors network availability and performance. NOT security-focused (that's SOC). |

> **SIEM vs XDR vs SOAR vs UEBA — Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Log aggregation, correlation, compliance reporting, retention | **SIEM** |
> | Unified detection + response across multiple layers in ONE platform | **XDR** |
> | Playbook, orchestrate multiple separate tools, automate IR workflow | **SOAR** |
> | Behavioral baseline, "unusual," "abnormal," "deviation from pattern," insider threat | **UEBA** |
>
> - Both SIEM and XDR "correlate." SIEM correlates **logs** passively. XDR correlates **telemetry across layers** and **responds** actively.
> - Both XDR and SOAR automate response. XDR does it **within its own platform**. SOAR **orchestrates separate tools** via playbooks.
> - Both SIEM and UEBA detect threats. SIEM uses **static rules** an analyst wrote. UEBA uses **ML behavioral baselines** per user.

> **IDS vs IPS vs Firewall vs WAF — Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Block traffic by port/protocol/IP at network boundary | **Firewall** |
> | Automatically block attacks based on signatures (network layer) | **IPS** |
> | Detect and alert only, no blocking | **IDS** |
> | Block web application attacks (SQLi, XSS, OWASP Top 10) | **WAF** |

> **EDR vs XDR vs HIDS — Decision Rules:**
>
> - HIDS = monitor + alert only (passive, single host)
> - EDR = monitor + detect + respond (active, endpoint only)
> - XDR = EDR extended across endpoint + network + cloud + email (cross-layer)

---

## 2. Cloud Security

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **CASB** | Cloud Access Security Broker | Sits between users and SaaS apps. Shadow IT discovery, cloud DLP, access control. "Cloud bouncer for users." |
| **CSPM** | Cloud Security Posture Management | Monitors cloud infrastructure configs for misconfigurations and compliance drift. "Cloud auditor for configs." |
| **CWPP** | Cloud Workload Protection Platform | Protects running workloads (VMs, containers, serverless). Runtime threat detection. "Cloud bodyguard for workloads." |
| **CNAPP** | Cloud-Native Application Protection Platform | CSPM + CWPP unified in one platform. Pick when question says "single/consolidated/unified." |
| **SWG** | Secure Web Gateway | Filters all web traffic (URLs, malware scanning). "Web proxy on steroids." Not cloud-specific. |
| **SASE** | Secure Access Service Edge | Umbrella: CASB + SWG + ZTNA + SD-WAN in one cloud platform. Multiple capabilities = SASE. |
| **ZTNA** | Zero Trust Network Access | Identity-verified access to specific apps. Replaces VPN. No broad network access. Per-app, per-session. |
| **SDP** | Software-Defined Perimeter | Dynamic 1-to-1 connections. Resources invisible to unauthorized users ("black cloud"). Implements ZTNA. |
| **IaaS** | Infrastructure as a Service | Provider gives you VMs/storage/networking. You manage OS and up. (AWS EC2, Azure VMs) |
| **PaaS** | Platform as a Service | Provider manages through runtime. You manage app + data only. (Heroku, Azure App Service) |
| **SaaS** | Software as a Service | Provider manages everything. You manage data + access only. (Office 365, Salesforce) |
| **FaaS** | Function as a Service | Serverless. Code runs on events, no server management. No OS patching. (AWS Lambda, Azure Functions) |
| **CSP** | Cloud Service Provider | The company providing cloud services (AWS, Azure, GCP). |

> **CASB vs CSPM vs CWPP vs CNAPP — Decision Rules:**
>
> | Question describes... | Answer |
> |---|---|
> | Users accessing unauthorized SaaS, shadow IT, cloud DLP | **CASB** |
> | Misconfigured security groups, public buckets, compliance drift | **CSPM** |
> | Container escape, runtime malware, workload vulnerability at runtime | **CWPP** |
> | "Single/unified/consolidated" combining config + workload protection | **CNAPP** |
>
> - CASB watches **people using cloud apps**. CSPM watches **cloud infrastructure settings**. Different things entirely.
> - Open S3 bucket = config problem = CSPM. Employee uploading PII to Dropbox = user behavior = CASB.
> - CNAPP = CSPM + CWPP. Only pick CNAPP when the question asks for both in one.

> **Shared Responsibility Model:**
>
> - Customer ALWAYS responsible for: **data, access management, identity** (all service models)
> - Provider ALWAYS responsible for: **physical security, hypervisor**
> - IaaS: customer manages OS and up. PaaS: customer manages app + data. SaaS: customer manages data + access only.

> **SASE vs CASB vs SWG vs ZTNA:**
>
> - CASB = cloud app access control. SWG = web traffic filtering. ZTNA = per-app zero trust access.
> - SASE = all three combined + SD-WAN. If the question lists multiple capabilities in one cloud platform → SASE.

---

## 3. Vulnerability Management & Threat Intelligence

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **CVE** | Common Vulnerabilities and Exposures | Unique identifier for a vulnerability (CVE-2024-12345). The "license plate." Maintained by MITRE. |
| **CVSS** | Common Vulnerability Scoring System | Severity rating 0-10. The "danger rating." Prioritizes patching. |
| **NVD** | National Vulnerability Database | NIST-maintained searchable database of CVEs with CVSS scores. The "DMV database." |
| **SCAP** | Security Content Automation Protocol | Umbrella framework for automated vuln scanning and compliance checking. Multi-vendor interoperability. |
| **CPE** | Common Platform Enumeration | Standardized IDs for platforms/products. Part of SCAP. "Which platforms are affected." |
| **CCE** | Common Configuration Enumeration | Standardized IDs for configuration settings. Part of SCAP. |
| **OVAL** | Open Vulnerability and Assessment Language | Machine-readable vuln test definitions. Part of SCAP. "Automated assessment." |
| **XCCDF** | Extensible Configuration Checklist Description Format | Security benchmark checklists (CIS benchmarks use this). Part of SCAP. |
| **STIX** | Structured Threat Information Expression | Language/format for describing threat intelligence (IOCs, campaigns, threat actors). The "package." |
| **TAXII** | Trusted Automated Exchange of Intelligence Information | Transport mechanism for STIX data. Publish/subscribe model. The "delivery truck." |
| **IoC** | Indicator of Compromise | Evidence breach HAS occurred (IPs, hashes, domains). Reactive/forensic. |
| **IoA** | Indicator of Attack | Evidence attack is in progress. Focuses on behavior/TTPs. Proactive. |
| **TTP** | Tactics, Techniques, and Procedures | Behavioral patterns of threat actors. Hardest to change (top of Pyramid of Pain). |

> **SCAP vs STIX/TAXII — Two Separate Worlds:**
>
> | World | Purpose | Standards |
> |---|---|---|
> | Vulnerability Management | Scanning, scoring, compliance | SCAP (CVE, CVSS, CPE, CCE, OVAL, XCCDF), NVD |
> | Threat Intelligence Sharing | Describing and exchanging threat data | STIX (format), TAXII (transport) |
>
> - "Automated vulnerability scanning / compliance checking" → **SCAP** (always)
> - "Sharing threat intel between organizations" → **STIX/TAXII** (always)
> - They never overlap. STIX never scans. SCAP never shares threat intel.

> **IoC vs IoA:**
>
> - IoC = evidence breach happened (past tense, forensic). File hashes, malicious IPs.
> - IoA = evidence attack is in progress (present tense, behavioral). Unusual process activity, lateral movement.

---

## 4. Threat Frameworks

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **ATT&CK** | Adversarial Tactics, Techniques, and Common Knowledge | MITRE's catalog of adversary TTPs with T-numbers. "What did attacker DO." Non-linear matrix. |
| **Kill Chain** | Cyber Kill Chain | Lockheed Martin's 7 sequential phases: Recon → Weaponize → Deliver → Exploit → Install → C2 → Actions. "At which STAGE." |
| **Diamond Model** | Diamond Model of Intrusion Analysis | 4 vertices: adversary, capability, infrastructure, victim. Attribution and relationships. "Pivot between elements." |
| **NIST CSF** | NIST Cybersecurity Framework | Identify, Protect, Detect, Respond, Recover. Organizational governance functions. "How should ORG handle it." |
| **NIST 800-53** | NIST Special Publication 800-53 | Comprehensive catalog of security controls for federal systems. The control library. |
| **NIST 800-207** | NIST Special Publication 800-207 | Zero trust architecture guidelines. "Never trust, always verify." |
| **ISO 27001** | ISO/IEC 27001 | International standard for Information Security Management Systems (ISMS). Certification-based. |
| **CIS** | Center for Internet Security | Publishes CIS Controls (prioritized security actions) and CIS Benchmarks (hardening guides). |

> **Framework Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | T-numbers, matrix of techniques, specific TTPs, threat hunting | **MITRE ATT&CK** |
> | Sequential phases, linear progression, delivery/exploitation/C2 | **Cyber Kill Chain** |
> | 4 elements, relationships, attribution, "pivot between known/unknown" | **Diamond Model** |
> | Organizational functions: Identify/Protect/Detect/Respond/Recover | **NIST CSF** |
> | Federal security controls catalog, compliance baselines | **NIST 800-53** |
> | Zero trust architecture principles | **NIST 800-207** |
> | International ISMS certification | **ISO 27001** |
> | Prioritized security actions, hardening benchmarks | **CIS** |

---

## 5. Identity & Access Management

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **AAA** | Authentication, Authorization, and Accounting | Three-part framework: verify identity, grant permissions, log activity. |
| **SSO** | Single Sign-On | One login grants access to multiple applications. |
| **MFA** | Multi-Factor Authentication | Requires 2+ factors: something you know, have, are, somewhere you are. |
| **SAML** | Security Assertion Markup Language | XML-based enterprise SSO. IdP → SP. Browser-based. "Signed XML." |
| **OAuth** | Open Authorization (2.0) | Authorization framework (NOT authentication). Grants limited access tokens. "Let app access my stuff." |
| **OIDC** | OpenID Connect | Authentication layer ON TOP of OAuth 2.0. ID tokens. "Log in with Google." |
| **SCIM** | System for Cross-domain Identity Management | Automated user provisioning/deprovisioning across SaaS. "Disable in AD → removed everywhere." Solves orphaned accounts. |
| **RADIUS** | Remote Authentication Dial-In User Service | Network access auth (Wi-Fi, VPN). UDP. Not web SSO. |
| **TACACS+** | Terminal Access Controller Access-Control System Plus | Like RADIUS but TCP, encrypts full payload, separates AAA functions. Cisco-heavy. |
| **LDAP** | Lightweight Directory Access Protocol | Queries directory services (Active Directory). Port 389 (636 for LDAPS). |
| **Kerberos** | Kerberos | Ticket-based auth for on-prem/AD. Port 88. Uses KDC (Key Distribution Center), TGT (Ticket Granting Ticket). |
| **PAM** | Privileged Access Management | Controls/audits elevated admin access. Credential vaulting, session recording, JIT. |
| **JIT** | Just-in-Time Access | No standing privileges. Time-limited elevated access with approval. Auto-revoked. |
| **FIDO2** | Fast Identity Online 2 | Passwordless auth standard using public key crypto. Hardware keys or platform authenticators. Phishing-resistant. |
| **RBAC** | Role-Based Access Control | Access by role (Admin, Editor, Viewer). AD groups. |
| **ABAC** | Attribute-Based Access Control | Access by attributes (time, location, department, clearance). Most flexible. Policy rules with conditions. |
| **MAC** | Mandatory Access Control | System/policy enforced, users can't override. SELinux, AppArmor. "Even root can't bypass." |
| **DAC** | Discretionary Access Control | Owner controls access. chmod, ACLs. Standard file permissions. |
| **ACL** | Access Control List | List of permissions attached to a resource defining who can do what. |
| **NAC** | Network Access Control | Posture check at the network door. Remediation VLAN if fail. Health check before granting access. |
| **PDP** | Policy Decision Point | Zero trust brain. Evaluates access requests, makes allow/deny decision. |
| **PEP** | Policy Enforcement Point | Zero trust bouncer. Executes PDP's decision. Allows/blocks traffic. |

> **SAML vs OAuth vs OIDC vs SCIM — Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Enterprise SSO, web-based, IdP → SP, XML assertions | **SAML** |
> | Third-party app access, "delegate permissions," API access tokens | **OAuth** |
> | "Log in with Google," prove identity via third party | **OIDC** |
> | Automated provisioning/deprovisioning, orphaned accounts, lifecycle | **SCIM** |
>
> - **OAuth ≠ authentication.** If question asks "prove identity" → OIDC, not OAuth.
> - **SAML stops login. SCIM removes the account.** SAML = authentication. SCIM = lifecycle management.

> **Access Control Models — Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | System enforced, users can't override, labels/classifications, SELinux | **MAC** |
> | Owner controls access, chmod, file permissions | **DAC** |
> | Access by job role, AD groups, Admin/Editor/Viewer | **RBAC** |
> | Access by attributes/conditions (time, location, department) | **ABAC** |
>
> - MAC is the strictest (military/government). ABAC is the most flexible (policy engines with conditions).

> **NAC vs Zero Trust:**
>
> - NAC = posture check **to get on the network** (gate at the door)
> - Zero trust = verification **for every resource request regardless of network location** (already on LAN? still verified)

> **RADIUS vs TACACS+:**
>
> | | RADIUS | TACACS+ |
> |---|---|---|
> | Protocol | UDP | TCP |
> | Encryption | Password only | Entire payload |
> | AAA | Combined | Separated (more granular) |
> | Common use | Network access (Wi-Fi, VPN) | Device admin (routers, switches) |

---

## 6. Cryptography & PKI

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **AES** | Advanced Encryption Standard | Symmetric encryption. Current standard. 128/192/256-bit keys. Fast, bulk data. |
| **3DES** | Triple Data Encryption Standard | Symmetric. Legacy, being phased out. Three passes of DES. |
| **RSA** | Rivest-Shamir-Adleman | Asymmetric. Key exchange, digital signatures, encryption of small data. Most widely used. |
| **ECC** | Elliptic Curve Cryptography | Asymmetric. Smaller keys, same security as RSA. Mobile/IoT friendly. |
| **DH** | Diffie-Hellman | Key exchange algorithm. Establishes shared secret over untrusted network. |
| **ECDHE** | Elliptic Curve Diffie-Hellman Ephemeral | Key exchange with PFS. Ephemeral keys per session. Modern TLS default. |
| **DSA** | Digital Signature Algorithm | Asymmetric. Digital signatures only (not encryption). |
| **SHA** | Secure Hash Algorithm | Hashing (SHA-256, SHA-3). One-way, integrity verification. Not encryption. |
| **MD5** | Message Digest 5 | Hashing. **Weak/deprecated.** Collisions found. Legacy use only. |
| **HMAC** | Hash-based Message Authentication Code | Hash + secret key. Provides integrity AND authenticity. |
| **PFS** | Perfect Forward Secrecy | Compromising long-term keys doesn't compromise past sessions. Ephemeral key exchange (DHE/ECDHE). |
| **PKI** | Public Key Infrastructure | Framework for managing digital certificates and public keys. |
| **CA** | Certificate Authority | Issues and signs digital certificates. Root CA > Intermediate CA > End Entity. |
| **CRL** | Certificate Revocation List | CA publishes full list of revoked certs periodically. Old way, can be stale. |
| **OCSP** | Online Certificate Status Protocol | Real-time "is this cert revoked?" query. Modern, lighter than CRL. |
| **CSR** | Certificate Signing Request | What you submit to a CA to get a cert issued. Contains your public key. |
| **CT** | Certificate Transparency | Public logs of issued certs. Detect mis-issuance. Audit trail. |
| **CAA** | CA Authorization | DNS record specifying which CAs may issue certs for your domain. |
| **HSTS** | HTTP Strict Transport Security | Forces browsers to use HTTPS only. Prevents SSL stripping. |
| **HSM** | Hardware Security Module | Dedicated tamper-resistant appliance for crypto key management. Standalone. |
| **TPM** | Trusted Platform Module | Embedded motherboard chip. Secure boot, key storage, platform attestation. |
| **EAP-TLS** | Extensible Authentication Protocol - TLS | Client cert + server cert for Wi-Fi. Most secure wireless auth. |
| **PEAP** | Protected EAP | Server cert only, client uses username/password in TLS tunnel. No client certs needed. |
| **WPA3** | Wi-Fi Protected Access 3 | Latest wireless security. SAE (Simultaneous Authentication of Equals) replaces PSK handshake. |
| **SAE** | Simultaneous Authentication of Equals | WPA3's key exchange. Resistant to offline dictionary attacks. |
| **E2EE** | End-to-End Encryption | Data encrypted from sender to recipient. No intermediary can read it. |

> **Symmetric vs Asymmetric vs Hashing — Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Bulk data encryption, speed, shared key, "encrypt database" | **Symmetric** (AES) |
> | Key exchange, digital signatures, non-repudiation, public/private pair | **Asymmetric** (RSA, ECC, DH) |
> | Integrity verification, password storage, "detect tampering," one-way | **Hashing** (SHA-256) |
>
> - Digital signatures = asymmetric (private key signs, public key verifies). Non-repudiation = always asymmetric.
> - "Two parties who never communicated need a shared secret" = Diffie-Hellman (asymmetric key exchange).

> **HSM vs TPM:**
>
> - TPM = embedded chip on motherboard. Built into the device.
> - HSM = standalone dedicated appliance. Enterprise key management for CAs.

> **CRL vs OCSP:**
>
> - CRL = periodic full list download. Can be stale.
> - OCSP = real-time single-cert query. Modern.
> - OCSP stapling = server pre-fetches its own OCSP response, includes in TLS handshake. Best performance.

> **EAP-TLS vs PEAP:**
>
> - EAP-TLS = client AND server certs. Most secure. "Each device gets a certificate."
> - PEAP = server cert only, client uses password. Easier to deploy, less secure.

---

## 7. Application Security & DevSecOps

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **SAST** | Static Application Security Testing | Scans source code for vulns. Build-time. No running app. White box. |
| **DAST** | Dynamic Application Security Testing | Tests a running app from outside. Runtime. Black box. Simulates attacker. |
| **IAST** | Interactive Application Security Testing | Agent inside running app. Combines SAST + DAST. Runtime. Lowest false positives. |
| **SCA** | Software Composition Analysis | Scans third-party dependencies for known CVEs. Build-time. Checks libraries, not your code. |
| **SBOM** | Software Bill of Materials | Inventory of all components/versions in software. The list, not the scanner. SCA reads the SBOM. |
| **RASP** | Runtime Application Self-Protection | Security built into the application itself. Detects and blocks attacks from inside at runtime. |
| **WAF** | Web Application Firewall | Protects web apps from HTTP attacks (SQLi, XSS). Application layer. |
| **SLSA** | Supply-chain Levels for Software Artifacts | Framework for software supply chain integrity ("Salsa"). Build provenance and verification. |
| **IaC** | Infrastructure as Code | Managing infrastructure via config files (Terraform, CloudFormation). Version-controlled, reproducible. |
| **CI/CD** | Continuous Integration / Continuous Delivery | Automated build, test, deploy pipeline. |
| **API** | Application Programming Interface | Programmatic interface between software components. REST, GraphQL. |
| **SDK** | Software Development Kit | Tools and libraries for building applications on a platform. |

> **SAST vs DAST vs IAST vs SCA — Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Scan source code, no running app, build-time, white box | **SAST** |
> | Test running app from outside, black box, simulate attacker | **DAST** |
> | Agent inside running app, combines static + dynamic | **IAST** |
> | Third-party libraries, dependencies, known CVEs in components | **SCA** |
>
> - SAST/SCA = build-time (shift-left). DAST/IAST = runtime.
> - SAST scans YOUR code. SCA scans code YOU IMPORTED.

---

## 8. Web Vulnerabilities

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **XSS** | Cross-Site Scripting | Attacker's script runs in victims' browsers. Three types: stored, reflected, DOM-based. |
| **CSRF** | Cross-Site Request Forgery | Tricks logged-in browser into making unintended request. No script injection. Exploits auto cookie sending. |
| **SQLi** | SQL Injection | Malicious SQL in input fields to manipulate database. `' OR 1=1--` |
| **SSRF** | Server-Side Request Forgery | Tricks server into making requests to internal systems. Cloud metadata attack (169.254.169.254). |
| **LFI** | Local File Inclusion | Path manipulation to execute a local file on the server. |
| **RFI** | Remote File Inclusion | Like LFI but includes file from attacker's external URL. |
| **IDOR** | Insecure Direct Object Reference | Changing an object ID in URL to access another user's data. Authorization flaw. |
| **TOCTOU** | Time of Check to Time of Use | Race condition between validation and use. Application vulnerability. |
| **XXE** | XML External Entity | Exploits XML parser to read local files or make server-side requests via malicious XML input. |

> **XSS Types — Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Script saved in database, affects ALL visitors, persistent | **Stored XSS** |
> | Victim clicks link, server reflects input back in response, in server logs | **Reflected XSS** |
> | Client-side JS, innerHTML/eval, URL fragment (#), server never sees payload | **DOM-based XSS** |
>
> - "Does the server process and return the payload?" YES = reflected. NO = DOM-based.
> - Fix stored/reflected = server-side. Fix DOM-based = client-side JavaScript.

> **XSS vs CSRF:**
>
> - XSS = attacker's script runs in browser. Script tag visible.
> - CSRF = no script injection. Tricks browser into making an unintended request. Fix: anti-CSRF tokens.

---

## 9. Attack Types & Techniques

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **APT** | Advanced Persistent Threat | Nation-state or well-funded group. Long-term, stealthy, targeted. |
| **BEC** | Business Email Compromise | Executive impersonation → financial fraud. The attack type, not the technique. |
| **DDoS** | Distributed Denial of Service | Overwhelm target with traffic from many sources. Availability attack. |
| **DoS** | Denial of Service | Overwhelm target from single source. |
| **MitM** | Man-in-the-Middle | Intercepts communication. SY0-701 calls this **"on-path attack."** |
| **MitB** | Man-in-the-Browser | Malware in browser intercepts/modifies web transactions. Banking trojans. |
| **RAT** | Remote Access Trojan | Malware providing attacker remote control of victim's system. |
| **C2/C&C** | Command and Control | Attacker's infrastructure for controlling compromised systems. |
| **PtH** | Pass the Hash | Authenticate using stolen NTLM hash without cracking the password. |
| **PtT** | Pass the Ticket | Authenticate using stolen Kerberos ticket. |

> **Password Attack Types:**
>
> | Attack | How It Works |
> |---|---|
> | **Brute force** | Try every possible combination. Slowest, guaranteed. |
> | **Dictionary** | Try common words/passwords from a list. |
> | **Password spraying** | Few common passwords against MANY accounts. Stays under lockout. |
> | **Credential stuffing** | Stolen creds from one breach tried on other services. Exploits reuse. |
> | **Rainbow table** | Pre-computed hash lookup table. Defeated by salting. |
> | **Kerberoasting** | Extract Kerberos service tickets from AD, crack offline. |

> **SY0-701 Terminology Updates:**
>
> - MitM → **"on-path attack"** (official exam term)
> - DMZ → **"screened subnet"** (official exam term)

---

## 10. Governance, Risk & Compliance

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **GRC** | Governance, Risk, and Compliance | Umbrella term for the discipline of managing risk, policies, and regulatory compliance. |
| **BIA** | Business Impact Analysis | Identifies critical business functions and impact of disruption. Prerequisite for BCP/DRP. |
| **BCP** | Business Continuity Plan | Keep business running during/after disaster. Broad — includes people, processes, facilities. |
| **DRP** | Disaster Recovery Plan | Restore IT systems after disaster. Narrow — subset of BCP, technical recovery. |
| **ALE** | Annual Loss Expectancy | SLE × ARO. Expected yearly financial loss from a threat. |
| **SLE** | Single Loss Expectancy | Asset Value × Exposure Factor. Cost of one incident. |
| **ARO** | Annual Rate of Occurrence | How often a threat is expected to occur per year. |
| **EF** | Exposure Factor | Percentage of asset value lost in one incident (0-100%). |
| **AV** | Asset Value | Dollar value of the asset. Starting point for quantitative risk. |
| **RPO** | Recovery Point Objective | Max acceptable data loss (time). "How old can the backup be?" Drives backup frequency. |
| **RTO** | Recovery Time Objective | Max acceptable downtime. "How fast must we recover?" Drives recovery infrastructure. |
| **MTTR** | Mean Time to Repair/Recover | Average time to restore operations after failure. |
| **MTTD** | Mean Time to Detect | Average time to discover an incident. SOC effectiveness metric. |
| **MTBF** | Mean Time Between Failures | Average time between repairable failures. Reliability metric. |
| **MTTF** | Mean Time to Failure | Expected lifespan of non-repairable component. |

> **Quantitative Risk Formulas (Memorize):**
>
> - SLE = AV × EF
> - ALE = SLE × ARO
> - Risk = Likelihood × Impact

> **Quantitative vs Qualitative:**
>
> - Quantitative = dollar amounts and numbers (ALE, SLE, ARO). "Calculate," "cost-benefit."
> - Qualitative = subjective ratings (high/medium/low), risk matrices, expert judgment. "Prioritize," "rank."

> **RPO vs RTO vs MTTR vs MTBF vs MTTF:**
>
> | Metric | Measures |
> |---|---|
> | RPO | Max acceptable DATA LOSS (drives backup frequency) |
> | RTO | Max acceptable DOWNTIME (drives recovery speed) |
> | MTTR | Average REPAIR time (maintainability) |
> | MTTD | Average DETECTION time (SOC speed) |
> | MTBF | Time between failures — REPAIRABLE devices |
> | MTTF | Time to failure — NON-REPAIRABLE devices |

> **BCP vs DRP:**
>
> - BCP = keep business running (broad, includes people/process/facilities)
> - DRP = restore IT systems (narrow, technical, subset of BCP)

---

## 11. Regulations & Compliance Frameworks

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **GDPR** | General Data Protection Regulation | EU data privacy law. Right to erasure, data portability, breach notification within 72 hours. |
| **HIPAA** | Health Insurance Portability and Accountability Act | US healthcare data protection. PHI (Protected Health Information). |
| **PCI DSS** | Payment Card Industry Data Security Standard | Credit card data protection. 12 requirements. Quarterly scans, annual audits. |
| **SOX** | Sarbanes-Oxley Act | US financial reporting integrity. Internal controls over financial data. |
| **FERPA** | Family Educational Rights and Privacy Act | US student education records privacy. |
| **COPPA** | Children's Online Privacy Protection Act | US children under 13 online data collection. |
| **FISMA** | Federal Information Security Management Act | US federal agency cybersecurity requirements. Uses NIST frameworks. |
| **SOC 1** | Service Organization Control Type 1 | Financial controls audit (SOX context). |
| **SOC 2** | Service Organization Control Type 2 | Security/trust controls audit (vendor risk). |
| **Type I** | Point-in-time | Control design assessment at a single point. "Exists today." |
| **Type II** | Over a period | Control effectiveness over 6-12 months. "Worked consistently." More valuable. |

> **SOC Reports:**
>
> - SOC 1 = financial controls. SOC 2 = security controls.
> - Type I = snapshot. Type II = over time. "Worked consistently" > "exists today."

> **PCI DSS Roles:**
>
> | Role | What They Do |
> |---|---|
> | **ASV** (Approved Scanning Vendor) | Quarterly external vulnerability scans |
> | **QSA** (Qualified Security Assessor) | On-site compliance audits |
> | **ISA** (Internal Security Assessor) | Employee trained for internal assessments |

---

## 12. Agreements & Policies

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **NDA** | Non-Disclosure Agreement | Prevents sharing confidential info. Sign FIRST before sharing anything proprietary. |
| **MSA** | Master Service Agreement | Foundational legal contract with vendor. Baseline terms for all future work. |
| **SOW** | Statement of Work | Specific project deliverables, timelines, milestones. References MSA. |
| **MOU** | Memorandum of Understanding | Informal agreement of mutual intent. Less binding than a contract. |
| **BPA** | Business Partners Agreement | Defines relationship/responsibilities between business partners. Joint ventures. |
| **SLA** | Service Level Agreement | Defines performance metrics (uptime, response time) a provider must meet. |
| **BAA** | Business Associate Agreement | HIPAA-required when vendor handles PHI. |
| **DPA** | Data Processing Agreement | GDPR-required when processor handles personal data. |
| **ISA** | Interconnection Security Agreement | Documents security requirements when connecting two organizations' networks. |
| **AUP** | Acceptable Use Policy | What users can/cannot do on org systems. Signed during onboarding. |
| **RoPA** | Records of Processing Activities | GDPR Art 30. Master register of ALL data processing org-wide. |
| **PIA/DPIA** | Privacy/Data Protection Impact Assessment | Evaluates privacy risks of ONE specific project or change. |

> **Agreement Order (typical vendor engagement):**
>
> 1. **NDA** — before sharing anything
> 2. **MSA** — baseline legal terms
> 3. **SOW** — specific project work
> 4. **SLA** — performance expectations

> **RoPA vs PIA/DPIA:**
>
> - RoPA = map of EVERYTHING (all processing activities org-wide)
> - PIA = assessment of ONE THING (single project's privacy impact)

---

## 13. Data Protection & Privacy

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **PII** | Personally Identifiable Information | Data that identifies an individual (name, SSN, email, biometrics). |
| **PHI** | Protected Health Information | Health-related PII (medical records, diagnoses, treatment). HIPAA-regulated. |
| **DLP** | Data Loss Prevention | Prevents unauthorized data exfiltration. Network, endpoint, or cloud variants. |
| **DRM** | Digital Rights Management | Controls how digital content can be used/distributed. Copy protection. |
| **CDE** | Cardholder Data Environment | Systems that store/process/transmit credit card data. PCI DSS scope boundary. |

> **Data Governance Roles:**
>
> | Role | Who | What They Do |
> |---|---|---|
> | **Data owner** | Business executive | Decides classification, access policies, retention. Makes the rules. |
> | **Data custodian** | IT staff | Implements owner's decisions. Backups, encryption, access provisioning. |
> | **Data steward** | Data management | Ensures data quality, consistency, metadata. "Data librarian." |
> | **Data controller** | Organization (GDPR) | Decides why/how data is processed. |
> | **Data processor** | Organization (GDPR) | Processes data on behalf of controller. |
>
> - Owner/custodian/steward = individual roles. Controller/processor = organizational/GDPR roles.
> - **Data owner is a BUSINESS role, not IT.** Exam will try to trick you.

> **De-identification Methods:**
>
> | Method | Reversible? | Context |
> |---|---|---|
> | **Tokenization** | Yes (vault) | PCI/payments, internal use |
> | **Pseudonymization** | Yes (mapping table) | GDPR/healthcare/research, external sharing |
> | **Anonymization** | No (permanent) | Irreversible, cannot re-link |
> | **Data masking** | No (for that copy) | Non-production environments, fictional values |
>
> - "Pseudo = sharing out, Token = keeping in." Hospital + research + re-link = pseudonymization.

---

## 14. Network & Infrastructure

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **VPN** | Virtual Private Network | Encrypted tunnel over untrusted network. Broad network access (vs ZTNA = per-app). |
| **VLAN** | Virtual Local Area Network | Logical network segmentation at Layer 2. |
| **SDN** | Software-Defined Networking | Separates control plane from data plane. Centralized programmable management. |
| **NFV** | Network Function Virtualization | Virtual firewalls/load balancers on commodity hardware. Replaces dedicated appliances. |
| **DMZ** | Demilitarized Zone | SY0-701 calls this **"screened subnet."** Network segment for public-facing services. |
| **ICS** | Industrial Control Systems | Umbrella for SCADA/DCS/PLCs. Availability > confidentiality. |
| **SCADA** | Supervisory Control and Data Acquisition | Monitors/controls industrial processes (power, water, manufacturing). Often air-gapped. |
| **DCS** | Distributed Control System | Controls industrial processes locally. Less geographically distributed than SCADA. |
| **PLC** | Programmable Logic Controller | Hardware device controlling physical processes (valves, motors). Component of ICS/SCADA. |
| **RTOS** | Real-Time Operating System | OS with guaranteed time constraints. Medical devices, avionics, manufacturing. |
| **IoT** | Internet of Things | Connected devices (cameras, sensors, appliances). Large attack surface, often unpatched. |
| **VPC** | Virtual Private Cloud | Isolated virtual network within a public cloud provider. |

---

## 15. Deception & Physical Security

| Term | What It Is |
|------|-----------|
| **Honeypot** | Single fake system, isolated from production. Attracts attackers. |
| **Honeynet** | Network of honeypots, still isolated/separate from production. |
| **Honeyfile** | Fake file (e.g., "passwords.txt") placed to detect unauthorized access. |
| **Honeytoken** | Fake credential or data element. Alerts when used. |
| **Deception technology** | Fake assets (servers, creds, files) deployed THROUGHOUT real production. Modern, automated, embedded. |

> **Deception Decision Rule:**
>
> - Isolated fake system(s) separate from production → **Honeypot/Honeynet**
> - Fake creds/files/tokens scattered throughout REAL production infrastructure → **Deception technology**
> - "Fake credentials in production network" = deception tech. Every time.

---

## 16. Incident Response & Forensics

| Acronym | Full Name | What It Does |
|---------|-----------|-------------|
| **CIRT/CSIRT** | Computer (Security) Incident Response Team | Team responsible for detecting, analyzing, responding to security incidents. |
| **IR** | Incident Response | The process of handling security incidents. |

> **IR Steps (order is sacred on the exam):**
>
> 1. **Preparation** — policies, tools, training, playbooks
> 2. **Detection/Identification** — alert fires, triage
> 3. **Containment** — stop the bleeding, isolate (DO NOT power off — preserve RAM)
> 4. **Eradication** — remove the threat (malware, compromised accounts)
> 5. **Recovery** — restore systems, verify clean
> 6. **Lessons Learned** — post-incident review, update procedures
>
> - Containment BEFORE eradication. Always.
> - "Pulling the plug" is almost always wrong. Isolate from network, preserve evidence.

> **Forensic Principles:**
>
> - **Order of volatility** — collect most volatile first: CPU registers → RAM → disk → logs → backups
> - **Chain of custody** — document every person, date, time, purpose. Any break = inadmissible.
> - **Legal hold** — suspends normal data retention/destruction. Overrides retention policies immediately.

---

## 17. Exam Terminology Quick Hits

| Exam Says | Means |
|-----------|-------|
| "On-path attack" | Man-in-the-middle |
| "Screened subnet" | DMZ |
| "Posture assessment" | Device health check (NAC context) or cloud config check (CSPM context) |
| "Shift left" | Integrate security earlier in SDLC |
| "Implicit trust zone" | Area where access granted by network location alone (zero trust eliminates these) |
| "Non-repudiation" | Digital signatures (asymmetric crypto) |
| "Key stretching" | bcrypt, PBKDF2 — makes password cracking computationally expensive |
| "Key escrow" | Third party holds copy of encryption keys |
| "Salting" | Random data added before hashing — defeats rainbow tables |
| "Credential vaulting" | PAM stores admin passwords, humans never know them |
| "Mantrap" | Access control vestibule — two-door interlocking entry |
| "Piggybacking" | Authorized person knowingly lets unauthorized person follow through |
| "Tailgating" | Unauthorized person follows without authorized person's knowledge |
| "Fail-open" | Device allows traffic when it fails (availability prioritized) |
| "Fail-closed" | Device blocks traffic when it fails (security prioritized) |
| "Jump box" | Jump server — hardened admin access point into a secure segment |
| "Policy Engine" | Zero trust brain — makes allow/deny decisions (also called PDP) |
| "Policy Administrator" | Zero trust intermediary — executes PE's decision, instructs PEP |
| "Adaptive identity" | Dynamic trust evaluation per-session based on real-time signals |
| "Threat scope reduction" | Zero trust principle — limit what any one identity can reach |
| "Open public ledger" | Blockchain — distributed tamper-evident record, publicly verifiable |
| "Steganography" | Hides data inside normal-looking files (image, audio, video) |
| "Secure enclave" | Hardware-isolated CPU region protecting sensitive data even from OS |
| "SAN certificate" | Subject Alternative Name — one cert covering multiple different domains |
| "Wildcard certificate" | `*.domain.com` — covers all subdomains of one domain |
| "Root of trust" | Foundational trusted CA at the top of certificate chain |
| "Journaling" | Write-ahead logging for database point-in-time recovery |
| "Managed PDU" | Smart power strip with remote monitoring and outlet control |
| "Platform diversity" | Using different vendors/OSes to reduce single-point vulnerability |

---

## 18. Security Control Categories and Types

### Control Categories

| Category | What It Covers | Examples |
|----------|---------------|---------|
| **Technical** | Technology-enforced controls. Hardware and software mechanisms. | Firewalls, encryption, IDS/IPS, MFA, access control lists |
| **Managerial / Administrative** | Policies, procedures, governance. People and paper controls. | Security policies, risk assessments, background checks, training programs |
| **Operational** | Day-to-day procedures carried out by people. Process-based controls. | Incident response procedures, change management, awareness training, guard patrols |
| **Physical** | Controls protecting physical access to facilities and hardware. | Locks, fencing, bollards, badge readers, security cameras, mantraps |

### Control Types

| Type | What It Does | When It Acts | Examples |
|------|-------------|-------------|---------|
| **Preventive** | Stops an incident before it occurs. | Before the event. | Firewalls, encryption, access badges, policies, fencing |
| **Detective** | Identifies that an incident has occurred or is occurring. | During or after the event. | IDS, SIEM, video surveillance, audit logs, motion sensors |
| **Corrective** | Reduces the impact after an incident occurs. Restores normal state. | After the event. | Backups/restore, patch deployment, incident response |
| **Deterrent** | Discourages potential attackers from attempting an attack. | Before the event (psychological effect). | Warning signs, visible cameras, security guards, lighting |
| **Compensating** | Alternative control used when primary control is not feasible. | Ongoing, supplements or replaces another control. | Network monitoring on a legacy system that cannot be patched |
| **Directive** | Instructs people on expected behavior. Policy and training controls. | Ongoing. | Security policies, acceptable use policies, compliance mandates |

> **Control Category × Type Matrix:**
>
> | Example | Category | Type |
> |---------|----------|------|
> | Firewall | Technical | Preventive |
> | Encryption | Technical | Preventive |
> | IDS alert | Technical | Detective |
> | Antivirus quarantine | Technical | Corrective |
> | Security policy | Managerial | Directive |
> | Risk assessment | Managerial | Detective (identifies gaps) |
> | Guard patrol schedule | Operational | Preventive / Detective |
> | Incident response plan | Operational | Corrective |
> | Fence / bollard | Physical | Preventive / Deterrent |
> | Security camera | Physical | Detective / Deterrent |
> | Warning signs | Physical | Deterrent |
> | Network monitoring on unpatched ICS | Technical | Compensating |

> **Control Type Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Stops attack before it happens, blocks access | **Preventive** |
> | Identifies / alerts after attack occurs, logs activity | **Detective** |
> | Fixes or restores after an incident | **Corrective** |
> | Discourages by being visible, "warning," "sign," "light" | **Deterrent** |
> | "Cannot patch," "legacy," used instead of primary control | **Compensating** |
> | Policy, mandate, training, acceptable use | **Directive** |
>
> - Deterrent vs Preventive: Deterrent works psychologically BEFORE an attempt (the attacker chooses not to try). Preventive physically/technically STOPS an attempt already in progress.
> - A control can belong to multiple types. A camera is both Detective (records evidence) and Deterrent (visible presence discourages).

---

## 19. Change Management

### Process Components

| Term | What It Means |
|------|--------------|
| **Approval process** | Formal authorization before changes are implemented. Change advisory board (CAB) reviews and approves. Prevents unauthorized changes. |
| **Ownership** | Individual or team accountable for the change. Owns the outcome and any rollback. |
| **Stakeholders** | All parties affected by or interested in the change. Must be notified and may need to approve. |
| **Impact analysis** | Assessment of how the change affects systems, users, security posture, and business operations before implementation. |
| **Test results** | Evidence from pre-production testing that the change works as intended. Required before production deployment. |
| **Backout plan** | Documented procedure to reverse the change if something goes wrong. Must be prepared before implementation begins. |
| **Maintenance window** | Pre-approved time period when changes are permitted, typically low-traffic hours. Minimizes business disruption. |
| **SOP (Standard Operating Procedure)** | Step-by-step documented process. Ensures changes are performed consistently and correctly by any operator. |

### Technical Implications of Changes

| Term | Security Implication |
|------|---------------------|
| **Allow list** | Only explicitly permitted items (apps, IPs, hashes) can execute or connect. More restrictive than deny list. |
| **Deny list / Block list** | Explicitly prohibited items are blocked. Everything else is permitted. Requires ongoing maintenance. |
| **Restricted activities** | Actions prohibited during change window (e.g., no additional changes while one is in progress, no access to production). |
| **Downtime** | Planned service interruption during the change. Must be communicated, scheduled, and minimized. |
| **Service restart** | Restarting a service to apply configuration changes. May cause brief interruption. Must be planned. |
| **Application restart** | Restarting an application (vs. OS service). Configuration and session state implications. |
| **Legacy applications** | Older systems that may not support modern patches or changes. May require compensating controls. Special handling needed. |
| **Dependencies** | Other systems or services that rely on the component being changed. Changes can break downstream dependencies unexpectedly. |

### Documentation and Version Control

| Term | What It Means |
|------|--------------|
| **Change documentation** | Records what changed, when, by whom, why, and the expected outcome. Audit trail. |
| **Version control** | Tracks changes to configurations, code, and scripts over time. Enables rollback to prior state. Examples: Git, SVN. |
| **Configuration baseline** | Approved, documented standard configuration. Changes measured against the baseline. |

> **Change Management Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Who approves changes before implementation | **Approval process / CAB** |
> | How to undo a failed change | **Backout plan** |
> | When changes are allowed to occur | **Maintenance window** |
> | Only approved software can run on endpoints | **Allow list** |
> | Old system that can't be updated | **Legacy application** — use compensating controls |
> | Track configuration history, rollback | **Version control** |
>
> - A backout plan must exist BEFORE the change. If asked "what should exist prior to making a change?" → backout plan.
> - Allow list is more secure than deny list. Deny list is easier to manage but harder to keep complete.

---

## 20. Physical Security

### Physical Barriers and Access Controls

| Term | What It Does |
|------|-------------|
| **Bollards** | Short, sturdy posts that prevent vehicle ramming attacks against buildings. Deterrent + preventive. |
| **Access control vestibule (mantrap)** | Two-door interlocking entry system. First door must close before second opens. Prevents tailgating/piggybacking. |
| **Fencing** | Perimeter barrier. Deters and delays unauthorized entry. Height and material determine security level. |
| **Video surveillance (CCTV)** | Cameras that record and/or monitor activity. Detective (evidence) and deterrent (visible presence). |
| **Security guards** | Human physical security. Flexible, can respond and use judgment. Expensive, subject to human error. |
| **Access badges** | RFID or smart card credentials that control physical entry. Logs who accessed where and when. |
| **Lighting** | Illuminates areas to deter unauthorized activity and support camera visibility. Low-cost deterrent. |

### Physical Sensors

| Sensor Type | How It Works | Best Used For |
|-------------|-------------|--------------|
| **Infrared (IR)** | Detects heat signatures from people and animals. Passive — senses emitted heat. | Indoor motion detection, perimeter alarms |
| **Pressure** | Detects weight applied to a surface (mat, floor panel). Triggers when someone steps on it. | Floors, safes, display cases, restricted access floors |
| **Microwave** | Emits microwave energy and detects movement based on reflection changes. Active sensor. Penetrates walls. | Large open areas, parking garages, outdoor perimeters |
| **Ultrasonic** | Emits ultrasonic sound waves and detects movement via reflection changes. Active. Does not penetrate walls. | Closed indoor spaces, offices, warehouses |

> **Sensor Type Decision Rules:**
>
> | If the scenario says... | Answer |
> |---|---|
> | Heat, body warmth, passive, interior rooms | **Infrared** |
> | Weight on floor, footstep triggers alarm, pressure mat | **Pressure** |
> | Large area, outdoor, penetrates walls or partitions | **Microwave** |
> | Closed room, indoor, sound-based, doesn't go through walls | **Ultrasonic** |
>
> - Microwave vs Ultrasonic: Both are active (emit and detect). Key differentiator is penetration. Microwave goes THROUGH walls. Ultrasonic does NOT.
> - Infrared is passive (detects, does not emit its own signal for detection — IR cameras differ). Context matters.

> **Tailgating vs Piggybacking:**
>
> - **Tailgating** — unauthorized person follows authorized person through a door WITHOUT their knowledge.
> - **Piggybacking** — unauthorized person follows WITH the authorized person's knowledge/consent (social engineering).
> - Both defeated by: access control vestibules (mantraps), security guards, policy enforcement.

---

## 21. Data Protection

### Data Types

| Data Type | What It Includes | Why It Matters |
|-----------|-----------------|---------------|
| **Regulated data** | Data governed by law or regulation (HIPAA PHI, PCI cardholder data, GDPR personal data). | Non-compliance results in legal penalties. Handling rules are externally mandated. |
| **Trade secret** | Proprietary business information providing competitive advantage. Formula, process, design. | Protected by law (trade secret law). Loss = competitive harm. |
| **Intellectual property (IP)** | Creations of the mind: patents, copyrights, trademarks, source code. | Legal protections apply. Unauthorized disclosure or theft is a legal and financial risk. |
| **Legal information** | Attorney-client communications, litigation strategy, contracts. | Often legally privileged. Exposure can compromise legal position. |
| **Financial information** | Earnings, forecasts, banking records, salary data. | Regulated (SOX for public companies). Insider trading risk if disclosed early. |
| **Human-readable data** | Plain text, documents, spreadsheets — directly readable by humans without processing. | Easier to exfiltrate covertly. No transformation needed by attacker. |
| **Non-human-readable data** | Binary files, encrypted data, proprietary formats — requires software or key to interpret. | Harder to use if stolen, but still requires proper protection. |

### Data Classification Levels

| Level | Description | Typical Use |
|-------|-------------|------------|
| **Public** | Intentionally available to anyone. No harm if disclosed. | Press releases, marketing materials, published documentation. |
| **Private** | Internal use only. Not for public release but lower sensitivity. | Internal memos, non-sensitive employee records. |
| **Sensitive** | Requires protection. Limited distribution. Harm if disclosed. | HR records, internal financial data, operational plans. |
| **Confidential** | Significant harm if disclosed. Restricted to specific authorized personnel. | Proprietary formulas, customer PII, merger plans. |
| **Restricted** | Highest internal classification. Severely limited access. | Encryption keys, source code, executive strategy. |
| **Critical** | Data whose loss or corruption would severely disrupt operations. | Core infrastructure configs, disaster recovery systems. |

### Data States

| State | When It Applies | Primary Protection Method |
|-------|----------------|--------------------------|
| **Data at rest** | Stored on disk, database, backup media, USB drive, cloud storage. | Encryption (full-disk encryption, database encryption, file-level encryption) |
| **Data in transit** | Moving across a network — between systems, to/from cloud, over internet. | TLS (Transport Layer Security), VPN, IPSec, HTTPS |
| **Data in use** | Actively being processed in memory, CPU, or application. | Secure enclaves, memory encryption, access controls, application security |

### Data Sovereignty and Geolocation

| Term | What It Means |
|------|--------------|
| **Data sovereignty** | Data is subject to the laws of the country where it is physically stored. GDPR data stored in the EU = EU jurisdiction. |
| **Geolocation** | Data or access is tied to a geographic location. Used to restrict processing or storage to specific regions. |
| **Geographic restrictions** | Controls that prevent data from being stored in or accessed from specific countries/regions. |

### Data Protection Methods

| Method | What It Does | Primary Data State Protected |
|--------|-------------|----------------------------|
| **Encryption** | Transforms data into unreadable ciphertext. Decryption requires key. | At rest and in transit |
| **Hashing** | One-way transformation for integrity verification. Cannot be reversed to original. | At rest (passwords, integrity checks) |
| **Masking** | Replaces real data with fictional but realistic values in non-production environments. | At rest (dev/test copies) |
| **Tokenization** | Replaces sensitive value with a token. Original stored in a vault. Reversible. | At rest and in transit (payment systems) |
| **Obfuscation** | Umbrella term — making data harder to understand or find. Masking, tokenization, steganography all qualify. | Any state |
| **Segmentation** | Isolates data by network, VLAN, or system boundary. Limits blast radius if breached. | At rest |
| **Permission restrictions** | ACLs, RBAC, ABAC controls limiting who can read, write, or delete data. | At rest and in use |

> **Data State Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Stored on a hard drive, database, USB, backup tape | **Data at rest** |
> | Sending email, uploading to cloud, API calls, FTP transfer | **Data in transit** |
> | Being processed by an application, loaded in RAM, in-memory database | **Data in use** |
>
> **Data Classification Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Anyone can see it, published externally | **Public** |
> | Internal only, general employees, low sensitivity | **Private** |
> | Requires care, limited audience, HR/financial | **Sensitive** |
> | Significant harm if disclosed, business-critical secrets | **Confidential** |
> | Highest classification, minimal access, keys/source code | **Restricted** |
>
> - The data owner (business role, not IT) decides classification level.
> - Sovereign jurisdiction follows WHERE data is stored, not where the organization is headquartered.

---

## 22. Resilience and Recovery

### High Availability

| Term | What It Does | Key Difference |
|------|-------------|---------------|
| **Load balancing** | Distributes traffic across multiple servers. Provides scalability and availability. If one node fails, others absorb load. | Active-active. Multiple servers handle live traffic simultaneously. |
| **Clustering** | Groups servers so they appear as one. Failover automatically shifts workload to surviving nodes. | Active-passive common. Focuses on automatic failover, not load distribution. |

> **Load Balancing vs Clustering:**
>
> - Load balancing = distribute traffic across servers for performance and availability. All nodes are active.
> - Clustering = group servers for failover. One node can be standby. Focus is fault tolerance.
> - A question about "distributing traffic" → load balancing. "Automatic failover if one server dies" → clustering.

### Site Types

| Site Type | Description | Cost | Recovery Time |
|-----------|-------------|------|--------------|
| **Hot site** | Fully operational duplicate. Live data replication. Staff can switch over in minutes to hours. | Highest | Minutes to hours |
| **Warm site** | Partially equipped. Systems present but not fully configured. Data must be restored. | Medium | Hours to days |
| **Cold site** | Empty facility with power and connectivity only. All hardware and software must be installed and configured. | Lowest | Days to weeks |

> **Site Type Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Immediately available, live data, failover in minutes | **Hot site** |
> | Partially configured, needs data restore, hours to recover | **Warm site** |
> | Empty building, install everything, days to weeks | **Cold site** |
>
> - Cost and RTO (Recovery Time Objective) are inversely related. Fastest recovery = highest cost.
> - Hot site = highest cost AND lowest RTO. Cold site = lowest cost AND highest RTO.

### Geographic and Platform Resilience

| Term | What It Does |
|------|-------------|
| **Geographic dispersion** | Distributes systems and data across physically separate locations. Protects against regional disasters. |
| **Platform diversity** | Uses different operating systems, vendors, or technologies across systems. Reduces risk of a single vulnerability affecting all systems. |
| **Multi-cloud** | Uses services from multiple cloud providers. Avoids vendor lock-in and reduces single-provider outage risk. |

### Capacity Planning

| Dimension | What to Plan For |
|-----------|-----------------|
| **People** | Sufficient trained staff to operate and maintain systems during normal operations and incidents. |
| **Technology** | Adequate compute, storage, and network capacity to handle peak load and support redundancy requirements. |
| **Infrastructure** | Physical space, power, cooling, and connectivity to support technology capacity. |

### Resilience Testing

| Test Type | What It Involves |
|-----------|-----------------|
| **Tabletop exercise** | Discussion-based walkthrough of a scenario. No live systems affected. Tests plans and decision-making. |
| **Failover testing** | Intentionally triggers a failover to verify that backup systems actually take over correctly. |
| **Simulation** | Full operational test that closely mimics a real disaster. More disruptive than tabletop. |
| **Parallel processing** | Running primary and backup systems simultaneously to compare output before fully switching over. |

> **Testing Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Discussion-based, no live systems, "walk through the plan" | **Tabletop exercise** |
> | Actually trigger the failover, test if backup works for real | **Failover testing** |
> | Full operational drill simulating real disaster, immersive | **Simulation** |
> | Run old and new systems side by side to compare | **Parallel processing** |

### Backups

| Term | What It Means |
|------|--------------|
| **Onsite backup** | Backup stored at the same physical location as production. Fast recovery. Vulnerable to same physical disaster. |
| **Offsite backup** | Backup stored at a separate physical location. Protected from local disasters. Slower recovery. |
| **Backup frequency** | How often backups are taken. Driven by RPO (Recovery Point Objective) — shorter RPO = more frequent backups. |
| **Backup encryption** | Encrypting backup data. Required to protect data at rest on backup media. Offline backups without encryption are a risk. |
| **Snapshot** | Point-in-time capture of a system or volume state. Fast to take, fast to restore. Common in VMs and cloud storage. |
| **Replication** | Continuous or near-continuous copying of data to another system or site. Near-zero data loss. Higher cost. |
| **Journaling** | Logs changes to data (write-ahead logging). Enables point-in-time recovery. Reduces data loss between full backups. |

> **Backup Type Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Point-in-time copy, VM, cloud volume | **Snapshot** |
> | Continuous copy to another site/system, near-zero data loss | **Replication** |
> | Transaction logs, write-ahead log, database recovery | **Journaling** |
> | Same location as production | **Onsite** |
> | Separate physical location | **Offsite** |
>
> - The 3-2-1 backup rule: 3 copies, 2 different media types, 1 offsite.
> - Onsite + offsite together satisfies the "geographically diverse" backup requirement.

### Power Resilience

| Term | What It Does |
|------|-------------|
| **UPS (Uninterruptible Power Supply)** | Battery backup that provides immediate power during outage. Buys time to gracefully shut down or switch to generator. |
| **Generator** | Provides sustained power during extended outage. Typically fueled by diesel or natural gas. Takes seconds to minutes to start. |
| **Dual supply** | Device has two separate power inputs from independent sources. If one power feed fails, the other maintains operation. |
| **Managed PDU (Power Distribution Unit)** | Smart power strip providing remote outlet monitoring and control. Enables remote power cycling. |

> **Power Resilience Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Instant power during outage, seconds of coverage | **UPS** |
> | Extended outage coverage, hours of power | **Generator** |
> | Two independent power feeds to one device | **Dual supply** |
> | Remote power cycling, monitoring individual outlets | **Managed PDU** |
>
> - UPS and generator work together: UPS provides instant power while generator starts up.

---

## 23. Security Architecture Expanded

### Modern Architecture Concepts

| Term | What It Does |
|------|-------------|
| **Microservices** | Architecture where applications are broken into small, independent services communicating via APIs. Each service is independently deployable. Attack surface is distributed. |
| **Containerization** | Packages an application and its dependencies into a portable container. Isolated from host OS. Enables consistent deployment. |
| **Docker** | Most common container runtime. Packages apps into images run as containers. |
| **Kubernetes (K8s)** | Container orchestration platform. Manages deployment, scaling, and failover of containers at scale. |
| **Virtualization** | Running multiple virtual machines on one physical host. Each VM is isolated with its own OS. Hypervisor manages resources. |
| **Embedded systems** | Purpose-built hardware running firmware for a specific function. Limited resources, often cannot be patched. Examples: printers, medical devices, routers. |
| **Hybrid cloud** | Combination of on-premises infrastructure and public cloud. Workloads can span both. Connectivity and data flow between the two must be secured. |
| **Sandboxing** | Executing code in an isolated environment to observe behavior without risking production systems. Used in malware analysis and application testing. |

### Infrastructure Considerations

| Consideration | What to Evaluate |
|---------------|-----------------|
| **Device placement** | Where network devices (firewalls, IDS, proxies) are positioned in the network topology. Determines what traffic they can inspect. |
| **Security zones** | Logical or physical network segments with consistent trust levels and controls. Screened subnet (DMZ), internal, and external zones. |
| **Attack surface** | All points where an attacker could attempt to enter or extract data. Fewer open ports, services, and interfaces = smaller attack surface. |
| **Connectivity** | How systems are connected (wired, wireless, VPN, leased line). Each connection type has different security implications. |
| **Failure modes** | How a device or control behaves when it fails. Critical design decision. |
| **Fail-open** | Device allows all traffic when it fails. Prioritizes availability. Lower security risk posture. |
| **Fail-closed** | Device blocks all traffic when it fails. Prioritizes security. Risks availability. |

> **Fail-Open vs Fail-Closed Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Security is paramount, block if unsure, high-security environment | **Fail-closed** |
> | Availability is paramount, life-safety system, cannot afford interruption | **Fail-open** |
>
> - Fail-closed = more secure, less available. Fail-open = more available, less secure.
> - Hospital ventilator system: fail-open (availability = life). Financial trading firewall: fail-closed (security = priority).

### Device Attributes

| Attribute | What It Means |
|-----------|--------------|
| **Active device** | Participates in traffic flow, can block or modify packets. IPS is active. Firewall is active. |
| **Passive device** | Monitors traffic without participating in the flow. Cannot block. IDS is passive. Uses span/mirror port. |
| **Inline** | Device sits directly in the traffic path. Can inspect AND block. IPS, firewalls. |
| **Tap / Monitor mode** | Connected to a copy of traffic (SPAN port or network tap). Cannot block. IDS, packet capture. |

### Network Appliances

| Appliance | What It Does |
|-----------|-------------|
| **Jump server (jump box)** | Hardened, isolated server used as a single controlled access point into a secure network segment. All admin access flows through it. |
| **Proxy server** | Intermediary between client and server. Caches content, filters requests, hides client identity. Forward proxy vs reverse proxy. |
| **Load balancer** | Distributes incoming traffic across multiple backend servers. Improves availability and performance. |
| **Sensors** | Network-connected devices (or software) that collect telemetry — traffic, environmental readings, physical access events — and feed data to monitoring systems. |

### Firewall Types

| Firewall Type | What It Inspects | Key Characteristic |
|--------------|-----------------|-------------------|
| **Layer 4 firewall** | IP addresses and ports (TCP/UDP). Network and transport layer. | Stateful packet filtering. Fast, no application awareness. |
| **Layer 7 firewall (NGFW)** | Application-layer content. URLs, application identity, user identity, payload. | Deep packet inspection. Identifies apps regardless of port. |
| **WAF (Web Application Firewall)** | HTTP/HTTPS traffic. Application-layer web attacks (SQLi, XSS). | Protects web applications specifically. OWASP Top 10. |
| **UTM (Unified Threat Management)** | All-in-one appliance combining firewall, IDS/IPS, antivirus, VPN, content filtering. | Single device, multiple functions. SMB-focused. |
| **NGFW (Next-Generation Firewall)** | Deep packet inspection, application awareness, user identity, SSL/TLS inspection. | Layer 7 awareness. Can detect applications on non-standard ports. |

> **Firewall Type Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Block by IP and port, basic filtering | **Layer 4 firewall** |
> | Application awareness, SSL inspection, user identity, deep packet | **NGFW** |
> | Web app attacks, SQLi, XSS, OWASP Top 10 | **WAF** |
> | All-in-one, single appliance for SMB, firewall + IPS + AV + VPN | **UTM** |
>
> - UTM and NGFW overlap. UTM = "everything in one box." NGFW = "deep inspection with application awareness." NGFW is enterprise; UTM is SMB.
> - WAF is always focused specifically on HTTP/HTTPS web application traffic.

### Port Security

| Term | What It Does |
|------|-------------|
| **802.1X** | IEEE standard for port-based Network Access Control (NAC). Device must authenticate before the switch port becomes active. Uses EAP (Extensible Authentication Protocol) for credentials. Works with RADIUS for authentication. |

### Secure Communication

| Term | What It Does |
|------|-------------|
| **IPSec** | Encrypts and authenticates IP packets. Two modes: Transport (encrypts payload only) and Tunnel (encrypts entire packet, used for VPNs). |
| **SD-WAN (Software-Defined Wide Area Network)** | Centrally managed WAN connectivity using software control. Can route traffic across MPLS, broadband, LTE. Optimizes path selection. Security policies applied centrally. |

### Secure Baselines

| Phase | What Happens |
|-------|-------------|
| **Establish** | Define the approved, hardened configuration standard for a system type (OS, application, network device). Reference configuration. |
| **Deploy** | Apply the baseline configuration to all systems of that type. Automate via IaC, configuration management tools (Ansible, Chef, Puppet). |
| **Maintain** | Continuously monitor for drift from the baseline. Enforce compliance. Update baseline when new patches or requirements emerge. |

> **Jump Server vs Proxy vs Bastion Host:**
>
> - Jump server = admin access point into a restricted network segment. Outbound admin sessions only.
> - Proxy server = intermediary for general user traffic. Content filtering, caching.
> - Bastion host = hardened server exposed to the internet, minimal services. Often used as jump server in cloud environments.

---

## 24. Cryptography Expanded

### Encryption Levels / Granularity

| Level | What Is Encrypted | Use Case |
|-------|------------------|---------|
| **Full-disk encryption (FDE)** | Entire storage device. Everything on the disk, including OS. | Laptop theft protection. BitLocker, FileVault. |
| **Partition encryption** | A specific disk partition or volume. Rest of disk may be unencrypted. | Encrypt data partition while leaving OS partition accessible. |
| **File encryption** | Individual files only. Encrypted regardless of where the file is stored. | Share a specific encrypted file without encrypting the whole system. |
| **Volume encryption** | A logical volume or container (may span multiple physical disks). | Encrypted virtual disk containers. VeraCrypt volumes. |
| **Database encryption** | Entire database or database files encrypted at rest. | Protects database files if storage is accessed directly. |
| **Record-level encryption** | Individual fields or records within a database encrypted separately. | Protecting specific sensitive fields (SSN, credit card) while leaving other fields searchable. |

> **Encryption Level Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Laptop stolen, entire drive protected, OS encrypted | **Full-disk encryption** |
> | Specific sensitive columns in a database encrypted | **Record-level encryption** |
> | Portable encrypted container, shared file vault | **Volume encryption** |
> | Individual file sent securely, file-level protection | **File encryption** |
>
> - Record-level encryption is most granular but most complex. Full-disk is simplest but least selective.
> - FDE protects data at rest but does NOT protect data while the system is running and unlocked.

### Obfuscation Techniques

| Term | What It Does |
|------|-------------|
| **Steganography** | Hides data inside other data (image, audio, video files). The existence of the hidden data is concealed. Not encryption — no key needed to see the file. Covert channel. |
| **Obfuscation** | Broad term for making data or code harder to understand. Includes steganography, masking, tokenization, code obfuscation. |

> **Steganography vs Encryption:**
>
> - Encryption = data is transformed and unreadable. Everyone knows something is encrypted.
> - Steganography = data is hidden inside another file. The hidden message is invisible — no one knows it exists.
> - Attacker who intercepts an encrypted file knows there is a secret. Attacker who intercepts a steganographic image sees only a normal image.

### Blockchain and Open Public Ledger

| Term | What It Does |
|------|-------------|
| **Blockchain** | Distributed, immutable ledger. Transactions recorded in blocks chained cryptographically. No central authority. Each block contains hash of previous block — tampering breaks the chain. |
| **Open public ledger** | A blockchain visible and verifiable by anyone. Provides transparency and tamper evidence. Used to prove that records have not been altered. |

> **Blockchain Exam Context:**
>
> - Blockchain provides non-repudiation and integrity for distributed systems — no single party controls the record.
> - "Prove data has not been tampered with" + "no central authority" + "distributed verification" → Blockchain.

### Key Management

| Term | What It Does |
|------|-------------|
| **Key management system (KMS)** | Software or service that creates, stores, rotates, and revokes cryptographic keys. Centralizes key lifecycle management. Cloud examples: AWS KMS, Azure Key Vault. |
| **Secure enclave** | Hardware-isolated region of a processor that protects code and data from the rest of the system — even the OS cannot access it. Examples: Apple Secure Enclave, Intel SGX. Used for biometric data, payment credentials. |

> **HSM vs KMS vs Secure Enclave:**
>
> - HSM = dedicated tamper-resistant hardware appliance. Enterprise CAs, financial systems.
> - KMS = software/service for key lifecycle management. Cloud-native key management.
> - Secure enclave = isolated CPU region. Device-level (phone, laptop). Protects from OS compromise.

### Certificate Types

| Certificate Type | What It Is |
|-----------------|-----------|
| **Self-signed certificate** | Certificate signed by its own private key, not a trusted CA. Free, no third-party validation. Browsers show warnings. Used in dev/test or internal systems where you control trust. |
| **Third-party certificate** | Issued by a trusted public CA (DigiCert, Let's Encrypt, Comodo). Trusted by default in browsers and OS. Required for public-facing services. |
| **Wildcard certificate** | A single certificate covering a domain and all its subdomains. `*.example.com` covers `mail.example.com`, `www.example.com`, etc. Does NOT cover multiple domains. |
| **SAN certificate (Subject Alternative Name)** | A certificate covering multiple different domain names explicitly listed. `example.com`, `example.org`, `mail.example.net` can all be covered by one SAN cert. |
| **Root of trust** | The foundational trusted anchor in a certificate chain. The Root CA certificate that all other certificates chain up to. Pre-installed in OS and browser trust stores. |

> **Certificate Type Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | All subdomains on one domain, `*.example.com` | **Wildcard certificate** |
> | Multiple different domains on one cert | **SAN certificate** |
> | No CA involved, browser warning, internal use, dev/test | **Self-signed certificate** |
> | Browsers trust it by default, public-facing website | **Third-party (CA-issued) certificate** |
> | Foundational trust anchor, root CA, pre-installed trust | **Root of trust** |
>
> - Wildcard = one domain + all subdomains. SAN = multiple different domains.
> - Self-signed = fine for internal tools. Never acceptable for public-facing services.

### Zero Trust Control Plane Details

| Component | Role |
|-----------|------|
| **Policy Engine (PE)** | The brain of zero trust. Evaluates access requests against policy. Makes the allow/deny decision. Considers identity, device posture, context, and risk signals. |
| **Policy Administrator (PA)** | Executes the Policy Engine's decision. Establishes or terminates sessions. Communicates the access decision to the Policy Enforcement Point. |
| **Policy Enforcement Point (PEP)** | The gatekeeper. Physically allows or blocks traffic based on PA's instruction. The bouncer. |
| **Adaptive identity** | Dynamically adjusts access based on real-time signals — device health, location, time, behavior. Identity trust is not static; it changes per-session or per-request. |
| **Threat scope reduction** | Principle of minimizing the blast radius by limiting what each identity/device/session can access. Least privilege applied dynamically. |
| **Policy-driven access control** | Access decisions are made by centralized policy rather than static network location. "You are on the LAN" is no longer sufficient to grant access. |

> **Zero Trust Control Plane Flow:**
>
> ```
> Subject requests resource
>       ↓
> Policy Enforcement Point (PEP) — intercepts all requests
>       ↓
> Policy Administrator (PA) — forwards to PE for evaluation
>       ↓
> Policy Engine (PE) — evaluates against policy (identity, device, context)
>       ↓
> PE decision returned to PA
>       ↓
> PA instructs PEP to allow or deny
>       ↓
> PEP permits or blocks the session
> ```

> **PDP vs Policy Engine:**
>
> - PDP (Policy Decision Point) and Policy Engine are the same concept. PDP is the older/generic term. "Policy Engine" is the NIST 800-207 zero trust specific term used on SY0-701.

---

## 25. Threat Actors and Motivations

### Threat Actor Types

| Term | Full Name / Category | What It Is |
|------|---------------------|------------|
| **Nation-state** | Nation-State Actor | Government-sponsored. Well-funded, highly sophisticated, long-term persistent access, stealthy. Motivations: espionage, sabotage, cyberwarfare. Example: APT (Advanced Persistent Threat) groups. |
| **Unskilled attacker** | Unskilled Attacker | SY0-701 term replacing "script kiddie." Uses pre-built tools without deep technical understanding. Low sophistication, limited funding. Motivation: disruption/chaos, notoriety. |
| **Hacktivist** | Hacktivist | Politically or ideologically motivated attacker. Targets organizations to make a statement. Motivation: philosophical/political beliefs. Tools: DDoS, defacement. |
| **Insider threat** | Insider Threat | Trusted individual with authorized access who causes harm. Three subtypes: malicious (intentional harm), negligent (accidental), compromised (outsider uses their account). |
| **Organized crime** | Organized Crime | Criminal organizations motivated by financial gain. Ransomware-as-a-service, data theft, fraud. Sophisticated but focused on profit, not espionage. |
| **Shadow IT** | Shadow IT | Unauthorized apps/devices used inside the organization without IT approval. Not a traditional attacker — creates risk through unmanaged data exposure, unpatched software, compliance gaps. |

### Threat Actor Attributes

| Attribute | Description |
|-----------|-------------|
| **Internal** | Has authorized access. Insider threats, negligent employees, compromised accounts. Harder to detect because activity blends with normal behavior. |
| **External** | No authorized access. Must breach perimeter. Most traditional attackers. |
| **Resources/funding** | Nation-states: unlimited. Organized crime: significant. Hacktivists: moderate. Unskilled: minimal. Determines tooling, persistence, and target scope. |
| **Sophistication** | Nation-states: highest (zero-days, custom malware). Organized crime: high (commercial tools, RaaS). Hacktivists: moderate. Unskilled: low (commodity tools). |

### Motivations

| Motivation | Typical Threat Actor |
|-----------|---------------------|
| **Data exfiltration** | Nation-state, organized crime, malicious insider |
| **Espionage** | Nation-state |
| **Financial gain** | Organized crime, ransomware operators |
| **Blackmail** | Organized crime, malicious insider |
| **Service disruption** | Hacktivist, nation-state, unskilled attacker |
| **Philosophical/political beliefs** | Hacktivist |
| **Ethical** | Authorized pentesters, security researchers |
| **Revenge** | Malicious insider (disgruntled employee) |
| **Disruption/chaos** | Unskilled attacker, hacktivist |
| **War** | Nation-state (cyberwarfare campaigns targeting critical infrastructure) |

> **Threat Actor Decision Rules:**
>
> | If the question describes... | Answer |
> |---|---|
> | Well-funded, stealthy, long-term, targeted, government interest | **Nation-state** |
> | Financial gain, ransomware, data theft for sale | **Organized crime** |
> | Pre-built tools, low skill, wants notoriety | **Unskilled attacker** |
> | Political/ideological cause, DDoS or defacement | **Hacktivist** |
> | Authorized access, disgruntled or negligent employee | **Insider threat** |
> | Unauthorized apps bypassing IT controls | **Shadow IT** |
>
> - Nation-state vs organized crime: nation-states want intelligence/disruption, organized crime wants money.
> - Malicious insider (revenge) vs compromised insider (their creds stolen by outsider) — the attacker is different, but the damage looks the same from inside.

---

## 26. Malware Types

| Term | What It Is |
|------|-----------|
| **Ransomware** | Encrypts victim's files or locks the system, demands payment for the key. Crypto ransomware = encrypts files. Locker ransomware = locks screen/device but data untouched. |
| **Trojan** | Malware disguised as legitimate software. Does not self-replicate. Requires user to execute it. RAT (Remote Access Trojan) is a common subtype. |
| **Worm** | Self-replicating malware that spreads across networks without user interaction. No host file needed. Exploits OS/network vulnerabilities automatically. |
| **Virus** | Requires a host file and user action to spread (opening the infected file). Attaches to legitimate programs. Does not self-propagate independently. |
| **Spyware** | Silently monitors user activity (keystrokes, browsing, credentials). Exfiltrates data without user knowledge. |
| **Bloatware** | Pre-installed unwanted software that consumes resources. Not inherently malicious but increases attack surface and degrades performance. |
| **Keylogger** | Records keystrokes to capture passwords, credit card numbers, and sensitive input. Can be software or hardware (USB keylogger). |
| **Logic bomb** | Malicious code that triggers on a specific condition: date/time, login event, file deletion. Lies dormant until condition is met. |
| **Rootkit** | Hides deep in the system to conceal attacker presence. Three levels: firmware (UEFI/BIOS — survives reinstall), kernel-mode (ring 0, hardest to detect), user-mode (ring 3, easier to detect). |

> **Malware Type Decision Rules:**
>
> | If the question describes... | Answer |
> |---|---|
> | Spreads automatically across network, no user action, exploits OS flaws | **Worm** |
> | Spreads via infected host file, needs user to open/execute | **Virus** |
> | Looks like legitimate software, no self-replication | **Trojan** |
> | Encrypted files, ransom demand, decryption key | **Ransomware (crypto)** |
> | Locked screen, locked device, ransom demand | **Ransomware (locker)** |
> | Hidden from OS, survives reboots, hides other malware | **Rootkit** |
> | Records keystrokes silently | **Keylogger** |
> | Triggers on date or event, planted by insider | **Logic bomb** |
> | Records activity, reports home, no visible damage | **Spyware** |
>
> - Worm vs virus: worm = no host file, spreads itself. Virus = needs a host file AND a user to execute.
> - Trojan vs virus: trojan = disguise, no spread. Virus = spreads to other files.
> - Rootkit vs trojan: trojan provides access, rootkit hides the access.
> - Logic bomb: insider threat signature — planted by someone with access who expects to leave.

---

## 27. Social Engineering and Human Vectors

| Term | What It Is |
|------|-----------|
| **Phishing** | Mass email campaign impersonating a trusted sender. Goal: steal credentials or deliver malware. Uses urgency, fear, and authority. Spear phishing = targeted at specific individual. Whaling = targets executives. |
| **Vishing** | Voice call-based social engineering. Attacker calls victim impersonating bank, IT support, or government. Collects credentials or account info verbally. |
| **Smishing** | SMS (Short Message Service)-based phishing. Malicious link in a text message. Often impersonates delivery services, banks, or toll systems. |
| **Pretexting** | Fabricating a believable scenario (pretext) to manipulate the victim. Attacker creates a false identity (IT support, auditor, vendor) before making a request. Foundation of most social engineering. |
| **Watering hole** | Compromises a website frequently visited by the target group. Victims infected when they browse the legitimate (now compromised) site. Targets a community, not an individual. |
| **Brand impersonation** | Creates fake websites, emails, or accounts mimicking a trusted brand (Microsoft, FedEx, PayPal). Drives credential harvesting or malware download. |
| **Typosquatting** | Registers misspelled domain names (gooogle.com, microosft.com) to catch mistyped URLs. Victims land on malicious site thinking it's legitimate. Also called URL hijacking. |
| **Impersonation** | Attacker poses as a trusted individual (executive, IT staff, vendor) to gain access or information. Differs from pretexting in that impersonation focuses on identity, pretexting focuses on the scenario. |
| **Misinformation** | False or inaccurate information spread without intent to deceive. Unintentional error. |
| **Disinformation** | False information spread deliberately to deceive or manipulate. Intentional. SY0-701 treats this as a threat vector — nation-states use disinformation campaigns. |

> **Social Engineering Decision Rules:**
>
> | If the question describes... | Answer |
> |---|---|
> | Bulk email, impersonating a brand, credential link | **Phishing** |
> | Phone call, impersonating support or bank | **Vishing** |
> | Text message with malicious link | **Smishing** |
> | Attacker invented a fake backstory/role before requesting info | **Pretexting** |
> | Compromised legitimate website visited by target group | **Watering hole** |
> | Misspelled domain, catches typos in URL | **Typosquatting** |
> | Fake site/email that looks exactly like a real brand | **Brand impersonation** |
> | Posing as a specific person (CEO, IT admin) | **Impersonation** |
> | False info spread by mistake / spread on purpose | **Misinformation / Disinformation** |
>
> - Pretexting provides the story. Impersonation provides the identity. They often occur together.
> - Watering hole: attacker doesn't target victims directly — waits for them to come to the compromised site.
> - Misinformation vs disinformation: one word difference on the exam. Unintentional = mis. Deliberate = dis.

---

## 28. Threat Vectors and Attack Surfaces

### Message-Based Vectors

| Vector | What It Is |
|--------|-----------|
| **Email** | Most common threat vector. Delivers phishing links, malicious attachments (macros, executables), BEC (Business Email Compromise). Spoofed sender headers bypass untrained users. |
| **SMS** | Smishing via text. Malicious links or fake authentication prompts. No email filter protection. |
| **Instant messaging (IM)** | Slack, Teams, Discord used to deliver malicious files or links. Users trust IM more than email. Less monitored by security controls. |

### File and Image-Based Vectors

| Vector | What It Is |
|--------|-----------|
| **Image-based attacks** | Steganography hides malicious payloads inside image files. Malicious SVGs can execute scripts. Attacker exfiltrates data in image metadata. |
| **File-based attacks** | Malicious macros in Office documents, polyglot files (valid in two formats simultaneously, bypasses single-type scanners), PDF exploits, weaponized archives (.zip, .iso). |

### Voice and Removable Device Vectors

| Vector | What It Is |
|--------|-----------|
| **Voice calls (vishing/SPIM)** | Vishing = voice phishing. SPIM (Spam over Instant Messaging) = unsolicited IM-based attacks. Both bypass traditional email filters. |
| **Removable devices** | USB drop attack: attacker leaves infected USB drives in target's parking lot or lobby hoping employees plug them in. Rubber Ducky: USB device that types keystrokes at high speed — appears as keyboard, bypasses USB policies. |

### Software and System Vectors

| Vector | What It Is |
|--------|-----------|
| **Vulnerable software — client-based** | Installed applications (browsers, PDF readers, email clients) with unpatched vulnerabilities. Requires agent/install on endpoint. Larger attack surface. |
| **Vulnerable software — agentless** | Web apps or services with no local install. Vulnerability is server-side. Client is a browser. Harder to patch — requires server-side update. |
| **Unsupported/end-of-life systems** | Software or hardware the vendor no longer patches. Every new CVE (Common Vulnerability and Exposure) found is a permanent vulnerability. No fix ever comes. |
| **Open service ports** | Unnecessary listening ports increase attack surface. Attackers port-scan for open services (Nmap). Every open port is a potential entry point. Close what you don't use. |
| **Default credentials** | Factory-set usernames/passwords (admin/admin, admin/password) on routers, switches, IoT (Internet of Things) devices. Attackers try defaults against every discovered device. |

### Network-Based Vectors

| Vector | What It Is |
|--------|-----------|
| **Rogue access point** | Unauthorized Wi-Fi AP (Access Point) connected to internal network. Bypasses perimeter security. Can be physical (device plugged in) or software-based. |
| **Evil twin** | Attacker creates a Wi-Fi AP with the same SSID (Service Set Identifier) as a legitimate network. Victims connect and all traffic flows through attacker. |
| **Bluejacking** | Sending unsolicited Bluetooth messages to nearby devices. Annoying but not data-stealing. No pairing required. |
| **Bluesnarfing** | Unauthorized access to data (contacts, calendar, messages) on a Bluetooth device by exploiting pairing vulnerabilities. Actual data theft. |

### Supply Chain Vectors

| Vector | What It Is |
|--------|-----------|
| **Managed service providers (MSPs)** | MSPs have privileged access to many customer environments. Compromising one MSP (Managed Service Provider) reaches all their clients simultaneously. Example: SolarWinds-style attacks. |
| **Vendors** | Third-party software vendors can be compromised to deliver malicious updates to all customers (supply chain poisoning). |
| **Suppliers** | Hardware suppliers can embed malicious components (firmware backdoors, rogue chips) before products reach the customer. |

> **Threat Vector Decision Rules:**
>
> | If the question describes... | Answer |
> |---|---|
> | USB device left in parking lot hoping someone plugs it in | **USB drop attack** |
> | USB device emulating a keyboard to type commands | **Rubber Ducky** |
> | Wi-Fi AP with same name as legitimate network | **Evil twin** |
> | Unauthorized AP plugged into internal network | **Rogue access point** |
> | Bluetooth data theft | **Bluesnarfing** |
> | Unsolicited Bluetooth messages | **Bluejacking** |
> | Compromising vendor to attack all its customers | **Supply chain / MSP vector** |
> | No more patches ever coming for a product | **End-of-life / unsupported system** |
>
> - Bluesnarfing vs bluejacking: snarfing = steals data. Jacking = sends messages. "Snarf" sounds like stealing.
> - Evil twin = attacker-controlled AP. Rogue AP = unauthorized AP connected to internal network (attacker or careless employee).

---

## 29. Vulnerability Types Expanded

### Application Vulnerabilities

| Term | What It Is |
|------|-----------|
| **Memory injection** | Attacker injects malicious code into a running process's memory space. DLL (Dynamic-Link Library) injection: forces a process to load a malicious DLL. Process injection: injects shellcode into a legitimate process (e.g., explorer.exe). Bypasses application whitelisting. |
| **Buffer overflow** | Writing more data to a buffer than it can hold, overwriting adjacent memory. Stack overflow: overwrites return address → redirects execution. Heap overflow: corrupts heap metadata → arbitrary code execution. Enables arbitrary code execution or crashes. |
| **Malicious update** | Compromising the software update mechanism to deliver malware as a trusted update. Users willingly install because it appears to be a legitimate patch. SolarWinds is the canonical example. |

### OS and Hardware Vulnerabilities

| Term | What It Is |
|------|-----------|
| **OS-based vulnerabilities** | Flaws in the operating system kernel, drivers, or core services. Exploited for privilege escalation, persistence, or lateral movement. Unpatched OS = permanent risk after end-of-life. |
| **Firmware vulnerabilities** | Bugs in low-level device firmware (UEFI/BIOS, router firmware, drive firmware). Can survive OS reinstallation. Firmware rootkits are extremely persistent. |
| **End-of-life hardware** | Hardware no longer receiving firmware or driver updates. Vulnerabilities discovered after EOL (End of Life) are never patched. |
| **Legacy hardware** | Older hardware that cannot support modern security controls (no TPM (Trusted Platform Module), no secure boot, no current OS). Risk cannot be fully mitigated. |

### Virtualization Vulnerabilities

| Term | What It Is |
|------|-----------|
| **VM escape** | Attacker breaks out of a VM (Virtual Machine) to access the hypervisor or other VMs on the same host. Crosses the virtualization boundary. Extremely serious — compromises all co-tenants. |
| **Resource reuse** | After a VM is deallocated or a container terminates, leftover data in memory or storage may be readable by the next tenant. Cloud-specific concern in shared infrastructure. |

### Cloud-Specific Vulnerabilities

| Term | What It Is |
|------|-----------|
| **Side-channel attack** | Extracts sensitive information by observing indirect system behavior — timing, power consumption, cache behavior — rather than attacking the algorithm directly. Especially relevant in shared cloud infrastructure where tenants share physical hardware (e.g., Spectre/Meltdown). |

### Cryptographic Vulnerabilities

| Term | What It Is |
|------|-----------|
| **Downgrade attack** | Forces a system to use a weaker protocol or cipher version (TLS 1.0 instead of TLS 1.3, SSL instead of TLS). Attacker manipulates the protocol negotiation handshake. POODLE and DROWN are classic examples. |
| **Collision attack** | Two different inputs that produce the same hash output. If found, integrity guarantees break. MD5 (Message Digest 5) is collision-vulnerable. SHA-1 (Secure Hash Algorithm 1) is deprecated for the same reason. |
| **Birthday attack** | Probability-based attack exploiting the birthday paradox: finding any two inputs with the same hash requires far fewer attempts than expected. The larger the hash output (SHA-256 vs MD5), the more resistant to birthday attacks. |

### Mobile Vulnerabilities

| Term | What It Is |
|------|-----------|
| **Sideloading** | Installing apps from outside the official app store (APK files on Android, .ipa files on iOS). Bypasses app store security review. Apps may contain malware or lack sandboxing controls. |
| **Jailbreaking / Rooting** | Removing manufacturer/OS restrictions to gain root access. iOS = jailbreaking. Android = rooting. Bypasses security controls: certificate pinning, sandboxing, MDM (Mobile Device Management) enforcement. |

### Zero-Day and Supply Chain Vulnerabilities

| Term | What It Is |
|------|-----------|
| **Zero-day** | A vulnerability unknown to the vendor with no patch available. "Day zero" = the day it's discovered is the same day exploitation is possible. High value to nation-states and organized crime. |
| **Supply chain — service provider** | Compromising a managed service, SaaS (Software as a Service), or cloud provider that many organizations depend on. One breach = many victims. |
| **Supply chain — hardware provider** | Malicious chips, firmware backdoors, or counterfeit components inserted during manufacturing or distribution. Very hard to detect. |
| **Supply chain — software provider** | Compromising a software vendor's build system or update server to distribute malware to all customers as a trusted update. |

> **Vulnerability Type Decision Rules:**
>
> | If the question describes... | Answer |
> |---|---|
> | Writing past a buffer boundary, redirecting execution | **Buffer overflow** |
> | Injecting code into a running legitimate process | **Memory injection / DLL injection** |
> | VM breaks out to hypervisor or host | **VM escape** |
> | Leftover data from previous VM/container tenant | **Resource reuse** |
> | Observing timing or cache behavior to extract crypto keys | **Side-channel attack** |
> | Forcing TLS 1.0 instead of TLS 1.3, POODLE | **Downgrade attack** |
> | Two inputs with the same hash output, MD5 weak | **Collision attack** |
> | Probability-based hash attack, birthday paradox | **Birthday attack** |
> | No patch exists yet, vendor unaware | **Zero-day** |
> | App installed from outside the official store | **Sideloading** |
> | Root access by removing OS restrictions | **Jailbreaking / Rooting** |
>
> - Downgrade vs on-path: downgrade manipulates protocol negotiation. On-path attack (MitM) intercepts content. Downgrade is often a prerequisite for a full on-path attack.
> - Collision vs birthday: a collision attack finds two specific inputs that collide. A birthday attack uses probability to find any collision faster than brute force.

---

## 30. Indicators of Malicious Activity

### Physical Attacks

| Term | What It Is |
|------|-----------|
| **Brute force (physical)** | Physically forcing entry — breaking locks, tailgating, ramming doors. No technical skill required. Bypasses logical controls entirely. |
| **RFID cloning** | Capturing RFID (Radio-Frequency Identification) signal from an access badge and copying it to a blank card. Attacker gains physical access using a cloned badge. |
| **Environmental attacks** | Targeting physical infrastructure: cutting power, manipulating temperature (data center cooling), flooding, or EMP (Electromagnetic Pulse) to destroy or disrupt systems. |

### Network Attacks

| Term | What It Is |
|------|-----------|
| **Amplified DDoS** | Attacker sends small requests to a third-party server that responds with a much larger reply — directed at the victim. DNS (Domain Name System) amplification: small query, large response. |
| **Reflected DDoS** | Spoofs victim's IP address in requests to legitimate servers. Servers send their responses to the victim, flooding it. Attacker never communicates with victim directly. |
| **DNS poisoning** | Corrupting a DNS (Domain Name System) server's cache to map a legitimate domain to a malicious IP. Victims are redirected without knowing. Also called DNS cache poisoning. |
| **DNS spoofing** | Broadly synonymous with DNS poisoning. Sometimes used to mean intercepting DNS queries in transit (on-path). |
| **DNS tunneling** | Encodes non-DNS data (C2 commands, exfiltrated data) inside DNS queries and responses. Bypasses firewalls that allow DNS. Hard to detect without DNS traffic analysis. |
| **Credential replay** | Capturing valid authentication credentials or tokens and retransmitting them to authenticate as the victim. Differs from brute force — no cracking needed. Countered by session tokens with short expiry and nonces. |
| **Protocol abuse** | Using legitimate protocols (HTTP, DNS, ICMP) for malicious purposes — C2 channels, data exfiltration, tunneling. Difficult to block without inspecting traffic content. |

### Application Attacks

| Term | What It Is |
|------|-----------|
| **Replay attack** | Capturing a valid data transmission (authentication request, session token) and retransmitting it to gain unauthorized access. Network-level version of credential replay. Countered by timestamps, nonces, and sequence numbers. |
| **Privilege escalation** | Gaining higher-level permissions than originally authorized. Vertical: user → admin. Horizontal: user → different user at same level. Exploits OS/application flaws or misconfigurations. |
| **Directory traversal** | Using `../` sequences in file paths to navigate outside the intended directory and access restricted files (e.g., `../../etc/passwd`). Related to LFI (Local File Inclusion) but specifically about path manipulation. |

### Behavioral Indicators of Malicious Activity

| Indicator | What It Signals |
|-----------|----------------|
| **Account lockout** | Multiple failed login attempts. May indicate password spraying or brute force against a specific account. |
| **Concurrent sessions** | Same account logged in from multiple geographic locations simultaneously. Often indicates credential theft or account sharing. |
| **Blocked content** | Security controls blocking unusual destinations or content categories — may indicate malware attempting C2 (Command and Control) communication. |
| **Impossible travel** | Account login from two geographically distant locations within a timeframe physically impossible to travel between. Strong indicator of credential compromise. |
| **Resource consumption** | Unusual CPU, memory, disk I/O, or bandwidth spike. May indicate cryptomining malware, data exfiltration, or ransomware encryption activity. |
| **Resource inaccessibility** | Systems or files suddenly unavailable. May indicate ransomware encrypting data, DoS (Denial of Service) attack, or destructive malware. |
| **Out-of-cycle logging** | Log entries appearing at unexpected times (3 AM, weekends) when normal users aren't active. May indicate automated attacker activity or insider misuse. |
| **Missing logs** | Gaps in log files or logs deleted. Common attacker anti-forensics behavior. Log deletion is a major red flag and should trigger immediate incident response. |
| **Published/documented indicators** | Threat intelligence feeds (IoC (Indicator of Compromise) databases, STIX (Structured Threat Information Expression)/TAXII (Trusted Automated Exchange of Intelligence Information), vendor bulletins) provide known-bad IPs, domains, file hashes. Matching these confirms compromise. |

> **DDoS Type Decision Rules:**
>
> | If the question describes... | Answer |
> |---|---|
> | Small request to third-party server generating large response directed at victim | **Amplified DDoS** |
> | Victim's spoofed IP receives responses from innocent third-party servers | **Reflected DDoS** |
> | Massive volume from many sources, no amplification mechanism | **Volumetric DDoS** |
>
> - Amplified and reflected often occur together (amplified reflection attack).
> - DNS amplification is the most common example: 1 query → 50x-100x response directed at victim.

> **Behavioral Indicator Decision Rules:**
>
> | If the question describes... | Answer |
> |---|---|
> | Login from New York at 8 AM, Tokyo at 9 AM | **Impossible travel** |
> | Same account active from three different IPs simultaneously | **Concurrent sessions** |
> | CPU at 100%, unusual outbound bandwidth, no user activity | **Resource consumption (cryptominer/exfiltration)** |
> | Log files empty or timestamps missing | **Missing logs (anti-forensics)** |
> | Activity at 3 AM on a weekend, no employees in | **Out-of-cycle logging** |
> | Files become encrypted and unreadable | **Resource inaccessibility (ransomware)** |

---

## 31. Mitigation Techniques Expanded

### Application Control

| Term | What It Is |
|------|-----------|
| **Application allow list** | Only pre-approved applications are permitted to execute. Everything else is blocked by default. Most restrictive, highest protection. Prevents unknown malware and unauthorized software. |
| **Application block list** | Known-bad applications are blocked. Everything else is allowed. Easier to manage but weaker — only stops known threats. |

### System and Network Mitigation

| Term | What It Is |
|------|-----------|
| **Isolation** | Separating a compromised, untrusted, or sensitive system from the rest of the network. Broader than IR (Incident Response) containment — includes network segmentation, air-gapping, sandbox isolation of suspicious files. |
| **Patching** | Applying vendor-released fixes for known vulnerabilities. Patch management process: inventory → test in staging → deploy → verify → document. Emergency patches (critical CVE) bypass normal schedule. |
| **Decommissioning** | Properly retiring end-of-life systems to eliminate attack surface. Includes: data wiping, certificate revocation, removing from network, updating asset inventory. Reduces exposure from unsupported systems. |
| **Configuration enforcement** | Continuously verifying and correcting system configurations against a known-good baseline. SCAP (Security Content Automation Protocol)/XCCDF (Extensible Configuration Checklist Description Format) benchmarks (CIS). Prevents configuration drift. |

### Host Hardening

| Term | What It Is |
|------|-----------|
| **Host-based firewall** | Firewall running on an individual endpoint (not a network device). Controls inbound/outbound traffic per host. Protects even when on a trusted internal network. Windows Defender Firewall, iptables. |
| **Host-based IPS** | IPS (Intrusion Prevention System) running as a software agent on an endpoint. Detects and blocks malicious behavior at the host level. Part of EDR (Endpoint Detection and Response) suites. |
| **Disabling ports/protocols** | Closing unnecessary network ports and disabling unused protocols (Telnet, FTP, SMBv1). Reduces attack surface by eliminating listening services that serve no business purpose. |
| **Default password changes** | Changing manufacturer-set credentials on all devices before deployment. Routers, switches, IoT (Internet of Things), servers. Default creds are publicly documented and scanned for by attackers. |
| **Removal of unnecessary software** | Uninstalling applications, services, and features not required for the system's function. Reduces attack surface and patch burden. Principle: minimum necessary software. |

> **Mitigation Technique Decision Rules:**
>
> | If the question asks how to... | Answer |
> |---|---|
> | Prevent unauthorized software from running | **Application allow list** |
> | Block known-bad applications | **Application block list** |
> | Protect an endpoint even inside the trusted network | **Host-based firewall** |
> | Stop attacks at the host level automatically | **Host-based IPS** |
> | Permanently reduce attack surface of legacy systems | **Decommissioning** |
> | Ensure configs match security baseline over time | **Configuration enforcement** |
> | Reduce attack surface from unused services | **Disabling ports/protocols + removing unnecessary software** |
>
> - Allow list vs block list: allow list is stronger but operationally harder. Pick allow list for high-security environments. Pick block list when you can't enumerate all legitimate software.
> - Decommissioning vs patching: patch if supported, decommission if end-of-life with no patch path.
> - Host-based firewall vs network IPS: host-based firewall controls traffic per endpoint. Network IPS sits inline on the network and protects all devices behind it.

---

## 32. Email Security

| Acronym/Term | Full Name | What It Does |
|---|---|---|
| **SPF** | Sender Policy Framework | DNS TXT record listing IP addresses authorized to send email for a domain. Validates the envelope sender. |
| **DKIM** | DomainKeys Identified Mail | Adds a cryptographic signature to email headers. Receiving server checks against sender's public DNS key to confirm message integrity. |
| **DMARC** | Domain-based Message Authentication, Reporting, and Conformance | Policy layer built on SPF + DKIM. Tells receivers what to do on auth failure (none / quarantine / reject) and enables aggregate reporting. |
| **Email gateway** | Secure Email Gateway | Inline appliance or cloud service that filters inbound/outbound email for spam, malware, and phishing before delivery. |

> **SPF vs DKIM vs DMARC — Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | DNS record listing authorized mail servers, envelope sender, IP list | **SPF** |
> | Cryptographic signature on email headers, message integrity, tamper detection | **DKIM** |
> | Policy for what to do on SPF/DKIM failure, quarantine, reject, reporting | **DMARC** |
> | Filters spam/malware/phishing before it reaches the inbox | **Email gateway** |
>
> - SPF says "only these IPs may send for my domain." DKIM says "I signed this message, check my DNS for the key." DMARC says "if SPF or DKIM fail, do THIS — and send me a report."
> - SPF and DKIM each solve part of the problem. DMARC requires both and enforces consequences for failure.
> - You can have SPF pass and DKIM pass yet still fail DMARC if the "From" header domain doesn't align.

---

## 33. Asset Management

| Acronym/Term | Full Name | What It Does |
|---|---|---|
| **Acquisition/procurement** | Secure Procurement | Vetting vendors, verifying supply chain integrity, and establishing security requirements before purchasing hardware or software. |
| **Asset tagging** | Asset Tagging | Attaching unique identifiers (barcodes, RFID, QR) to hardware assets for inventory and tracking. |
| **CMDB** | Configuration Management Database | Central repository tracking all IT assets, their configurations, and relationships. The authoritative asset inventory. |
| **Lifecycle tracking** | Asset Lifecycle Management | Monitoring assets from acquisition through deployment, maintenance, and disposal. |
| **Data sanitization** | Data Sanitization | Removing data from a device so it cannot be recovered before disposal or reuse. |
| **Overwrite/wipe** | Overwrite (Software Wipe) | Writes patterns of data over all storage sectors. Effective for functioning drives. |
| **Degaussing** | Degaussing | Applies a strong magnetic field to destroy data on magnetic media (HDDs, tapes). Renders media unusable. |
| **Cryptographic erase** | Cryptographic Erase | Deletes the encryption key for a self-encrypting drive. All data becomes unrecoverable ciphertext. Fast. |
| **Physical destruction** | Physical Destruction | Shredding, pulverizing, or incinerating media. The only guaranteed method. Used for SSDs and sensitive data. |
| **Certificate of destruction** | Certificate of Destruction | Document from a certified vendor confirming media was destroyed. Required for compliance and audit. |
| **Data retention policy** | Data Retention Policy | Defines how long data must be kept before destruction. Driven by regulations (e.g., HIPAA = 6 years). |
| **Legal hold** | Legal Hold | Suspends all data retention schedules and destruction. Overrides policy when litigation is anticipated. |

> **Sanitization Method Decision Rules:**
>
> | Scenario | Method |
> |---|---|
> | Functioning HDD, reuse within org | **Overwrite/wipe** |
> | Functioning HDD, transfer or disposal, no reuse of media needed | **Degaussing** (destroys media too) |
> | Self-encrypting drive (SED/SSD), fast, cryptographically secure | **Cryptographic erase** |
> | SSDs, NVMe, flash media with sensitive data | **Physical destruction** (overwrite not reliable on SSDs) |
> | Maximum assurance, classified, top secret | **Physical destruction** |
>
> - Degaussing does NOT work on SSDs or optical media. Only magnetic media.
> - Cryptographic erase is only valid if the drive was encrypted from day one. Post-hoc encryption doesn't retroactively protect old data.
> - Overwrite is NOT reliable for SSDs due to wear-leveling — data may persist in remapped sectors.

---

## 34. Common Ports and Secure Protocols

| Service | Insecure Port/Protocol | Secure Replacement | Port |
|---|---|---|---|
| **FTP** (File Transfer Protocol) | 21 | **SFTP** (SSH File Transfer Protocol) | 22 |
| **FTP** (File Transfer Protocol) | 21 | **FTPS** (FTP Secure / FTP over TLS) | 990 |
| **SSH** (Secure Shell) | — | **SSH** (already secure) | 22 |
| **Telnet** | 23 | **SSH** (Secure Shell) | 22 |
| **SMTP** (Simple Mail Transfer Protocol) | 25 | **SMTPS** / submission | 587 |
| **DNS** (Domain Name System) | 53 | **DoT** (DNS over TLS) / **DoH** (DNS over HTTPS) | 853 / 443 |
| **HTTP** (Hypertext Transfer Protocol) | 80 | **HTTPS** (HTTP Secure) | 443 |
| **POP3** (Post Office Protocol 3) | 110 | **POP3S** | 995 |
| **IMAP** (Internet Message Access Protocol) | 143 | **IMAPS** | 993 |
| **SNMP** (Simple Network Management Protocol) | 161 (queries) / 162 (traps) | SNMPv3 (encryption + auth) | 161/162 |
| **LDAP** (Lightweight Directory Access Protocol) | 389 | **LDAPS** | 636 |
| **RDP** (Remote Desktop Protocol) | 3389 | Use VPN + RDP or RD Gateway | 3389 |
| **Syslog** | 514 (UDP) | Syslog over TLS | 6514 |
| **Kerberos** | — | (already secure, ticket-based) | 88 |
| **RADIUS** (Remote Authentication Dial-In User Service) | — | 1812 (auth), 1813 (accounting) | 1812/1813 |
| **TACACS+** (Terminal Access Controller Access-Control System Plus) | — | TCP, full payload encryption | 49 |
| **NetBIOS** | 137–139 | Replace with DNS + SMB over TCP | — |
| **SMB** (Server Message Block) | 445 | SMB 3.x with encryption | 445 |
| **SQL Server** | — | 1433 (firewall-restrict) | 1433 |
| **MySQL** | — | 3306 (firewall-restrict) | 3306 |

> **Insecure → Secure Replacement Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Replace Telnet for remote admin | **SSH port 22** |
> | Replace FTP, keep same protocol family, add TLS wrapper | **FTPS port 990** |
> | Replace FTP, use SSH subsystem | **SFTP port 22** |
> | Replace HTTP | **HTTPS port 443** |
> | Replace POP3 | **POP3S port 995** |
> | Replace IMAP | **IMAPS port 993** |
> | Replace LDAP | **LDAPS port 636** |
> | Replace SMTP for sending | **SMTPS port 587** |
>
> - The pattern: add "S" (for Secure/SSL/TLS) and the port often changes. SFTP is the exception — it's SSH-based, not FTP+TLS.
> - SFTP (port 22) is NOT the same as FTPS (port 990). SFTP is SSH-subsystem. FTPS is FTP + TLS.
> - SNMPv1/v2 send community strings in cleartext. SNMPv3 adds authentication and encryption. Same port, different version.

---

## 35. Mobile Device Management

| Acronym/Term | Full Name | What It Does |
|---|---|---|
| **MDM** | Mobile Device Management | Centrally manages and enforces policy on mobile devices. |
| **Remote wipe** | Remote Wipe | Erases all data on a lost or stolen device via MDM command. |
| **Geofencing** | Geofencing | MDM policy triggered by device entering or leaving a geographic boundary. |
| **Containerization** | Mobile Containerization | Separates corporate apps/data from personal apps/data in an isolated encrypted container. |
| **BYOD** | Bring Your Own Device | Employee uses personally owned device for work. Org has limited control. |
| **COPE** | Corporate-Owned, Personally Enabled | Org owns the device, allows personal use. Full MDM control. |
| **CYOD** | Choose Your Own Device | Employee selects from an approved list of devices. Org owns or co-manages. |
| **Corporate-owned** | Corporate-Owned Only | Org owns and controls device, no personal use intended. Maximum control. |

> **MDM Capabilities Quick Reference:**
>
> | Capability | What It Enforces |
> |---|---|
> | Remote wipe | Erase on loss/theft |
> | Screen lock enforcement | PIN/biometric required |
> | Encryption enforcement | Storage must be encrypted |
> | App management (whitelist/blacklist) | Approved apps only |
> | Camera disable | Block camera in sensitive areas |
> | Geofencing | Restrict use by location |
> | Containerization | Separate work/personal data |

> **Deployment Model Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Employee's own device, partial org control, MDM limited | **BYOD** |
> | Org owns device, allows personal use, full MDM control | **COPE** |
> | Employee picks from approved options, org manages | **CYOD** |
> | Org owns, work-only, maximum control | **Corporate-owned** |
>
> - BYOD = least org control, lowest cost, highest risk. Corporate-owned = most org control, highest cost, lowest risk.
> - COPE = full control with personal use perk. Most common enterprise model.
> - The key distinguishing question: "Who owns the device?" Personal = BYOD. Org = COPE or Corporate-owned.

---

## 36. Automation and Orchestration

| Acronym/Term | Full Name | What It Does |
|---|---|---|
| **Automation** | Security Automation | Using scripts, tools, or platforms to perform repetitive security tasks without manual intervention. |
| **Orchestration** | Security Orchestration | Coordinating multiple automated tools and systems to execute a multi-step workflow. |
| **Guard rails** | Automated Guard Rails | Policy-as-code enforcement that prevents misconfiguration or policy violations before they happen. |
| **Runbook** | Runbook | Step-by-step automated procedure for a specific task (e.g., disable compromised account, create firewall rule). |
| **Playbook** | Security Playbook | Orchestrated workflow for a specific incident type. Coordinates tools automatically. Used in SOAR. |

> **Automation Use Cases:**
>
> | Use Case | What It Does |
> |---|---|
> | User provisioning / deprovisioning | Auto-create or disable accounts when triggered by HR system |
> | Resource provisioning | Spin up/tear down cloud resources via IaC on demand |
> | Guard rails | Block deployment of non-compliant infrastructure (e.g., unencrypted S3 buckets) |
> | Security group management | Auto-update firewall/cloud security group rules based on policy |
> | Ticket creation | Auto-open incident ticket when alert fires |
> | Escalation | Auto-escalate unacknowledged alerts to on-call engineer |
> | Enabling/disabling services and access | Lock account on detection of compromise without human delay |
> | CI/CD security testing | Run SAST/DAST/SCA scans automatically in the pipeline |
> | API integrations | Connect disparate tools (SIEM → ticketing → AD → firewall) |

> **Benefits of Automation and Orchestration:**
>
> | Benefit | Why It Matters |
> |---|---|
> | Efficiency / time saving | Removes manual, repetitive work from analyst load |
> | Enforcing baselines | Consistent policy application — no human variance |
> | Standard infrastructure configs | Every deployment uses the same hardened template |
> | Scaling securely | New resources provisioned with security built in, no manual setup |
> | Reaction time | Response in seconds vs. hours for human-driven processes |
> | Workforce multiplier | One analyst can manage far more alerts with automation support |
> | Employee retention | Reduces burnout from low-value repetitive tasks |

### Other Considerations

| Consideration | What It Means |
|---------------|--------------|
| **Complexity** | Automation adds system dependencies. More integration points = more potential failure modes. Keep automations simple and well-documented. |
| **Cost** | Automation tools (SOAR platforms, IaC tools, custom scripts) require licensing, development, and maintenance investment. |
| **Single point of failure** | Over-reliance on one automation platform means if it goes down, all automated workflows stop. Design redundancy. |
| **Technical debt** | Hastily built automations accumulate technical debt. Scripts break when APIs change. Regular maintenance required. |
| **Ongoing supportability** | Automated systems need staff who understand them. If the person who built the automation leaves, can others maintain it? |

> **SOAR vs Automation vs Orchestration:**
>
> - Automation = a single tool does a task automatically.
> - Orchestration = coordinating multiple tools in a sequence.
> - SOAR (Security Orchestration, Automation, and Response) = platform that does both, with playbooks, for IR workflows.
> - "SOAR" is the specific product category. "Automation and orchestration" is the broader capability they provide.

---

## 37. Investigation Data Sources

| Acronym/Term | Full Name | What It Does |
|---|---|---|
| **Firewall logs** | Firewall Logs | Record allowed/denied connection attempts (source/dest IP, port, protocol). First stop for network investigation. |
| **Application logs** | Application Logs | Application-generated records of events, errors, and user actions. Captures app-layer behavior. |
| **Endpoint logs** | Endpoint Logs | Activity logs from individual hosts (process execution, file access, registry changes). EDR source. |
| **Windows Event Log** | Windows Event Log | Windows OS audit log. Key event IDs: 4624 (logon success), 4625 (logon failure), 4688 (process created), 4648 (explicit credential use). |
| **Syslog** | System Log | Unix/Linux standard logging protocol. Sends log data to a central log server (port 514/UDP or 6514/TLS). |
| **journald** | systemd Journal Daemon | Modern Linux log manager (part of systemd). Structured binary logs, queried with `journalctl`. |
| **IPS/IDS logs** | IPS/IDS Logs | Alerts on detected attack signatures and anomalies. Contains signature names, severity, source/dest. |
| **Network logs** | Network Logs | Traffic metadata from routers, switches, proxies. Includes flow records and connection attempts. |
| **pcap** | Packet Capture | Full packet content captured by tools like Wireshark or tcpdump. Enables deep traffic inspection. |
| **NetFlow** | NetFlow | Network traffic metadata: source/dest IP, ports, protocol, bytes, duration. Flow summary — not full packet content. |
| **sFlow** | Sampled Flow | Like NetFlow but uses statistical sampling. Lower overhead, less granular. |
| **IPFIX** | IP Flow Information Export | IETF standard version of NetFlow. The open-standard successor. |
| **SNMP traps** | Simple Network Management Protocol Traps | Devices push unsolicited alerts to the management station when a threshold is breached. |
| **Email headers** | Email Metadata | Reveal routing path, originating IP, timestamps, authentication results (SPF/DKIM/DMARC). |
| **File metadata** | File Properties | Timestamps (created/modified/accessed), author, file size, location. Used in forensics. |
| **Vulnerability scan results** | Vulnerability Scan Output | Report of identified vulnerabilities per host, with CVE IDs and severity. Baseline for remediation. |
| **Dashboard** | Security Dashboard | Visual aggregation of metrics and alerts. Real-time status view from SIEM or monitoring platform. |

> **Log Source Decision Rules:**
>
> | Investigation Scenario | Best Source |
> |---|---|
> | "Who logged in to what server and when?" | **Windows Event Log** (Event ID 4624) or **endpoint logs** |
> | "What traffic passed through the firewall?" | **Firewall logs** |
> | "Was there an attack against the web server?" | **Application logs** + **WAF logs** |
> | "What is the network traffic pattern between these hosts?" | **NetFlow / IPFIX** |
> | "What exactly was in the malicious packet?" | **pcap / Wireshark** |
> | "Did any network device alert on an attack?" | **IPS/IDS logs** |
> | "Which devices are sending SNMP alerts?" | **SNMP traps** |
> | "Where did this email really come from?" | **Email headers** |
>
> - NetFlow = flow metadata (who talked to whom). pcap = full packet content (what they said). NetFlow is fast to search; pcap is the full record.
> - SNMP traps are PUSH (device notifies manager). SNMP polling is PULL (manager asks device). Traps are for threshold alerts.
> - Syslog is the transport. The application log is the content. They're different layers.

---

## 38. Web Filtering

| Acronym/Term | Full Name | What It Does |
|---|---|---|
| **Agent-based filtering** | Endpoint Web Filtering Agent | Software installed on the endpoint that filters web traffic locally, regardless of network location. Effective for remote/roaming users. |
| **Centralized proxy** | Centralized Web Proxy | All web traffic routes through a proxy server for inspection, filtering, and logging. Single enforcement point for on-prem users. |
| **URL scanning** | URL Reputation Scanning | Checks requested URLs against threat intelligence databases to block known-malicious addresses. |
| **Content categorization** | Content Categorization | Classifies websites by type (social media, gambling, adult, malware) to apply category-based block policies. |
| **Block rules** | Block Rules | Administrator-defined allow/deny rules for specific domains, URLs, or categories. |
| **Reputation-based filtering** | Reputation-Based Filtering | Scores sites based on historical behavior, domain age, and threat history. Blocks low-reputation sites. |
| **DNS filtering** | DNS Filtering | Blocks resolution of known-bad domain names at the DNS layer. Prevents connection before it starts. |

> **Web Filtering Method Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Remote/roaming users, works off-network, software on device | **Agent-based filtering** |
> | All traffic routes through one point, on-prem, central logging | **Centralized proxy** |
> | Blocks domains before DNS resolves them, simplest enforcement | **DNS filtering** |
> | Blocks by site reputation score, threat history, domain age | **Reputation-based filtering** |
> | Blocks entire category (social media, gambling) | **Content categorization + block rules** |
>
> - Agent-based works when the device leaves the corporate network. Centralized proxy loses control when users go off-prem (unless combined with VPN).
> - DNS filtering is the fastest and cheapest to implement but only blocks at the domain level — not specific URLs or page content.
> - SWG (Secure Web Gateway) is a product that combines centralized proxy + URL scanning + content categorization + reputation filtering in one solution.

---

## 39. Vulnerability Management Expanded

| Acronym/Term | Full Name | What It Does |
|---|---|---|
| **White box pen test** | Known-Environment Penetration Test | Tester has full knowledge of the environment (architecture, source code, credentials). SY0-701 term: "known environment." |
| **Gray box pen test** | Partially Known Environment Penetration Test | Tester has partial knowledge (e.g., knows IP ranges, not internal architecture). SY0-701 term: "partially known environment." |
| **Black box pen test** | Unknown-Environment Penetration Test | Tester has no prior knowledge. Simulates external attacker. SY0-701 term: "unknown environment." |
| **Bug bounty** | Bug Bounty Program | Organization pays external researchers for responsibly disclosing security vulnerabilities. Crowd-sourced security testing. |
| **True positive** | True Positive (TP) | Scanner reports a vulnerability that actually exists. Correct detection. |
| **False positive** | False Positive (FP) | Scanner reports a vulnerability that does NOT exist. Alert fatigue; requires tuning. |
| **True negative** | True Negative (TN) | Scanner reports no vulnerability, and none exists. Correct non-detection. |
| **False negative** | False Negative (FN) | Scanner misses a vulnerability that actually exists. Most dangerous — undetected risk. |
| **Compensating control** | Compensating Control | Alternative security measure used when the primary control cannot be applied (e.g., legacy system can't be patched → network isolation). |
| **Exception** | Vulnerability Exception | Documented acknowledgment that a vulnerability will not be remediated, with justification and owner sign-off. Temporary. |
| **Exemption** | Vulnerability Exemption | Permanent or long-term acknowledgment that a system is excluded from a control requirement, with formal approval. |
| **Cyber insurance** | Cyber Liability Insurance | Transfers residual financial risk of a cyber incident to an insurer. Risk transference control. |
| **Rescanning** | Validation Rescan | Re-running the vulnerability scan after remediation to confirm the vulnerability is gone. |

> **Pen Test Environment Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Full knowledge — source code, architecture, credentials provided | **Known environment (white box)** |
> | Some information — IP ranges or user credentials, not full design | **Partially known environment (gray box)** |
> | No prior information — simulate external attacker from scratch | **Unknown environment (black box)** |
>
> - SY0-701 uses "known / partially known / unknown environment" — NOT "white/gray/black box." Know both but expect the exam to use the new terms.
> - Unknown environment (black box) = most realistic attacker simulation. Known environment (white box) = most thorough coverage.

> **Scan Result Interpretation:**
>
> | Result | Real Vuln? | Detected? | Impact |
> |---|---|---|---|
> | True Positive | YES | YES | Correct — act on it |
> | False Positive | NO | YES | Wasted effort — tune scanner |
> | True Negative | NO | NO | Correct — no action |
> | False Negative | YES | NO | DANGEROUS — missed risk |
>
> - False negatives are more dangerous than false positives. An undetected real vuln is an open door.

> **Remediation Options in Order of Preference:**
>
> 1. **Patch** — fix the vulnerability directly
> 2. **Compensating control** — mitigate risk when patching isn't possible
> 3. **Exception/Exemption** — document accepted risk, formal approval required
> 4. **Cyber insurance** — transfer residual financial risk

---

## 40. Incident Response Expanded

| Acronym/Term | Full Name | What It Does |
|---|---|---|
| **Tabletop exercise** | Tabletop Exercise | Discussion-based IR rehearsal. No systems touched. Team talks through response to a scenario. Tests plans and communication. |
| **Simulation** | IR Simulation | Hands-on exercise using real or realistic systems. Simulates an actual incident to test technical response capability. |
| **Root cause analysis** | Root Cause Analysis (RCA) | Post-incident investigation to determine the underlying reason the incident occurred, not just what happened. Feeds lessons learned. |
| **Internal reporting** | Internal Incident Reporting | Notifying management, legal counsel, HR, and other internal stakeholders per the IR plan. |
| **External reporting** | External Incident Reporting | Mandatory notification to regulators, law enforcement, affected individuals, or media depending on breach type and jurisdiction. |
| **Breach notification** | Breach Notification | Legal requirement to notify affected parties after a data breach. GDPR: 72 hours. HIPAA: 60 days. |
| **Stakeholder management** | Stakeholder Management | Coordinating communication to internal and external parties throughout an incident. Manages expectations and legal obligations. |

> **Training Type Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Discussion-based, no real systems, talk through the scenario, test the plan | **Tabletop exercise** |
> | Hands-on, real or realistic environment, technical practice | **Simulation** |
> | Determine why the incident happened, prevent recurrence | **Root cause analysis** |
>
> - Tabletop = cheapest, most common, tests communication and process. No technical execution.
> - Simulation = tests actual technical capability. More expensive, requires preparation.
> - RCA is a post-incident activity, not a training type — but it's tested in the 4.8 objective.

> **External Reporting Triggers:**
>
> | Situation | Who to Notify |
> |---|---|
> | PII or PHI breach | Affected individuals + regulators (HHS for HIPAA, DPA for GDPR) |
> | Criminal activity (ransomware, fraud) | Law enforcement (FBI, CISA) |
> | Publicly traded company breach | SEC (Securities and Exchange Commission), shareholders |
> | Critical infrastructure attack | CISA (Cybersecurity and Infrastructure Security Agency) |
> | Media inquiry | Communications team, then media (controlled disclosure) |

---

## 41. Monitoring Activities Expanded

| Acronym/Term | Full Name | What It Does |
|---|---|---|
| **Alert tuning** | Alert Tuning | Adjusting alert thresholds, filters, and rules to reduce false positives without increasing false negatives. Ongoing process. |
| **Quarantine** | Security Quarantine | Isolating a suspicious file, email, or system from the rest of the environment pending investigation. |
| **Archiving** | Log Archiving | Long-term storage of logs for compliance, forensics, and historical analysis. Retention period driven by regulation. |
| **Signature-based AV** | Signature-Based Antivirus | Compares files against a database of known malware signatures. Fast but blind to new/unknown threats. |
| **Heuristic AV** | Heuristic Antivirus | Analyzes code structure and behavior patterns to detect malware without a known signature. Catches variants. |
| **Behavioral AV** | Behavioral Antivirus | Monitors running processes for malicious actions (file encryption, registry modification, network scanning). Catches zero-days in action. |
| **Scheduled reports** | Scheduled Security Reports | Pre-configured reports generated at regular intervals (daily/weekly/monthly) for management and compliance. |
| **Ad-hoc reports** | Ad-Hoc Reports | On-demand reports generated in response to a specific question or incident. |
| **Compliance reporting** | Compliance Reporting | Reports demonstrating adherence to regulatory requirements (PCI DSS quarterly scans, SOX controls). |

> **Antivirus Detection Method Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Known malware, hash match, signature database | **Signature-based** |
> | No known signature, code analysis, detects variants | **Heuristic** |
> | Monitors running process behavior, catches zero-days in action | **Behavioral** |
>
> - Signature-based is fastest but misses new threats (zero-days, polymorphic malware).
> - Behavioral detection has the highest false positive rate but is best for unknown threats.
> - Modern AV combines all three layers.

> **Alert Tuning Goal:**
>
> - Reduce false positives → raise threshold or add exceptions → risk: may increase false negatives
> - Reduce false negatives → lower threshold → risk: may increase false positives
> - The goal is balance: catch real threats without drowning analysts in noise
> - Document all tuning changes — untuned alerts are a compliance finding in many frameworks

---

## 42. Security Governance

### Document Hierarchy

| Term | What It Is |
|------|-----------|
| **Policy** | Mandatory, high-level statements of organizational intent. Senior leadership sets these. Non-compliance has consequences. (e.g., "All sensitive data must be encrypted.") |
| **Standard** | Specific, mandatory requirements for implementing a policy. Defines HOW policy is met with measurable criteria. (e.g., "AES-256 must be used for data at rest.") |
| **Procedure** | Step-by-step instructions for completing a specific task. Mandatory, operational. (e.g., "How to grant a new employee network access.") |
| **Guideline** | Recommendations and best practices. NOT mandatory — users may use judgment to deviate. (e.g., "It is recommended to use a password manager.") |

> **Policy vs Standard vs Procedure vs Guideline — Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | "Mandatory," "organizational intent," "senior leadership," high-level "must" statement | **Policy** |
> | Specific requirements, measurable criteria, "how the policy is implemented," technical specs | **Standard** |
> | Step-by-step, "how to," operational instructions, checklist | **Procedure** |
> | "Recommended," "best practice," optional, "should" not "must" | **Guideline** |
>
> - Policies and standards are BOTH mandatory. Guidelines are NEVER mandatory.
> - Hierarchy: Policies define the WHAT → Standards define the HOW (measurable) → Procedures define the STEPS → Guidelines offer suggestions.

### Key Policy Types

| Policy | What It Governs |
|--------|----------------|
| **Information security policy** | Overarching policy covering the organization's approach to protecting information assets. Parent document for all other security policies. |
| **Acceptable Use Policy (AUP)** | Defines permitted and prohibited use of organizational systems and resources. Signed during employee onboarding. |
| **Business continuity policy** | Mandates the organization maintain operations during disruption. Governs who authorizes the BCP (Business Continuity Plan) and triggers activation. |
| **Disaster recovery policy** | Mandates restoration of IT systems after disaster. Defines RTO (Recovery Time Objective) and RPO (Recovery Point Objective) thresholds. |
| **Incident response policy** | Establishes authority, escalation, and communication framework for handling security incidents. Who can declare an incident, who must be notified. |
| **SDLC (Software Development Lifecycle) policy** | Mandates security integration at each development phase. Includes secure coding standards, code review, and testing requirements. |
| **Change management policy** | Requires all changes to systems go through a formal approval process. Prevents unauthorized modifications. |

### Key Standards

| Standard Type | What It Specifies |
|---------------|------------------|
| **Password standards** | Minimum length, complexity requirements, password history (no reuse), maximum age/expiration, and lockout thresholds. |
| **Access control standards** | Which access control model applies to which systems, minimum privilege requirements, review frequency. |
| **Physical security standards** | Badge access requirements, visitor log procedures, surveillance coverage, mantrap deployment, clean desk policy. |
| **Encryption standards** | Which algorithms are approved (e.g., AES-256 for data at rest, TLS 1.2+ for data in transit), key length minimums. |

### Key Procedures

| Procedure | What It Covers |
|-----------|---------------|
| **Onboarding** | Steps for granting system access, issuing credentials, collecting signed AUP (Acceptable Use Policy), provisioning accounts when an employee joins. |
| **Offboarding** | Steps for revoking all access, disabling accounts, recovering equipment, and preserving data when an employee leaves. |
| **Change management procedure** | Formal steps: submit change request → CAB (Change Advisory Board) review → approval → scheduled maintenance window → implement → test → document. Includes rollback plan. |
| **Playbook** | Step-by-step IR (Incident Response) procedure for a specific threat scenario. Operationalizes the incident response policy. |

### External Considerations

| Category | Examples | Impact on Governance |
|----------|----------|---------------------|
| **Regulatory** | GDPR (General Data Protection Regulation), HIPAA (Health Insurance Portability and Accountability Act), PCI DSS (Payment Card Industry Data Security Standard), SOX (Sarbanes-Oxley Act) | Mandatory compliance. Non-compliance = fines, sanctions. |
| **Legal** | Jurisdiction-specific laws, e-discovery requirements, legal hold obligations, liability standards | Legal hold must suspend normal data retention. Governs evidence preservation. |
| **Industry** | Sector-specific standards (e.g., NERC CIP (North American Electric Reliability Corporation Critical Infrastructure Protection) for power, SWIFT CSP (Customer Security Programme) for banking) | Often voluntary but become mandatory for market access. |
| **Local/regional** | State-level laws (e.g., CCPA — California Consumer Privacy Act), regional frameworks | May be more restrictive than national law. |
| **National** | Country-level laws (US FISMA — Federal Information Security Management Act, UK Cyber Essentials) | Jurisdiction determines which laws apply. |
| **Global** | Multi-national obligations, import/export controls (EAR — Export Administration Regulations, ITAR — International Traffic in Arms Regulations) | Products, software, and crypto algorithms may have export restrictions. |

### Policy Monitoring and Revision

| Concept | What It Means |
|---------|--------------|
| **Policy lifecycle** | Policies are created, approved, published, maintained, reviewed, revised, and retired — they are not static documents. |
| **Periodic review** | Policies should be reviewed on a scheduled cadence (commonly annually) to verify they remain accurate and relevant. |
| **Revision triggers** | Events that prompt out-of-cycle policy updates: new regulations, security incidents, technology changes, audit findings, organizational restructuring. |

### Governance Structures

| Structure | What It Is |
|-----------|-----------|
| **Board of directors** | Highest governance body. Sets organizational risk appetite and holds executive leadership accountable for security posture. |
| **Security committee** | Cross-functional body (IT, legal, HR, business) that makes security decisions, reviews policy, and oversees risk. |
| **Government entities** | Regulatory bodies (e.g., SEC — Securities and Exchange Commission, FTC — Federal Trade Commission) that impose compliance obligations and enforcement. |
| **Centralized governance** | Single authority makes all security decisions. Consistent policy enforcement. Less flexible but easier to audit. |
| **Decentralized governance** | Business units make local security decisions within a broad framework. More flexible, harder to maintain consistency. |

---

## 43. Risk Management Expanded

### Risk Identification Methods

| Method | How It Works |
|--------|-------------|
| **Brainstorming** | Structured group sessions to enumerate potential threats. Leverages collective experience. |
| **Interviews** | Subject matter experts queried individually to identify risks specific to their area. |
| **Historical data** | Past incidents, near-misses, and industry data used to identify likely future risks. |
| **Threat modeling** | Systematic analysis of system design to identify attack surfaces and potential threats before implementation. |

### Risk Assessment Types

| Type | When Used |
|------|----------|
| **Ad hoc** | Triggered by a specific event, change, or concern. Unscheduled, reactive. (e.g., after a vendor breach announcement) |
| **Recurring** | Scheduled assessments at regular intervals (quarterly, annually). Ongoing program. |
| **One-time** | Single assessment for a specific project or acquisition. Not repeated. |
| **Continuous** | Real-time or near-real-time risk monitoring. Automated tooling. Reflects current state. |

### Risk Tracking Tools

| Tool | What It Is |
|------|-----------|
| **Risk register** | Document (or database) listing all identified risks, their likelihood, impact, risk owner, current controls, and mitigation status. The master inventory of organizational risk. |
| **Risk matrix** | Grid plotting likelihood on one axis and impact on the other. Each cell represents a risk level. Qualitative prioritization tool. |
| **Risk heat map** | Visual version of the risk matrix. Uses color coding (red/yellow/green) to show concentration of high-risk areas at a glance. |
| **KRI (Key Risk Indicator)** | Metric that signals rising risk BEFORE an incident occurs. Leading indicator. (e.g., patch rate below 90% = elevated breach risk) |

### Risk Appetite vs Risk Tolerance

| Concept | Definition |
|---------|-----------|
| **Risk appetite** | How much risk the organization WANTS to take to achieve its objectives. Strategic, set by leadership. "We are willing to accept X level of risk." |
| **Risk tolerance** | How much risk the organization CAN accept — the acceptable variation around risk appetite. Operational boundary. |
| **Risk threshold** | The specific point at which risk exceeds tolerance and requires escalation or action. |

> **Risk Appetite Postures — Decision Rules:**
>
> | Posture | Description | When Exam Uses It |
> |---------|-------------|------------------|
> | **Expansionary** | Aggressive growth orientation. Higher risk accepted for competitive advantage. Startups, high-growth companies. | "Prioritize innovation over security controls," "accept higher risk for market speed" |
> | **Conservative** | Risk-averse. Stability and compliance over growth. Prefers proven approaches, minimal risk. Banks, healthcare, government. | "Minimize exposure," "prefer lower risk even at cost of opportunity" |
> | **Neutral** | Balanced. Accepts moderate risk proportional to reward. Most enterprises. | "Balance risk and reward," "moderate risk acceptance" |

### Risk Management Strategies

| Strategy | What It Means | Example |
|----------|--------------|---------|
| **Transfer** | Shift financial impact to a third party. Does NOT eliminate the risk. | Cyber liability insurance, outsourcing to a vendor who accepts liability |
| **Accept** | Acknowledge the risk exists and choose to live with it. Must be documented. | Deciding not to patch an isolated legacy system after cost-benefit analysis |
| **Avoid** | Eliminate the activity that creates the risk entirely. | Canceling a project that introduces unacceptable risk |
| **Mitigate** | Reduce the likelihood or impact of the risk. Most common strategy. | Patching, adding MFA (Multi-Factor Authentication), implementing controls |

> **Exemption vs Exception:**
>
> | Term | What It Means |
> |------|--------------|
> | **Exception** | Temporary, conditional deviation from a policy. Time-limited, requires approval, must be documented. (e.g., "Legacy system cannot meet password complexity — exception approved for 90 days while migration occurs.") |
> | **Exemption** | Permanent exclusion from a policy requirement. Granted when a policy provision structurally cannot apply. Requires senior approval. |
>
> - Exception = temporary. Exemption = permanent.
> - Both require documentation and approval. Neither means "ignore the policy."

> **Risk Strategy Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Insurance, outsource liability, third party absorbs financial loss | **Transfer** |
> | "We acknowledge and document," cost exceeds benefit, residual risk | **Accept** |
> | "We will not perform this activity," eliminate the source | **Avoid** |
> | Add controls, patch, implement safeguards, reduce likelihood or impact | **Mitigate** |
>
> - Transfer does NOT remove the risk — it shifts the financial consequence.
> - Accept requires documentation. Never just "ignore it."

### Risk Reporting

| Concept | What It Involves |
|---------|----------------|
| **Risk reporting** | Communicating risk status to stakeholders. Internal: board, executive team, risk committee. External: regulators, auditors, investors (as required). |
| **Risk dashboard** | Visual summary of current risk posture against appetite/tolerance thresholds. |

---

## 44. Third-Party Risk Management Expanded

### Vendor Assessment Methods

| Method | What It Is |
|--------|-----------|
| **Penetration testing of vendor** | Org or authorized third party tests the vendor's systems for vulnerabilities. Requires explicit authorization and rules of engagement. |
| **Right-to-audit clause** | Contractual provision allowing the organization to audit the vendor's security controls at any time. Included in vendor contracts during negotiation. |
| **Evidence of internal audits** | Vendor provides results of their own internal audit program as proof of ongoing compliance. Self-reported. |
| **Independent assessments** | Third-party auditor (not the org, not the vendor) evaluates the vendor's controls. Most objective. SOC 2 (Service Organization Control Type 2) Type II is an example. |
| **Supply chain analysis** | Evaluating the security of the vendor's own suppliers and sub-processors — the full upstream chain, not just the vendor themselves. |
| **Security questionnaire** | Standardized set of questions sent to vendor to assess their security posture. SIG (Standardized Information Gathering) and CAIQ (Consensus Assessments Initiative Questionnaire) are common frameworks. |

### Rules of Engagement

| Concept | What It Covers |
|---------|---------------|
| **Rules of engagement** | Formal document defining the scope, boundaries, permitted activities, timing, and notification requirements for a security assessment. Signed before any testing begins. Protects both parties. |
| **Scope** | Which systems, networks, and applications are in-scope for testing. |
| **Authorized activities** | What the assessor is permitted to do (e.g., scanning, exploitation, social engineering — each explicitly authorized or excluded). |

### Vendor Monitoring

| Activity | What It Involves |
|----------|----------------|
| **Ongoing monitoring** | Continuous or periodic review of vendor security posture after contract award. Not a one-time assessment. |
| **Performance metrics** | Measuring vendor against SLA (Service Level Agreement) terms and security KPIs (Key Performance Indicators). |
| **Compliance verification** | Confirming vendor maintains required certifications and controls over time (e.g., annual SOC 2 reports). |

### Vendor Selection

| Activity | What It Involves |
|----------|----------------|
| **Due diligence** | Research conducted BEFORE selecting a vendor. Evaluating security posture, financial stability, reputation, and compliance status. |
| **Conflict of interest** | Ensuring vendor selection decisions are made objectively, without personal relationships or financial interests influencing the outcome. |
| **Minimum security requirements** | Baseline security controls a vendor MUST meet to be eligible for selection. Non-negotiable thresholds. |

### Supply Chain Risks

| Risk Category | Specific Threats |
|---------------|----------------|
| **Hardware providers** | Tampered or counterfeit components inserted during manufacturing or shipping. Malicious firmware pre-installed. Difficult to detect after deployment. |
| **Software providers** | Compromised software updates pushing malware to customers (e.g., SolarWinds-style supply chain attack). Malicious code in legitimate packages. |
| **Managed service providers (MSPs)** | MSP (Managed Service Provider) has broad access to client networks. Compromise of MSP infrastructure grants attacker access to all managed clients simultaneously. |

> **Vendor Assessment Method Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | "Contractual right to review vendor controls," negotiate into contract | **Right-to-audit clause** |
> | Org hires third party to test vendor's systems | **Penetration testing (of vendor)** |
> | Vendor submits their own audit findings | **Evidence of internal audits** |
> | Independent auditor evaluates vendor, SOC 2 Type II report | **Independent assessment** |
> | Standardized questionnaire, SIG, CAIQ | **Security questionnaire** |
> | Review of vendor's own upstream suppliers | **Supply chain analysis** |

---

## 45. Security Compliance

### Compliance Monitoring

| Concept | What It Means |
|---------|--------------|
| **Due diligence** | Research and investigation performed BEFORE a decision or action. Proactive. Identifying risks before entering a relationship. "We evaluated their security controls before signing the contract." |
| **Due care** | Ongoing responsibility and reasonable action AFTER a decision. Reactive maintenance. "We continue to monitor and enforce controls throughout the relationship." |
| **Attestation** | Formal written declaration that controls exist and function as described. Required by many compliance frameworks. Management signs off that they have reviewed and the statements are accurate. |
| **Acknowledgement** | User or employee confirms (typically in writing) they have read, understood, and agree to comply with a policy. AUP (Acceptable Use Policy) sign-off is a form of acknowledgement. |
| **Internal monitoring** | Organization monitors its own compliance posture through internal audits, self-assessments, and control testing. |
| **External monitoring** | Third parties (regulators, auditors, customers) monitor organization's compliance through audits, certifications, and reporting requirements. |
| **Compliance automation** | Use of tools to continuously check configurations, access controls, and policies against compliance requirements. Reduces manual audit burden. |

> **Due Diligence vs Due Care — Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | "Before selecting," "prior to signing," research phase, vendor evaluation | **Due diligence** |
> | "Ongoing," "after implementation," "continuing responsibility," "monitoring," "maintaining" | **Due care** |
>
> - Due diligence = BEFORE. Due care = AFTER and ONGOING.
> - Failing due diligence = negligence for not researching. Failing due care = negligence for not maintaining.

### Privacy Compliance

| Concept | What It Means |
|---------|--------------|
| **Data subject** | The individual whose personal data is being collected, processed, or stored. The person the data is ABOUT. GDPR (General Data Protection Regulation) gives data subjects rights over their own data. |
| **Data inventory** | A catalog of all personal data the organization collects, stores, and processes — what data, where it lives, how long it's kept, who has access. Foundation for compliance. |
| **Data retention** | Policies defining how long different categories of data are kept before secure deletion. Balances business need, legal requirement, and privacy obligation. |
| **Right to be forgotten** | GDPR (General Data Protection Regulation) right allowing data subjects to request deletion of their personal data when it is no longer necessary for its original purpose. Also called "right to erasure." |

### Compliance Reporting

| Type | What It Covers |
|------|---------------|
| **Internal reporting** | Reports to board, executive management, risk committee, and audit committee on compliance posture, control gaps, and remediation status. |
| **External reporting** | Reports to regulators, external auditors, customers (as required by contract), and the public (breach notifications). Driven by legal and regulatory obligations. |

### Consequences of Non-Compliance

| Consequence | Description |
|-------------|-------------|
| **Fines** | Financial penalties imposed by regulators. GDPR (General Data Protection Regulation): up to 4% of global annual revenue. PCI DSS (Payment Card Industry Data Security Standard): monthly fines. |
| **Sanctions** | Regulatory restrictions on business operations. May include bans on processing certain data types or operating in specific markets. |
| **Reputational damage** | Loss of customer trust, negative press coverage, and reduced market position following a public compliance failure or breach. |
| **Loss of license** | Revocation of the legal authority to operate in a regulated industry (e.g., financial services, healthcare). Severe — can end the business. |
| **Contractual impacts** | Breach of contract with customers, partners, or vendors who required compliance as a contract term. May result in contract termination or civil liability. |

---

## 46. Audits and Assessments

### Attestation

| Concept | What It Means |
|---------|--------------|
| **Attestation** | A formal declaration by management or a qualified auditor that controls exist, are properly designed, and operate effectively. Written sign-off. "We attest that our controls meet the stated requirements." |

### Internal Audits

| Type | What It Involves |
|------|----------------|
| **Compliance audit (internal)** | Internal team evaluates whether the organization is adhering to its own policies and applicable regulatory requirements. |
| **Audit committee** | Board-level or senior management committee that oversees the internal audit function, reviews findings, and ensures independence of auditors from the teams they audit. |
| **Self-assessment** | Business unit or system owner evaluates their own controls against a standard. Less rigorous than independent audit — more frequent, lower cost. Used as a control testing mechanism between full audits. |

### External Audits

| Type | What It Involves |
|------|----------------|
| **Regulatory audit** | Audit conducted by or required by a government regulator (e.g., HIPAA (Health Insurance Portability and Accountability Act) audit by HHS, PCI DSS (Payment Card Industry Data Security Standard) audit required by card brands). |
| **Examination** | Formal review by a regulatory body, often without advance notice. Common in financial services (bank examiners). More authoritative than an assessment. |
| **Assessment** | Evaluation of controls against a framework or standard, typically by an external party. May or may not result in a formal certification. Risk-focused. |
| **Independent third-party audit** | Audit performed by a qualified external firm with no relationship to the organization. Most credible form — no conflict of interest. SOC 2 (Service Organization Control Type 2) Type II is the most common example in security. |

### Penetration Testing

| Term | What It Means |
|------|--------------|
| **Physical penetration testing** | Attempts to gain unauthorized physical access to facilities — lock picking, tailgating, badge cloning, social engineering security personnel. Tests physical controls. |
| **Offensive (red team)** | Simulates real-world attacker behavior. Attempts to achieve a defined objective (e.g., access to sensitive data) using any available technique. Tests detection AND prevention. |
| **Defensive (blue team)** | Detects, responds to, and contains simulated attacks. Evaluates the effectiveness of monitoring, alerting, and IR (Incident Response) processes. |
| **Integrated (purple team)** | Red team and blue team work collaboratively in real time. Red team shares TTPs (Tactics, Techniques, and Procedures) as they execute; blue team improves detection simultaneously. Maximum learning. |
| **Known environment** | Tester is given full information: network diagrams, source code, credentials, system architecture. Formerly called "white box." Most thorough — no time wasted on reconnaissance. |
| **Partially known environment** | Tester is given limited information (e.g., IP range but no credentials, or some documentation). Formerly called "gray box." Balances realism with efficiency. |
| **Unknown environment** | Tester is given no information — starts from zero, just like an external attacker. Formerly called "black box." Most realistic simulation of external threat. |

> **SY0-701 Terminology Change:**
>
> - White box → **Known environment**
> - Gray box → **Partially known environment**
> - Black box → **Unknown environment**
>
> The exam will use the new terms. Know both in case old terms appear in distractor options.

### Reconnaissance

| Type | What It Is |
|------|-----------|
| **Passive reconnaissance** | Gathering information about a target WITHOUT directly interacting with the target's systems. Uses OSINT (Open Source Intelligence): public records, WHOIS, job postings, social media, DNS lookups. Target never knows it happened. |
| **Active reconnaissance** | Directly probing or scanning the target's systems to gather information. Port scanning, banner grabbing, vulnerability scanning. Target systems log the activity. Noisier, detectable. |

> **Pen Test Type Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | Simulate real attacker, achieve objective, test all defenses | **Red team (offensive)** |
> | Detect and respond to attack, test monitoring and alerting | **Blue team (defensive)** |
> | Red and blue collaborate, share TTPs in real time, maximize learning | **Purple team (integrated)** |
> | Full info: diagrams, source code, credentials provided to tester | **Known environment** |
> | Some info provided, limited scope | **Partially known environment** |
> | No info given, start from scratch like an external attacker | **Unknown environment** |
> | OSINT, public records, no target contact, target unaware | **Passive reconnaissance** |
> | Port scanning, probing, direct interaction with target systems | **Active reconnaissance** |
>
> - Active recon touches the target. Passive recon never does.
> - Red/blue/purple = WHO is doing the testing and HOW they collaborate. Known/unknown = HOW MUCH information the tester starts with. These are separate dimensions — a red team can operate in known or unknown environment.

---

## 47. Security Awareness Practices

### Phishing Campaigns

| Concept | What It Means |
|---------|--------------|
| **Simulated phishing campaign** | Organization sends fake phishing emails to employees to test susceptibility. Click rates and credential submission rates are tracked. Employees who fail receive immediate training. |
| **Click rate** | Percentage of employees who clicked a link in a simulated phishing email. Key metric for program effectiveness. |
| **Reporting rate** | Percentage of employees who reported the suspicious email to the security team. High reporting rate = healthy security culture. |
| **Responding to reported messages** | Defined process for employees to report suspicious emails (e.g., "Report Phishing" button). Security team reviews and escalates if legitimate threat. |
| **Recognizing a phishing attempt** | Training employees to identify phishing indicators: mismatched sender domains, urgent language, unexpected attachments, hover-over URL inspection, generic greetings, requests for credentials. |

### Anomalous Behavior Recognition

| Behavior Type | What It Is | Example |
|---------------|-----------|---------|
| **Risky behavior** | Actions that are known to be dangerous or policy-violating. The employee knows (or should know) it is wrong. | Connecting unauthorized USB drives, sharing passwords, disabling antivirus |
| **Unexpected behavior** | Actions that are unusual for a specific user or context, even if not inherently wrong. May indicate account compromise. | Finance employee suddenly accessing engineering repos at 2am |
| **Unintentional behavior** | Accidental actions that create security risk with no malicious intent. | Emailing sensitive data to the wrong recipient, misconfiguring a cloud bucket |

> **Anomalous Behavior Decision Rules:**
>
> | If the question says... | Answer |
> |---|---|
> | "Knowingly violated policy," "ignored security rules," deliberate misuse | **Risky behavior** |
> | "Unusual for that user," "out of character," "never done this before," possible compromise | **Unexpected behavior** |
> | "Accidentally," "mistake," "didn't mean to," inadvertent | **Unintentional behavior** |

### User Training Topics

| Topic | What Training Covers |
|-------|---------------------|
| **Policy and handbooks** | Where to find security policies, how to read them, and the employee's responsibility to comply. Acknowledgement process. |
| **Situational awareness** | Recognizing social engineering attempts in real time: urgency, authority, pressure tactics, unusual requests, pretexting. |
| **Insider threat awareness** | Recognizing behavioral indicators in coworkers: sudden disgruntlement, unusual data access patterns, financial stress, policy violations. Clear reporting channels without fear of retaliation. |
| **Password management** | Creating strong, unique passwords; using password managers; never reusing passwords across accounts; recognizing credential phishing. |
| **Removable media and cables** | USB (Universal Serial Bus) drive risks (BadUSB, malware autorun); juice jacking (malicious charging cable or public charging port that exfiltrates data); policy on authorized vs unauthorized media. |
| **Social engineering recognition** | Red flags in emails (mismatched domains, urgency, unexpected attachments), phone calls (vishing), and physical access attempts (tailgating, piggybacking). |
| **OPSEC (Operational Security)** | Not disclosing sensitive org info on social media, in public spaces, or in unencrypted channels. Awareness of what information attackers can weaponize. |
| **Hybrid and remote work** | VPN (Virtual Private Network) usage requirements; securing home Wi-Fi; physical document security at home; shoulder surfing risks in public spaces; locking screens when stepping away. |

### Reporting and Monitoring

| Concept | What It Involves |
|---------|----------------|
| **Clear reporting channels** | Employees must know HOW and WHERE to report suspicious activity (IT helpdesk, SIEM (Security Information and Event Management) ticket, "Report Phishing" button, security hotline). |
| **Metrics tracking** | Click rates on phishing simulations, report rates, training completion rates, repeat offender identification. Used to measure program effectiveness. |
| **Improvement tracking** | Comparing metrics over time to show whether the program is reducing risky behavior. Reported to management. |
| **Initial reporting** | First report of a suspected incident or phishing email. Triggers investigation workflow. |
| **Recurring reporting** | Ongoing status updates to stakeholders throughout an incident or awareness campaign cycle. |

### Program Development

| Element | What It Involves |
|---------|----------------|
| **Role-based training** | Different training content for different job functions. Finance employees get wire fraud training. IT admins get privileged access training. Executives get spear-phishing training. |
| **Training frequency** | Annual minimum for most frameworks; high-risk roles may require quarterly. Phishing simulations typically monthly or quarterly. |
| **Gamification** | Using points, leaderboards, badges, and competition to increase engagement and retention in security training. |
| **Executive buy-in** | Leadership visibly supporting and participating in security awareness programs. Critical for culture change — employees follow what leadership models. |

> **Security Awareness vs Technical Controls:**
>
> - Security awareness training addresses the **human** layer — it changes behavior.
> - Technical controls (MFA, DLP, email filtering) address the **system** layer — they enforce regardless of behavior.
> - Exam will ask which addresses the "human element" or "social engineering risk" → always **security awareness training**.
> - Training does NOT replace technical controls. Both are required.

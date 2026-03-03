# Domain 4 Glossary Additions — New Sections 32–41

These sections cover gaps identified in the Domain 4 gap analysis. Add to `glossary.md` after section 17.

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

> **Mobile Connection Security:**
>
> | Connection | Risk |
> |---|---|
> | Cellular | Encrypted by carrier, SIM swapping risk, SS7 (Signaling System 7) vulnerabilities |
> | Wi-Fi | Rogue AP risk, eavesdropping on open networks, use VPN |
> | Bluetooth | Short range, bluejacking (unsolicited messages), bluesnarfing (data theft), bluesniffing |

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

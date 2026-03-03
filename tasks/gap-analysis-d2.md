# Domain 2 Gap Analysis: Threats, Vulnerabilities, and Mitigations (22%)

Generated: 2026-03-03
Source files analyzed: `glossary.md`, `concept-walkthrough.md`, `notes.md`
Reference: [CompTIA SY0-701 Exam Objectives](https://assets.ctfassets.net/82ripq7fjls2/6TYWUym0Nudqa8nGEnegjG/0f9b974d3b1837fe85ab8e6553f4d623/CompTIA-Security-Plus-SY0-701-Exam-Objectives.pdf)

---

## Coverage Legend

- **COVERED** — Topic appears in study materials with sufficient detail
- **PARTIAL** — Some aspects covered, key details missing (specifics noted)
- **MISSING** — Not covered at all in any study file

---

## 2.1 Compare and Contrast Common Threat Actors and Motivations

### Threat Actors

| Topic | Status | Notes |
|-------|--------|-------|
| Nation-state | **PARTIAL** | Mentioned only as "APT" in glossary (Section 9). No dedicated coverage of nation-state characteristics, examples, or how they differ from other actors. |
| Unskilled attacker | **MISSING** | No mention. SY0-701 replaced "script kiddie" with "unskilled attacker" — this terminology change needs coverage. |
| Hacktivist | **MISSING** | No mention in any file. |
| Insider threat | **PARTIAL** | UEBA section in glossary/walkthrough mentions insider threat detection, but no coverage of insider threat as a threat actor type (disgruntled employee, negligent insider, etc.). |
| Organized crime | **MISSING** | No mention. Financial motivation, ransomware-as-a-service connection not covered. |
| Shadow IT | **PARTIAL** | Mentioned in CASB context (glossary + walkthrough) as something CASB discovers. Not covered as a threat actor/vector in its own right — the risk it introduces (unmanaged apps, data exposure) is not framed from a Domain 2 threat perspective. |

### Motivations

| Topic | Status | Notes |
|-------|--------|-------|
| Data exfiltration | **PARTIAL** | DLP glossary entry references preventing exfiltration, but no coverage of data exfiltration as a threat motivation or its relationship to specific actor types. |
| Espionage | **MISSING** | No mention. Should be linked to nation-state actors. |
| Service disruption | **PARTIAL** | DDoS/DoS defined in glossary, but "service disruption" as a motivation category is not discussed. |
| Blackmail | **MISSING** | No mention. |
| Financial gain | **MISSING** | No mention as a motivation category despite being the most common. |
| Philosophical/political beliefs | **MISSING** | No mention. Should be linked to hacktivists. |
| Ethical | **MISSING** | No mention. Ethical hacking/authorized pentest motivation not discussed. |
| Revenge | **MISSING** | No mention. Should be linked to insider threats. |
| Disruption/chaos | **MISSING** | No mention. |
| War | **MISSING** | No mention. Cyberwarfare as motivation not discussed. |

### Threat Actor Attributes

| Topic | Status | Notes |
|-------|--------|-------|
| Internal/external | **MISSING** | No explicit coverage of internal vs. external classification of threat actors. |
| Resources/funding | **MISSING** | No mention. Nation-state = well-funded, unskilled = limited resources, etc. |
| Level of sophistication/capability | **PARTIAL** | APT described as "well-funded" in glossary, but no systematic treatment of sophistication levels across actor types. |

### 2.1 Summary

**Overall: MOSTLY MISSING.** The study materials cover security tools that detect threats (UEBA, DLP, CASB) but do not cover the threat actors themselves, their motivations, or their attributes. This is a significant gap — the exam tests actor-motivation mapping directly (e.g., "which threat actor is most likely motivated by financial gain?").

---

## 2.2 Explain Common Threat Vectors and Attack Surfaces

### Message-Based Vectors

| Topic | Status | Notes |
|-------|--------|-------|
| Email | **PARTIAL** | BEC (Business Email Compromise) defined in glossary. Phishing mentioned. No coverage of email as a general threat vector (malicious attachments, links, spoofing mechanics). |
| SMS (Short Message Service) | **PARTIAL** | Smishing listed in glossary under social engineering. No dedicated SMS vector discussion. |
| Instant messaging (IM) | **MISSING** | No mention as a threat vector. |

### Other Technical Vectors

| Topic | Status | Notes |
|-------|--------|-------|
| Image-based | **MISSING** | No mention. Steganography, malicious image files, embedded payloads not covered. |
| File-based | **MISSING** | No mention as a vector category. Malicious documents, macros, polyglot files not covered. |
| Voice call (vishing, spam over IP) | **PARTIAL** | Vishing listed as a social engineering term in glossary. SPIM/spam over IP not covered. |
| Removable devices | **MISSING** | No mention. USB attacks (rubber ducky, USB drop attacks, data exfiltration via USB) not covered. |
| Vulnerable software (client-based vs. agentless) | **PARTIAL** | "Vulnerable software" referenced indirectly through CVE/CVSS/patching discussions. The client-based vs. agentless distinction is not covered. |
| Unsupported systems and applications | **MISSING** | No mention. End-of-life software, legacy systems as attack surface not covered here (partially in 2.3). |
| Unsecure networks (wireless, wired, Bluetooth) | **PARTIAL** | WPA3/SAE/EAP-TLS covered in glossary (crypto section). Bluetooth attacks, wired network risks, rogue access points not covered. |
| Open service ports | **MISSING** | No mention. Common risky ports, port scanning, unnecessary open services not covered. |
| Default credentials | **MISSING** | Mentioned only as a hardening technique in 2.5 context ("default password changes"). Not covered as an attack surface/vector. |

### Supply Chain Vectors

| Topic | Status | Notes |
|-------|--------|-------|
| Managed service providers (MSPs) | **PARTIAL** | MSSP defined in glossary but only as a security service. MSPs as a supply chain attack vector (compromise MSP to reach customers) not covered. |
| Vendors | **MISSING** | No coverage as a supply chain vector. |
| Suppliers | **MISSING** | No coverage. Hardware/software supply chain compromise not discussed as a vector. |

### Human Vectors/Social Engineering

| Topic | Status | Notes |
|-------|--------|-------|
| Phishing | **PARTIAL** | Mentioned in glossary but no detailed coverage of phishing techniques, indicators, or variants beyond naming. |
| Vishing | **PARTIAL** | Listed in glossary. Minimal detail. |
| Smishing | **PARTIAL** | Listed in glossary. Minimal detail. |
| Misinformation/disinformation | **MISSING** | No mention. This is a newer SY0-701 topic — distinction between misinformation (unintentional) vs. disinformation (deliberate) not covered. |
| Impersonation | **MISSING** | No mention as a standalone social engineering technique. |
| Business email compromise (BEC) | **COVERED** | Defined in glossary: "Executive impersonation to financial fraud." |
| Pretexting | **MISSING** | No mention. Fabricating a scenario/backstory to extract information not covered. |
| Watering hole | **MISSING** | No mention. Compromising websites frequently visited by target group. |
| Brand impersonation | **MISSING** | No mention. Fake websites/emails mimicking trusted brands. |
| Typosquatting | **MISSING** | No mention. Registering misspelled domain names. |

### 2.2 Summary

**Overall: MOSTLY MISSING.** Social engineering terms are listed but not explained in depth. Technical vectors (image-based, file-based, removable devices, open ports, default creds) are almost entirely absent. Supply chain as a vector is not covered. The study materials approach these topics from the defender/tool side (what detects them) rather than the attacker side (what they are and how they work), which is what 2.2 tests.

---

## 2.3 Explain Various Types of Vulnerabilities

### Application Vulnerabilities

| Topic | Status | Notes |
|-------|--------|-------|
| Memory injection | **MISSING** | No mention. DLL injection, process injection not covered. |
| Buffer overflow | **PARTIAL** | Listed in glossary web vulns section but only as a term. No explanation of how buffer overflows work (stack vs. heap, exploitation). |
| Race conditions (TOCTOU) | **COVERED** | TOCTOU defined in glossary: "Race condition between validation and use." |
| Malicious update | **MISSING** | No mention. Compromised software updates as a vulnerability. |

### OS-Based Vulnerabilities

| Topic | Status | Notes |
|-------|--------|-------|
| OS-based vulnerabilities | **MISSING** | No coverage. Unpatched OS, privilege escalation via OS flaws, kernel vulnerabilities not discussed. |

### Web-Based Vulnerabilities

| Topic | Status | Notes |
|-------|--------|-------|
| SQL injection (SQLi) | **COVERED** | Defined in glossary with example (`' OR 1=1--`). WAF connection noted. |
| Cross-site scripting (XSS) | **COVERED** | All three types (stored, reflected, DOM-based) covered with decision rules in glossary. |

### Hardware Vulnerabilities

| Topic | Status | Notes |
|-------|--------|-------|
| Firmware | **MISSING** | No mention of firmware vulnerabilities. UEFI/BIOS attacks, firmware rootkits not covered. |
| End-of-life hardware | **MISSING** | No mention. Hardware that no longer receives updates/patches. |
| Legacy hardware | **MISSING** | No mention. Older hardware that cannot support modern security controls. |

### Virtualization Vulnerabilities

| Topic | Status | Notes |
|-------|--------|-------|
| VM escape | **MISSING** | No mention. Breaking out of a virtual machine to access the hypervisor or host. |
| Resource reuse | **MISSING** | No mention. Data remnants in memory/storage after VM deallocation. |

### Cloud-Specific Vulnerabilities

| Topic | Status | Notes |
|-------|--------|-------|
| Side-channel attacks | **MISSING** | No mention. Extracting data through shared physical resources in cloud (timing, cache). |
| Misconfiguration | **PARTIAL** | CSPM in glossary/walkthrough covers cloud misconfiguration detection (open S3 buckets, security groups). The vulnerability itself is discussed from the tool perspective, not as a vulnerability type. |

### Supply Chain Vulnerabilities

| Topic | Status | Notes |
|-------|--------|-------|
| Service provider | **MISSING** | No coverage of service provider compromise as a vulnerability type. |
| Hardware provider | **MISSING** | No mention. Compromised hardware in supply chain. |
| Software provider | **PARTIAL** | SBOM and SCA mentioned in glossary (DevSecOps section) but framed as tools, not as the vulnerability class. SLSA mentioned. |

### Cryptographic Vulnerabilities

| Topic | Status | Notes |
|-------|--------|-------|
| Downgrade attack | **MISSING** | No mention. Forcing use of weaker cipher/protocol version. |
| Collision attack | **MISSING** | MD5 listed as "weak/deprecated, collisions found" but collision attacks not explained as a concept. |
| Birthday attack | **MISSING** | No mention. Probability-based attack on hash functions. |

### Other Vulnerability Types

| Topic | Status | Notes |
|-------|--------|-------|
| Misconfiguration | **PARTIAL** | Referenced via CSPM but not covered as a standalone vulnerability type (default settings, open permissions, unnecessary services). |
| Mobile device — sideloading | **MISSING** | No mention. Installing apps from outside official app stores. |
| Mobile device — jailbreaking | **MISSING** | No mention. Removing manufacturer restrictions to gain root access. |
| Zero-day | **MISSING** | No mention. Vulnerability unknown to vendor with no patch available. |

### 2.3 Summary

**Overall: MOSTLY MISSING.** Web vulnerabilities (SQLi, XSS) and TOCTOU are well covered. Nearly everything else is absent: hardware vulns, virtualization vulns, cloud-specific vulns, cryptographic attacks, mobile vulns, zero-day, OS vulns, and supply chain vulns. This is a major gap.

---

## 2.4 Given a Scenario, Analyze Indicators of Malicious Activity

### Malware Types

| Topic | Status | Notes |
|-------|--------|-------|
| Ransomware | **MISSING** | No definition or coverage. One of the most exam-relevant malware types. |
| Trojan | **PARTIAL** | RAT (Remote Access Trojan) defined in glossary but "trojan" as a general malware category is not explained. |
| Worm | **MISSING** | No mention. Self-propagating malware. |
| Spyware | **MISSING** | No mention. |
| Bloatware | **MISSING** | No mention. Pre-installed unwanted software. |
| Virus | **MISSING** | No mention as a malware type (polymorphic viruses especially). |
| Keylogger | **MISSING** | No mention. |
| Logic bomb | **MISSING** | No mention. Code that triggers on a condition (date, event). |
| Rootkit | **MISSING** | No mention. Malware that hides deep in OS/firmware. |

### Physical Attacks

| Topic | Status | Notes |
|-------|--------|-------|
| Brute force (physical) | **MISSING** | No mention of physical brute force (breaking locks, doors). |
| RFID cloning | **MISSING** | No mention. Copying RFID badge data. |
| Environmental attacks | **MISSING** | No mention. Power manipulation, temperature, flooding. |

### Network Attacks

| Topic | Status | Notes |
|-------|--------|-------|
| DDoS (distributed, amplified, reflected) | **PARTIAL** | DDoS/DoS defined in glossary. Amplified and reflected variants not explained. |
| DNS attacks (poisoning, spoofing) | **MISSING** | No mention. DNS cache poisoning, DNS hijacking, DNS tunneling. |
| On-path attack | **COVERED** | Defined in glossary as MitM with SY0-701 terminology note. |
| Credential replay | **MISSING** | No mention. Capturing and reusing authentication credentials. |
| Malicious code | **MISSING** | No mention as a network attack indicator. |
| Protocol abuse | **MISSING** | No mention. Abusing legitimate protocols for malicious purposes. |

### Application Attacks

| Topic | Status | Notes |
|-------|--------|-------|
| Injection | **COVERED** | SQLi covered in detail. XXE, SSRF, LFI/RFI also in glossary. |
| Buffer overflow | **PARTIAL** | Listed but not explained in depth. |
| Replay attack | **MISSING** | No mention. Capturing and retransmitting valid data. |
| Privilege escalation | **MISSING** | No mention. Gaining higher-level permissions than authorized. |
| Forgery (CSRF, SSRF) | **COVERED** | Both CSRF and SSRF defined with decision rules in glossary. |
| Directory traversal | **MISSING** | No mention (LFI is related but directory traversal as `../../etc/passwd` not explicitly covered). |

### Cryptographic Attacks

| Topic | Status | Notes |
|-------|--------|-------|
| Downgrade | **MISSING** | No mention. |
| Collision | **PARTIAL** | MD5 collision mentioned in passing. Not explained as an attack. |
| Birthday | **MISSING** | No mention. |

### Password Attacks

| Topic | Status | Notes |
|-------|--------|-------|
| Password spraying | **COVERED** | Defined in glossary password attacks table. |
| Brute force | **COVERED** | Defined in glossary password attacks table. |
| Dictionary | **COVERED** | Defined in glossary password attacks table. |
| Credential stuffing | **COVERED** | Defined in glossary password attacks table. |
| Rainbow table | **COVERED** | Defined in glossary with salting countermeasure. |

### Indicators of Malicious Activity

| Topic | Status | Notes |
|-------|--------|-------|
| Account lockout | **MISSING** | No mention as an indicator. |
| Concurrent sessions | **MISSING** | No mention. Multiple active sessions from different locations. |
| Blocked content | **MISSING** | No mention as an indicator. |
| Impossible travel | **PARTIAL** | UEBA walkthrough describes "logs in from Romania at 3am" scenario which is essentially impossible travel, but the term itself is not used. |
| Resource consumption | **MISSING** | No mention. Unusual CPU/memory/bandwidth as an indicator. |
| Resource inaccessibility | **MISSING** | No mention. Systems becoming unavailable as an indicator. |
| Out-of-cycle logging | **MISSING** | No mention. Unexpected log entries outside normal patterns. |
| Missing logs | **MISSING** | No mention. Log deletion as evidence of compromise. |
| Published/documented indicators | **MISSING** | No mention. Using published threat feeds and IOC databases. |

### 2.4 Summary

**Overall: MAJOR GAPS.** Password attacks are well covered. On-path attacks, injection/forgery web attacks are covered. Nearly all malware types are missing (ransomware, worm, virus, rootkit, keylogger, logic bomb). Physical attacks are entirely absent. Network attack variants (amplified/reflected DDoS, DNS attacks, credential replay) are missing. All behavioral indicators (account lockout, concurrent sessions, impossible travel, missing logs, etc.) are missing. This is the highest-weight domain and needs urgent attention.

---

## 2.5 Explain the Purpose of Mitigation Techniques

### Core Mitigation Techniques

| Topic | Status | Notes |
|-------|--------|-------|
| Segmentation | **PARTIAL** | VLAN and screened subnet (DMZ) defined in glossary. Network segmentation mentioned for ICS/SCADA. Not covered as a general mitigation technique with micro-segmentation. |
| Access control | **COVERED** | RBAC, ABAC, MAC, DAC all covered with decision rules in glossary. |
| Application allow list | **MISSING** | No mention. Permitting only approved applications to run. |
| Application block list | **MISSING** | No mention. Blocking known-bad applications. |
| Isolation | **PARTIAL** | Containment step in IR mentions isolation. Honeypot isolation mentioned. Not covered as a general mitigation technique. |
| Patching | **PARTIAL** | Mentioned indirectly (CVE/CVSS drive patching priority). Not covered as a mitigation technique — patch management process, patch testing, rollback not discussed. |
| Encryption | **COVERED** | Extensive coverage in glossary crypto section (AES, RSA, ECC, TLS, E2EE, etc.). |
| Monitoring | **COVERED** | Extensive coverage: SIEM, XDR, SOAR, UEBA, EDR, IDS/IPS, FIM all covered with decision rules. |
| Least privilege | **PARTIAL** | PAM and JIT defined in glossary. Least privilege as a general principle not explicitly stated as a mitigation technique. |
| Configuration enforcement | **PARTIAL** | CSPM covers cloud config enforcement. SCAP/XCCDF covers compliance benchmarks. Not framed as a general mitigation technique. |
| Decommissioning | **MISSING** | No mention. Properly retiring systems/software to reduce attack surface. |

### Hardening Techniques

| Topic | Status | Notes |
|-------|--------|-------|
| Encryption (as hardening) | **COVERED** | See crypto section above. |
| Installation of endpoint protection | **PARTIAL** | EDR defined in glossary. Not framed as a hardening step. |
| Host-based firewall | **MISSING** | No mention. Configuring firewalls on individual hosts. |
| Host-based IPS | **MISSING** | No mention. IPS is covered but only at network level, not host-based. |
| Disabling ports/protocols | **MISSING** | No mention as a hardening technique. |
| Default password changes | **PARTIAL** | Listed in glossary exam quick-hits as "credential vaulting" context. Not explicitly covered as a hardening step. |
| Removal of unnecessary software | **MISSING** | No mention. Reducing attack surface by removing unneeded applications. |

### 2.5 Summary

**Overall: PARTIAL.** Access control models and encryption are well covered. Monitoring tools are extensively covered. However, several key mitigation techniques are missing or only partially covered: application allow/block listing, decommissioning, host-based firewalls/IPS, disabling ports/protocols, removing unnecessary software. Patching as a process needs more depth.

---

## Priority Remediation Plan

### Critical Gaps (High Impact, Zero Coverage)

These topics have NO coverage and appear frequently on the exam:

1. **Malware types** (2.4) — ransomware, worm, virus, spyware, keylogger, logic bomb, rootkit, bloatware
2. **Threat actors and motivations** (2.1) — the entire actor-motivation matrix
3. **Cryptographic attacks** (2.3/2.4) — downgrade, collision, birthday attacks
4. **Social engineering techniques** (2.2) — pretexting, watering hole, typosquatting, brand impersonation, misinformation/disinformation
5. **Behavioral indicators** (2.4) — account lockout, impossible travel, concurrent sessions, missing logs, resource consumption
6. **Zero-day vulnerabilities** (2.3)
7. **Virtualization vulnerabilities** (2.3) — VM escape, resource reuse
8. **Mobile vulnerabilities** (2.3) — sideloading, jailbreaking
9. **Application allow/block listing** (2.5)

### Significant Gaps (Partial Coverage, Needs Depth)

These topics are mentioned but need dedicated study:

10. **Network attack variants** (2.4) — amplified/reflected DDoS, DNS attacks, credential replay
11. **Supply chain** (2.2/2.3) — as both vector and vulnerability type
12. **Hardening techniques** (2.5) — host-based firewall/IPS, disabling ports, removing software
13. **Threat vectors** (2.2) — image-based, file-based, removable devices, open ports, default credentials
14. **Patching and decommissioning** (2.5)

### Adequately Covered (Review Only)

These topics have good coverage and need only review:

- Password attacks (brute force, spraying, credential stuffing, rainbow tables)
- Web vulnerabilities (SQLi, XSS types, CSRF, SSRF, XXE, IDOR)
- On-path attacks
- Access control models (RBAC, ABAC, MAC, DAC)
- Encryption and cryptographic fundamentals
- Monitoring tools (SIEM, XDR, SOAR, UEBA, EDR, IDS/IPS)

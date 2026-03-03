# Domain 2 Glossary Validation Report

**Date:** 2026-03-03
**File validated:** `tasks/new-glossary-d2.md`
**Validated against:** Official CompTIA Security+ SY0-701 Exam Objectives (Version 5.0), cross-referenced with Professor Messer SY0-701 course outline, DestCert study guide, InfoSec Institute, and ExamCompass resources.

---

## Methodology

Every item in the new glossary content (sections 25-31) was checked against the official SY0-701 Domain 2 objectives (2.1 through 2.5) and their exact sub-bullets. Items are classified as:

- **VALID** — Explicitly listed in official objectives
- **INFERRED** — Not explicitly named but clearly implied by an objective bullet
- **QUESTIONABLE** — May be out of scope or too detailed for the exam
- **MISSING FROM CONTENT** — Listed in official objectives but absent from the glossary

---

## Section 25: Threat Actors and Motivations (Objective 2.1)

**Objective 2.1: Compare and contrast common threat actors and motivations.**

### Threat Actor Types

| Glossary Item | Status | Notes |
|---|---|---|
| Nation-state | **VALID** | Explicitly listed in 2.1 |
| Unskilled attacker | **VALID** | Explicitly listed in 2.1 |
| Hacktivist | **VALID** | Explicitly listed in 2.1 |
| Insider threat | **VALID** | Explicitly listed in 2.1 |
| Organized crime | **VALID** | Explicitly listed in 2.1 |
| Shadow IT | **VALID** | Explicitly listed in 2.1 |

### Threat Actor Attributes

| Glossary Item | Status | Notes |
|---|---|---|
| Internal/External | **VALID** | Explicitly listed in 2.1 under "Attributes of actors" |
| Resources/funding | **VALID** | Explicitly listed in 2.1 under "Attributes of actors" |
| Sophistication/capability | **VALID** | Explicitly listed in 2.1 as "Level of sophistication/capability" |

### Motivations

| Glossary Item | Status | Notes |
|---|---|---|
| Data exfiltration | **VALID** | Explicitly listed in 2.1 |
| Espionage | **VALID** | Explicitly listed in 2.1 |
| Financial gain | **VALID** | Explicitly listed in 2.1 |
| Blackmail | **VALID** | Explicitly listed in 2.1 |
| Service disruption | **VALID** | Explicitly listed in 2.1 |
| Philosophical/political beliefs | **VALID** | Explicitly listed in 2.1 |
| Ethical | **VALID** | Explicitly listed in 2.1 |
| Revenge | **VALID** | Explicitly listed in 2.1 |
| Disruption/chaos | **VALID** | Explicitly listed in 2.1 |
| War | **VALID** | Explicitly listed in 2.1 |

**Section 25 verdict: COMPLETE.** All 2.1 objective items are covered. No missing items. No questionable additions.

---

## Section 26: Malware Types (Objective 2.4)

**Objective 2.4: Given a scenario, analyze indicators of malicious activity — Malware attacks sub-section.**

| Glossary Item | Status | Notes |
|---|---|---|
| Ransomware | **VALID** | Explicitly listed in 2.4 under "Malware attacks" |
| Trojan | **VALID** | Explicitly listed in 2.4 |
| Worm | **VALID** | Explicitly listed in 2.4 |
| Virus | **VALID** | Explicitly listed in 2.4 |
| Spyware | **VALID** | Explicitly listed in 2.4 |
| Bloatware | **VALID** | Explicitly listed in 2.4 |
| Keylogger | **VALID** | Explicitly listed in 2.4 |
| Logic bomb | **VALID** | Explicitly listed in 2.4 |
| Rootkit | **VALID** | Explicitly listed in 2.4 |

**Section 26 verdict: COMPLETE.** All officially listed malware types are covered. No missing items.

---

## Section 27: Social Engineering and Human Vectors (Objective 2.2)

**Objective 2.2: Explain common threat vectors and attack surfaces — "Human vectors/social engineering" sub-section.**

| Glossary Item | Status | Notes |
|---|---|---|
| Phishing | **VALID** | Explicitly listed in 2.2 |
| Vishing | **VALID** | Explicitly listed in 2.2 |
| Smishing | **VALID** | Explicitly listed in 2.2 |
| Pretexting | **VALID** | Explicitly listed in 2.2 |
| Watering hole | **VALID** | Explicitly listed in 2.2 |
| Brand impersonation | **VALID** | Explicitly listed in 2.2 |
| Typosquatting | **VALID** | Explicitly listed in 2.2 |
| Impersonation | **VALID** | Explicitly listed in 2.2 |
| Misinformation/Disinformation | **VALID** | Explicitly listed in 2.2 as "Misinformation/disinformation" |
| Spear phishing | **INFERRED** | Not a separate bullet in 2.2 but is a standard sub-type of phishing. Every major study resource covers it as part of the phishing bullet. Acceptable to include. |
| Whaling | **INFERRED** | Same as spear phishing — a sub-type of phishing, not separately listed but universally taught alongside it. Acceptable. |

### Missing from content

| Official Item | Status | Notes |
|---|---|---|
| **Business email compromise (BEC)** | **MISSING FROM CONTENT** | Explicitly listed in 2.2 under "Human vectors/social engineering." The glossary mentions BEC in passing as part of the Email vector description in Section 28 but does not give it its own entry or definition in the social engineering section where the objective places it. BEC should have a standalone entry explaining what it is: attacker compromises or impersonates a business email account to authorize fraudulent transactions, typically targeting finance departments. |

**Section 27 verdict: ONE GAP.** BEC needs a standalone entry in the social engineering section.

---

## Section 28: Threat Vectors and Attack Surfaces (Objective 2.2)

**Objective 2.2: Explain common threat vectors and attack surfaces.**

### Message-Based Vectors

| Glossary Item | Status | Notes |
|---|---|---|
| Email | **VALID** | Explicitly listed in 2.2 |
| SMS | **VALID** | Explicitly listed in 2.2 as "Short Message Service (SMS)" |
| Instant messaging (IM) | **VALID** | Explicitly listed in 2.2 |

### File and Image-Based Vectors

| Glossary Item | Status | Notes |
|---|---|---|
| Image-based attacks | **VALID** | Explicitly listed in 2.2 as "Image-based" |
| File-based attacks | **VALID** | Explicitly listed in 2.2 as "File-based" |

### Voice and Removable Device Vectors

| Glossary Item | Status | Notes |
|---|---|---|
| Voice calls | **VALID** | Explicitly listed in 2.2 as "Voice call" |
| Removable devices | **VALID** | Explicitly listed in 2.2 as "Removable device" |
| SPIM (Spam over IM) | **QUESTIONABLE** | Not explicitly listed in 2.2. While IM is listed as a vector, SPIM is not a specific term in the objectives. Minor addition — not harmful but not required. |
| Rubber Ducky | **INFERRED** | Not explicitly listed but falls under "Removable device" vector. Common exam scenario topic. Acceptable. |
| USB drop attack | **INFERRED** | Not explicitly listed but falls under "Removable device" vector. Standard exam topic. |

### Software and System Vectors

| Glossary Item | Status | Notes |
|---|---|---|
| Vulnerable software — client-based | **VALID** | Explicitly listed in 2.2 as "Vulnerable software — Client-based vs. agentless" |
| Vulnerable software — agentless | **VALID** | Explicitly listed in 2.2 |
| Unsupported/end-of-life systems | **VALID** | Explicitly listed in 2.2 as "Unsupported systems and applications" |
| Open service ports | **VALID** | Explicitly listed in 2.2 |
| Default credentials | **VALID** | Explicitly listed in 2.2 |

### Network-Based Vectors

| Glossary Item | Status | Notes |
|---|---|---|
| Rogue access point | **INFERRED** | Not a separate bullet in 2.2 but falls under "Unsecure networks — Wireless." Standard exam topic for wireless attacks. |
| Evil twin | **INFERRED** | Not a separate bullet in 2.2 but falls under "Unsecure networks — Wireless." Standard exam topic. |
| Bluejacking | **INFERRED** | Falls under "Unsecure networks — Bluetooth." Not explicitly named but is a core Bluetooth attack type covered by all study resources. |
| Bluesnarfing | **INFERRED** | Falls under "Unsecure networks — Bluetooth." Same as above. |

### Supply Chain Vectors

| Glossary Item | Status | Notes |
|---|---|---|
| MSPs (Managed Service Providers) | **VALID** | Explicitly listed in 2.2 under "Supply chain" |
| Vendors | **VALID** | Explicitly listed in 2.2 |
| Suppliers | **VALID** | Explicitly listed in 2.2 |

### Missing from content

| Official Item | Status | Notes |
|---|---|---|
| Unsecure networks — Wired | **MISSING FROM CONTENT** | The objective explicitly lists "Wired" as a sub-bullet under "Unsecure networks" alongside Wireless and Bluetooth. The glossary covers Wireless (rogue AP, evil twin) and Bluetooth (bluejacking, bluesnarfing) but has no entry for wired network threats (e.g., unauthorized physical network access, network taps, unencrypted wired traffic). |

**Section 28 verdict: ONE GAP.** Wired network threats need coverage. One QUESTIONABLE item (SPIM) is not harmful but not required.

---

## Section 29: Vulnerability Types Expanded (Objective 2.3)

**Objective 2.3: Explain various types of vulnerabilities.**

### Application Vulnerabilities

| Glossary Item | Status | Notes |
|---|---|---|
| Memory injection | **VALID** | Explicitly listed in 2.3 under "Application" |
| Buffer overflow | **VALID** | Explicitly listed in 2.3 |
| Malicious update | **VALID** | Explicitly listed in 2.3 |
| DLL injection (in memory injection entry) | **INFERRED** | Not separately listed but is a form of memory injection. Acceptable detail. |

### Race Conditions

| Official Item | Status | Notes |
|---|---|---|
| **Race conditions** | **MISSING FROM CONTENT** | Explicitly listed in 2.3 under "Application" with sub-bullets "Time-of-check (TOC)" and "Time-of-use (TOU)." The glossary does not cover race conditions, TOC, or TOU anywhere. This is a notable gap. |

### OS and Hardware Vulnerabilities

| Glossary Item | Status | Notes |
|---|---|---|
| OS-based vulnerabilities | **VALID** | Explicitly listed in 2.3 as "Operating system (OS)-based" |
| Firmware vulnerabilities | **VALID** | Explicitly listed in 2.3 under "Hardware — Firmware" |
| End-of-life hardware | **VALID** | Explicitly listed in 2.3 under "Hardware — End-of-life" |
| Legacy hardware | **VALID** | Explicitly listed in 2.3 under "Hardware — Legacy" |

### Virtualization Vulnerabilities

| Glossary Item | Status | Notes |
|---|---|---|
| VM escape | **VALID** | Explicitly listed in 2.3 under "Virtualization" |
| Resource reuse | **VALID** | Explicitly listed in 2.3 under "Virtualization" |

### Cloud-Specific Vulnerabilities

| Glossary Item | Status | Notes |
|---|---|---|
| Side-channel attack | **INFERRED** | Not explicitly named in 2.3 but falls under "Cloud-specific" as a well-known cloud vulnerability. All major study resources cover it here. Acceptable. |

### Cryptographic Vulnerabilities

| Glossary Item | Status | Notes |
|---|---|---|
| Downgrade attack | **QUESTIONABLE placement** | Downgrade attacks are explicitly listed in 2.4 under "Cryptographic attacks," NOT in 2.3. The 2.3 objective lists "Cryptographic" as a generic vulnerability type. The glossary places downgrade here in section 29. While the content itself is correct and exam-relevant, the placement creates a mapping inconsistency — these are 2.4 indicators, not 2.3 vulnerabilities. Not a content error, just an organizational note. |
| Collision attack | **QUESTIONABLE placement** | Same as downgrade — listed in 2.4 under "Cryptographic attacks," not 2.3. |
| Birthday attack | **QUESTIONABLE placement** | Same as above — 2.4 item, not 2.3. |

### Mobile Vulnerabilities

| Glossary Item | Status | Notes |
|---|---|---|
| Sideloading | **VALID** | Explicitly listed in 2.3 under "Mobile device — Side loading" |
| Jailbreaking | **VALID** | Explicitly listed in 2.3 under "Mobile device — Jailbreaking" |

### Zero-Day and Supply Chain Vulnerabilities

| Glossary Item | Status | Notes |
|---|---|---|
| Zero-day | **VALID** | Explicitly listed in 2.3 |
| Supply chain — service provider | **VALID** | Explicitly listed in 2.3 |
| Supply chain — hardware provider | **VALID** | Explicitly listed in 2.3 |
| Supply chain — software provider | **VALID** | Explicitly listed in 2.3 |

### Missing from content

| Official Item | Status | Notes |
|---|---|---|
| **Race conditions (TOC/TOU)** | **MISSING FROM CONTENT** | Explicitly listed in 2.3 under "Application" with sub-bullets "Time-of-check (TOC)" and "Time-of-use (TOU)." A race condition occurs when a system's behavior depends on the sequence or timing of uncontrollable events. TOC/TOU is when a resource is checked for a condition (permissions, existence) and then used, but the resource changes between the check and the use. This is a distinct exam topic. |
| **Web-based — SQL injection (SQLi)** | **MISSING FROM CONTENT** | Explicitly listed in 2.3 under "Web-based." SQLi is covered in Section 30 under application attacks (2.4) but is NOT defined in Section 29 where the vulnerability type itself belongs (2.3). The glossary should define SQLi as a vulnerability type. |
| **Web-based — Cross-site scripting (XSS)** | **MISSING FROM CONTENT** | Explicitly listed in 2.3 under "Web-based." Same issue as SQLi — may appear in other sections but is not covered in the vulnerability types section where 2.3 places it. |
| **Misconfiguration** | **MISSING FROM CONTENT** | Explicitly listed in 2.3 as a top-level vulnerability type. No standalone entry explains misconfiguration as a vulnerability category (default settings, open permissions, unnecessary services, verbose error messages). |

**Section 29 verdict: FOUR GAPS.** Race conditions (TOC/TOU), SQLi, XSS, and misconfiguration all need coverage as vulnerability types under 2.3. Cryptographic attacks (downgrade, collision, birthday) are valid content but belong to 2.4 — organizational note only.

---

## Section 30: Indicators of Malicious Activity (Objective 2.4)

**Objective 2.4: Given a scenario, analyze indicators of malicious activity.**

### Physical Attacks

| Glossary Item | Status | Notes |
|---|---|---|
| Brute force (physical) | **VALID** | Explicitly listed in 2.4 under "Physical attacks — Brute force" |
| RFID cloning | **VALID** | Explicitly listed in 2.4 under "Physical attacks — RFID cloning" |
| Environmental attacks | **VALID** | Explicitly listed in 2.4 under "Physical attacks — Environmental" |

### Network Attacks

| Glossary Item | Status | Notes |
|---|---|---|
| Amplified DDoS | **INFERRED** | Amplification is a sub-type of DDoS, which is explicitly listed in 2.4. All study resources cover amplified DDoS as part of the DDoS bullet. |
| Reflected DDoS | **INFERRED** | Same — sub-type of the explicit DDoS bullet. |
| DNS poisoning | **VALID** | Explicitly listed in 2.4 under "Network attacks — DNS attacks" |
| DNS spoofing | **INFERRED** | Closely related to DNS poisoning. Often used interchangeably. Covered by the DNS attacks bullet. |
| DNS tunneling | **QUESTIONABLE** | Not explicitly listed in 2.4. Falls under DNS attacks conceptually but is not a standard sub-bullet. Some study guides cover it, others don't. Useful knowledge but may be too detailed for the core objectives. Not harmful to include. |
| Credential replay | **VALID** | Explicitly listed in 2.4 under "Network attacks — Credential replay" |
| Protocol abuse | **QUESTIONABLE** | Not explicitly listed in 2.4. This is a general concept, not a specific objective bullet. Useful context but not a testable discrete item. |
| On-path attack (MitM) | **MISSING FROM GLOSSARY BUT REFERENCED** | Explicitly listed in 2.4 under "Network attacks — On-path attack." The glossary mentions it in passing but does not have a standalone definition entry. |

### Network Attacks — Missing from content

| Official Item | Status | Notes |
|---|---|---|
| **Wireless attacks** | **MISSING FROM CONTENT** | Explicitly listed in 2.4 under "Network attacks" with typical sub-items: evil twin, rogue access point, deauthentication/disassociation. While some wireless concepts appear in Section 28 (threat vectors), the 2.4 context is about recognizing wireless attack indicators — different from listing vectors. |
| **Malicious code** | **MISSING FROM CONTENT** | Explicitly listed in 2.4 under "Network attacks — Malicious code." This covers malicious scripts, macros, and code injected into network traffic or executed through network-delivered payloads. |

### Application Attacks

| Glossary Item | Status | Notes |
|---|---|---|
| Replay attack | **VALID** | Explicitly listed in 2.4 under "Application attacks — Replay" |
| Privilege escalation | **VALID** | Explicitly listed in 2.4 under "Application attacks — Privilege escalation" |
| Directory traversal | **VALID** | Explicitly listed in 2.4 under "Application attacks — Directory traversal" |

### Application Attacks — Missing from content

| Official Item | Status | Notes |
|---|---|---|
| **Injection** | **MISSING FROM CONTENT** | Explicitly listed in 2.4 under "Application attacks — Injection." While SQLi appears in the cryptographic/vulnerability sections, injection as a 2.4 attack indicator (recognizing injection in logs, detecting SQLi/command injection attempts) is not covered. |
| **Buffer overflow** | **MISSING FROM CONTENT** | Explicitly listed in 2.4 under "Application attacks — Buffer overflow." Covered in Section 29 as a vulnerability type (2.3) but not as a 2.4 attack indicator. |
| **Forgery (CSRF/SSRF)** | **MISSING FROM CONTENT** | Explicitly listed in 2.4 under "Application attacks — Forgery." Cross-Site Request Forgery (CSRF) and Server-Side Request Forgery (SSRF) are testable items. Neither appears in the glossary. |

### Cryptographic Attacks

Note: Downgrade, collision, and birthday attacks appear in Section 29 (mapped to 2.3) rather than here in Section 30 (where 2.4 places them). The content exists but is in the wrong section from an objective-mapping perspective.

### Password Attacks — Missing from content

| Official Item | Status | Notes |
|---|---|---|
| **Password spraying** | **MISSING FROM CONTENT** | Explicitly listed in 2.4 under "Password attacks — Spraying." The glossary mentions "password spraying" in passing under the "Account lockout" behavioral indicator but does not define it as a standalone attack type. |
| **Brute force (password)** | **MISSING FROM CONTENT** | Explicitly listed in 2.4 under "Password attacks — Brute force." Distinct from physical brute force (which IS covered). Password brute force = systematically trying all possible password combinations. |

### Behavioral Indicators

| Glossary Item | Status | Notes |
|---|---|---|
| Account lockout | **VALID** | Explicitly listed in 2.4 under "Indicators" |
| Concurrent sessions | **VALID** | Explicitly listed in 2.4 as "Concurrent session usage" |
| Blocked content | **VALID** | Explicitly listed in 2.4 |
| Impossible travel | **VALID** | Explicitly listed in 2.4 |
| Resource consumption | **VALID** | Explicitly listed in 2.4 |
| Resource inaccessibility | **VALID** | Explicitly listed in 2.4 |
| Out-of-cycle logging | **VALID** | Explicitly listed in 2.4 |
| Missing logs | **VALID** | Explicitly listed in 2.4 |
| Published/documented indicators | **VALID** | Explicitly listed in 2.4 as "Published/documented" |

**Section 30 verdict: SIGNIFICANT GAPS.** Missing: on-path attack (standalone entry), wireless attack indicators, malicious code, injection attacks, buffer overflow (as attack indicator), forgery (CSRF/SSRF), password spraying, and password brute force. Some items (DNS tunneling, protocol abuse) are questionable additions.

---

## Section 31: Mitigation Techniques Expanded (Objective 2.5)

**Objective 2.5: Explain the purpose of mitigation techniques used to secure the enterprise.**

| Glossary Item | Status | Notes |
|---|---|---|
| Application allow list | **VALID** | Explicitly listed in 2.5 as "Application allow list" |
| Application block list | **INFERRED** | Not explicitly listed in 2.5 but is the natural counterpart to allow list. All study resources cover both. |
| Isolation | **VALID** | Explicitly listed in 2.5 |
| Patching | **VALID** | Explicitly listed in 2.5 |
| Decommissioning | **VALID** | Explicitly listed in 2.5 |
| Configuration enforcement | **VALID** | Explicitly listed in 2.5 |
| Host-based firewall | **VALID** | Explicitly listed in 2.5 under "Hardening techniques — Host-based firewall" |
| Host-based IPS (HIPS) | **VALID** | Explicitly listed in 2.5 under "Hardening techniques — Host-based intrusion prevention system (HIPS)" |
| Disabling ports/protocols | **VALID** | Explicitly listed in 2.5 under "Hardening techniques — Disabling ports/protocols" |
| Default password changes | **VALID** | Explicitly listed in 2.5 under "Hardening techniques — Default password changes" |
| Removal of unnecessary software | **VALID** | Explicitly listed in 2.5 under "Hardening techniques — Removal of unnecessary software" |

### Missing from content

| Official Item | Status | Notes |
|---|---|---|
| **Segmentation** | **MISSING FROM CONTENT** | Explicitly listed in 2.5 as a top-level mitigation technique. Network segmentation (VLANs, subnets, micro-segmentation) limits lateral movement. The glossary mentions "network segmentation" in passing under Isolation but does not give it a standalone entry. |
| **Access control** | **MISSING FROM CONTENT** | Explicitly listed in 2.5 with sub-bullets "Access control list (ACL)" and "Permissions." Neither ACLs nor permissions are defined in the glossary as 2.5 mitigation items. |
| **Encryption** | **MISSING FROM CONTENT** | Explicitly listed in 2.5 as both a top-level mitigation technique AND under "Hardening techniques — Encryption." File-level encryption (EFS), full disk encryption (BitLocker, FileVault), encryption at rest/in transit are all relevant. The glossary does not cover encryption as a mitigation. |
| **Monitoring** | **MISSING FROM CONTENT** | Explicitly listed in 2.5 as a top-level mitigation technique. Continuous monitoring of network traffic, logs, and system behavior to detect threats. |
| **Least privilege** | **MISSING FROM CONTENT** | Explicitly listed in 2.5. Users and processes get only the minimum permissions needed. A fundamental security principle. |
| **Installation of endpoint protection** | **MISSING FROM CONTENT** | Explicitly listed in 2.5 under "Hardening techniques." Antivirus, anti-malware, EDR (Endpoint Detection and Response) agent deployment. |

**Section 31 verdict: SIGNIFICANT GAPS.** Six items from the official 2.5 objectives are missing: segmentation, access control (ACL/permissions), encryption, monitoring, least privilege, and endpoint protection installation.

---

## Summary

### Overall Coverage Statistics

| Section | Glossary Items | Valid/Inferred | Questionable | Missing from Official | Official Items Missing from Glossary |
|---|---|---|---|---|---|
| 25 (Threat Actors) | 19 | 19 | 0 | 0 | 0 |
| 26 (Malware) | 9 | 9 | 0 | 0 | 0 |
| 27 (Social Engineering) | 11 | 11 | 0 | 0 | 1 (BEC) |
| 28 (Threat Vectors) | 18 | 16 | 2 | 0 | 1 (wired networks) |
| 29 (Vulnerability Types) | 16 | 13 | 3 (placement) | 0 | 4 (race conditions, SQLi, XSS, misconfiguration) |
| 30 (Indicators) | 18 | 16 | 2 | 0 | 8 (on-path, wireless, malicious code, injection, buffer overflow, forgery, spraying, brute force) |
| 31 (Mitigation) | 11 | 11 | 0 | 0 | 6 (segmentation, access control, encryption, monitoring, least privilege, endpoint protection) |

### Critical Missing Items (must add)

These items are **explicitly listed** in the official CompTIA SY0-701 exam objectives and are absent from the glossary:

1. **Business email compromise (BEC)** — 2.2 human vectors
2. **Wired network threats** — 2.2 unsecure networks
3. **Race conditions (TOC/TOU)** — 2.3 application vulnerabilities
4. **SQL injection (SQLi)** — 2.3 web-based vulnerabilities
5. **Cross-site scripting (XSS)** — 2.3 web-based vulnerabilities
6. **Misconfiguration** — 2.3 vulnerability type
7. **On-path attack (MitM)** — 2.4 network attacks (needs standalone entry)
8. **Wireless attack indicators** — 2.4 network attacks
9. **Malicious code** — 2.4 network attacks
10. **Injection attacks** — 2.4 application attacks
11. **Buffer overflow as attack indicator** — 2.4 application attacks
12. **Forgery (CSRF/SSRF)** — 2.4 application attacks
13. **Password spraying** — 2.4 password attacks (needs standalone entry)
14. **Password brute force** — 2.4 password attacks
15. **Segmentation** — 2.5 mitigation technique
16. **Access control (ACL/permissions)** — 2.5 mitigation technique
17. **Encryption as mitigation** — 2.5 mitigation technique
18. **Monitoring** — 2.5 mitigation technique
19. **Least privilege** — 2.5 mitigation technique
20. **Installation of endpoint protection** — 2.5 hardening technique

### Questionable Items (consider removing or noting as supplementary)

1. **SPIM** — Not in objectives; minor addition
2. **DNS tunneling** — Not explicitly in 2.4; useful but may be out of scope
3. **Protocol abuse** — Not in objectives; general concept, not a discrete exam item
4. **Cryptographic attacks placement** — Downgrade, collision, and birthday are in section 29 (mapped to 2.3) but officially belong to 2.4

### What the Glossary Does Well

- Sections 25 and 26 (threat actors and malware) are **100% complete** with no gaps
- Decision rule tables are excellent study aids and correctly match exam scenarios to answers
- Depth of explanation for covered items is appropriate for exam preparation
- Social engineering section is nearly complete (just missing BEC)
- Behavioral indicators section is complete

### Recommendations

1. **Priority 1:** Add the 20 missing items listed above. Sections 30 (indicators) and 31 (mitigation) have the most gaps.
2. **Priority 2:** Move cryptographic attacks (downgrade, collision, birthday) from section 29 to section 30, or duplicate them, so they map correctly to objective 2.4.
3. **Priority 3:** Add a note that some items (SQLi, XSS, buffer overflow) appear under both 2.3 (vulnerability type) and 2.4 (attack indicator) — the exam tests them from both angles. The glossary should cover both perspectives.
4. **Low priority:** Consider removing or marking SPIM, DNS tunneling, and protocol abuse as supplementary material beyond the core objectives.

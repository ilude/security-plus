# Gap Analysis: Domain 1 & Domain 3

Coverage comparison of study materials (glossary.md, concept-walkthrough.md, notes.md) against official SY0-701 exam objectives.

**Legend:**
- **COVERED** — Topic appears in study materials with sufficient detail
- **PARTIAL** — Some aspects present but key details missing
- **MISSING** — Not covered at all

---

## Domain 1: General Security Concepts (12%)

### 1.1 — Compare and Contrast Various Types of Security Controls

| Sub-topic | Status | Notes |
|-----------|--------|-------|
| **Categories: Technical** | MISSING | Not defined in any study file. Glossary mentions technical controls indirectly (firewalls, encryption) but never names the category itself |
| **Categories: Managerial/Administrative** | MISSING | Not defined. No mention of managerial controls as a category |
| **Categories: Operational** | MISSING | Not defined as a category anywhere |
| **Categories: Physical** | MISSING | Physical security items appear under 1.2 coverage but not framed as a control category |
| **Types: Preventive** | MISSING | Not defined or listed |
| **Types: Detective** | MISSING | Not defined or listed |
| **Types: Corrective** | MISSING | Not defined or listed |
| **Types: Deterrent** | MISSING | Not defined or listed |
| **Types: Compensating** | MISSING | Mentioned once in concept-walkthrough.md ("compensating controls" for ICS/SCADA) but never defined |
| **Types: Directive** | MISSING | Not defined or listed |

**Objective 1.1 verdict: MISSING.** This entire objective has zero structured coverage. The control categories and types matrix — a foundational exam topic — is completely absent from all study files.

---

### 1.2 — Summarize Fundamental Security Concepts

| Sub-topic | Status | Notes |
|-----------|--------|-------|
| **CIA triad** | PARTIAL | Referenced in glossary intro to 1.1 controls but never explicitly defined with explanations of each component (Confidentiality, Integrity, Availability) |
| **Non-repudiation** | COVERED | Glossary section 17 defines it as digital signatures (asymmetric crypto). Also in crypto decision rules |
| **AAA (Authentication, Authorization, Accounting)** | COVERED | Glossary section 5 has full entry with definition |
| **Gap analysis** | MISSING | Not mentioned anywhere in study materials |
| **Zero Trust** | COVERED | Glossary entries for ZTNA, PDP, PEP, implicit trust zones. Concept-walkthrough covers adaptive auth vs zero trust |
| **Zero Trust: Control Plane (Adaptive identity, Threat scope reduction, Policy-driven access control)** | PARTIAL | PDP/PEP defined in glossary. "Adaptive identity" and "threat scope reduction" as specific terms are missing. Policy-driven access control not explicitly named |
| **Zero Trust: Policy Administrator** | MISSING | Not mentioned |
| **Zero Trust: Policy Engine** | MISSING | Not mentioned. PDP is listed but "Policy Engine" as a distinct component is not |
| **Zero Trust: Implicit trust zones** | COVERED | Glossary section 17 defines it |
| **Zero Trust: Subject/System** | MISSING | Not mentioned as zero trust components |
| **Zero Trust: Policy Enforcement Point** | COVERED | PEP defined in glossary section 5 |
| **Physical security: Bollards** | MISSING | Not mentioned |
| **Physical security: Access control vestibule** | MISSING | Not mentioned |
| **Physical security: Fencing** | MISSING | Not mentioned |
| **Physical security: Video surveillance** | MISSING | Not mentioned |
| **Physical security: Security guard** | MISSING | Not mentioned |
| **Physical security: Access badge** | MISSING | Not mentioned |
| **Physical security: Lighting** | MISSING | Not mentioned |
| **Physical security: Sensors (Infrared, Pressure, Microwave, Ultrasonic)** | MISSING | Not mentioned |
| **Deception tech: Honeypot** | COVERED | Glossary section 15 with definition and decision rules |
| **Deception tech: Honeynet** | COVERED | Glossary section 15 |
| **Deception tech: Honeyfile** | COVERED | Glossary section 15 |
| **Deception tech: Honeytoken** | COVERED | Glossary section 15 |

**Objective 1.2 verdict: PARTIAL.** AAA, zero trust core, non-repudiation, and deception tech are well covered. Physical security is completely missing (all 8+ sub-topics). Gap analysis concept is missing. Zero trust control plane details (Policy Administrator, Policy Engine, adaptive identity, threat scope reduction) need work. CIA triad needs explicit definitions.

---

### 1.3 — Explain the Importance of Change Management Processes

| Sub-topic | Status | Notes |
|-----------|--------|-------|
| **Approval process** | MISSING | Not mentioned |
| **Ownership** | MISSING | Not mentioned |
| **Stakeholders** | MISSING | Not mentioned |
| **Impact analysis** | MISSING | Not mentioned |
| **Test results** | MISSING | Not mentioned |
| **Backout plan** | MISSING | Not mentioned |
| **Maintenance window** | MISSING | Not mentioned |
| **Standard operating procedures** | MISSING | Not mentioned |
| **Technical implications: Allow lists/deny lists** | MISSING | Not mentioned in change management context |
| **Technical implications: Restricted activities** | MISSING | Not mentioned |
| **Technical implications: Downtime** | MISSING | Not mentioned |
| **Technical implications: Service restart** | MISSING | Not mentioned |
| **Technical implications: Application restart** | MISSING | Not mentioned |
| **Technical implications: Legacy applications** | MISSING | Not mentioned |
| **Technical implications: Dependencies** | MISSING | Not mentioned |
| **Documentation** | MISSING | Not mentioned in change management context |
| **Version control** | MISSING | Not mentioned in change management context |

**Objective 1.3 verdict: MISSING.** Entire objective is absent from all study files. Zero coverage of change management processes or their security implications.

---

### 1.4 — Explain the Importance of Using Appropriate Cryptographic Solutions

| Sub-topic | Status | Notes |
|-----------|--------|-------|
| **PKI** | COVERED | Glossary section 6: PKI, CA, CRL, OCSP, CSR, CT, CAA defined |
| **PKI: Public key / Private key** | COVERED | Implied throughout asymmetric crypto entries (RSA, ECC, DH) |
| **PKI: Key escrow** | COVERED | Glossary section 17 defines it ("third party holds copy of encryption keys") |
| **Encryption: Symmetric (AES, 3DES)** | COVERED | Glossary section 6 with decision rules |
| **Encryption: Asymmetric (RSA, ECC, DH)** | COVERED | Glossary section 6 with decision rules |
| **Encryption: Key exchange (DH, ECDHE)** | COVERED | Glossary section 6: DH, ECDHE, PFS defined |
| **Encryption levels: Full-disk, Partition, File, Volume, Database, Record** | MISSING | No mention of encryption levels/granularity |
| **Encryption: Transport/communication** | PARTIAL | TLS mentioned in EAP-TLS/PEAP context, HSTS covered. No explicit "transport encryption" category |
| **Encryption: Key length** | PARTIAL | AES entry mentions 128/192/256-bit. Not covered as a general concept |
| **Encryption: Algorithms** | COVERED | AES, 3DES, RSA, ECC, DH, ECDHE all listed |
| **Tools: TPM** | COVERED | Glossary section 6: defined with use cases |
| **Tools: HSM** | COVERED | Glossary section 6: defined with HSM vs TPM decision rule |
| **Tools: Key management system** | MISSING | Not mentioned |
| **Tools: Secure enclave** | MISSING | Not mentioned |
| **Obfuscation: Steganography** | MISSING | Not mentioned anywhere |
| **Obfuscation: Tokenization** | COVERED | Glossary section 13 with de-identification methods table |
| **Obfuscation: Data masking** | COVERED | Glossary section 13 |
| **Hashing** | COVERED | SHA, MD5, HMAC defined in glossary section 6 |
| **Salting** | COVERED | Glossary section 17 defines it |
| **Digital signatures** | COVERED | Covered in crypto decision rules (asymmetric, non-repudiation) |
| **Key stretching** | COVERED | Glossary section 17 defines it (bcrypt, PBKDF2) |
| **Blockchain** | MISSING | Not mentioned |
| **Open public ledger** | MISSING | Not mentioned |
| **Certificates: CA** | COVERED | Glossary section 6 |
| **Certificates: CRL** | COVERED | Glossary section 6 with CRL vs OCSP decision rule |
| **Certificates: OCSP** | COVERED | Glossary section 6 including OCSP stapling |
| **Certificates: Self-signed** | MISSING | Not mentioned |
| **Certificates: Third-party** | MISSING | Not explicitly discussed as a certificate type |
| **Certificates: Root of trust** | PARTIAL | CA hierarchy mentioned (Root CA > Intermediate CA > End Entity) but "root of trust" as a concept not named |
| **Certificates: CSR** | COVERED | Glossary section 6 |
| **Certificates: Wildcard** | MISSING | Not mentioned |
| **Certificates: SAN (Subject Alternative Name)** | MISSING | Not mentioned |

**Objective 1.4 verdict: PARTIAL.** Core crypto (symmetric/asymmetric/hashing/PKI) is strong. Significant gaps in encryption levels, steganography, blockchain/public ledger, key management system, secure enclave, and specific certificate types (self-signed, wildcard, SAN).

---

## Domain 1 Summary

| Objective | Coverage | Priority |
|-----------|----------|----------|
| 1.1 Security controls | MISSING | HIGH — Foundational topic, guaranteed exam questions |
| 1.2 Fundamental concepts | PARTIAL | HIGH — Physical security entirely missing |
| 1.3 Change management | MISSING | HIGH — Entire objective absent |
| 1.4 Cryptographic solutions | PARTIAL | MEDIUM — Core crypto strong, gaps in specifics |

---

## Domain 3: Security Architecture (18%)

### 3.1 — Compare and Contrast Security Implications of Different Architecture Models

| Sub-topic | Status | Notes |
|-----------|--------|-------|
| **Cloud: IaaS/PaaS/SaaS** | COVERED | Glossary section 2: all three defined with responsibility breakdown |
| **Cloud: XaaS / FaaS** | COVERED | FaaS defined in glossary as serverless |
| **Cloud: Responsibility matrix** | COVERED | Glossary section 2 "Shared Responsibility Model" with per-model breakdown |
| **Cloud: Hybrid considerations** | MISSING | Hybrid cloud not discussed |
| **Cloud: Third-party vendors** | PARTIAL | CSP mentioned; third-party vendor risk not explored in architecture context |
| **Infrastructure as Code (IaC)** | PARTIAL | Defined in glossary section 7 (Terraform, CloudFormation) but not discussed in architecture security context |
| **Serverless** | COVERED | FaaS defined with "no server management" and "no OS patching" |
| **Microservices** | MISSING | Not mentioned in any study file |
| **Network infrastructure: Physical isolation / Air-gapped** | PARTIAL | Air-gapped mentioned in ICS/SCADA context only, not as a general network concept |
| **Network infrastructure: Logical segmentation** | PARTIAL | VLAN defined in glossary section 14 but not elaborated as segmentation strategy |
| **Network infrastructure: SDN** | COVERED | Glossary section 14: "Separates control plane from data plane. Centralized programmable management" |
| **Network infrastructure: SD-WAN** | PARTIAL | Mentioned in SASE definition but not independently defined |
| **On-premises vs cloud vs hybrid** | PARTIAL | Cloud models covered, on-premises not discussed, hybrid missing |
| **Centralized vs decentralized** | MISSING | Not mentioned |
| **Containerization** | MISSING | Not mentioned in any study file |
| **Virtualization** | MISSING | Not discussed (VPC mentioned briefly but virtualization concepts absent) |
| **IoT** | COVERED | Glossary section 14: "Connected devices, large attack surface, often unpatched" |
| **ICS/SCADA** | COVERED | Glossary section 14 plus concept-walkthrough section 9 with security recommendations |
| **RTOS** | COVERED | Glossary section 14: "OS with guaranteed time constraints" |
| **Embedded systems** | MISSING | Not mentioned as a distinct topic |
| **High availability** | MISSING | Not covered under architecture (appears only in glossary as BCP/DRP context) |
| **Considerations: Availability, Resilience, Cost, Responsiveness, Scalability, Ease of deployment, Risk transference, Ease of recovery, Patch availability, Inability to patch, Power, Compute** | MISSING | None of these architecture selection considerations are discussed |

**Objective 3.1 verdict: PARTIAL.** Cloud models and responsibility matrix are strong. ICS/SCADA/IoT/RTOS covered. Major gaps in microservices, containerization, virtualization, hybrid cloud, embedded systems, and all architecture selection considerations.

---

### 3.2 — Given a Scenario, Apply Security Principles to Secure Enterprise Infrastructure

Note: The user's prompt grouped some 3.1 official topics under 3.2 and vice versa. This analysis follows the official CompTIA objective mapping.

| Sub-topic | Status | Notes |
|-----------|--------|-------|
| **Infrastructure considerations: Device placement** | MISSING | Not discussed |
| **Infrastructure considerations: Security zones** | PARTIAL | DMZ/screened subnet defined in glossary. Broader security zone concepts not covered |
| **Infrastructure considerations: Attack surface** | MISSING | Not defined or discussed |
| **Infrastructure considerations: Connectivity** | MISSING | Not discussed |
| **Infrastructure considerations: Failure modes (fail-open, fail-closed)** | MISSING | Not mentioned |
| **Infrastructure considerations: Device attributes (active/passive)** | MISSING | Not mentioned |
| **Infrastructure considerations: Device attributes (inline vs tap/monitor)** | PARTIAL | NIDS mentioned as "placed on span/mirror port or network tap" but inline vs tap not contrasted |
| **Network appliances: Jump server** | MISSING | Not mentioned |
| **Network appliances: Proxy server** | MISSING | Not mentioned independently (SWG described as "web proxy on steroids") |
| **Network appliances: IPS/IDS** | COVERED | Glossary section 1: both defined with decision rules |
| **Network appliances: Load balancer** | MISSING | Not mentioned |
| **Network appliances: Sensors** | MISSING | Not mentioned as network appliances |
| **Port security: 802.1X** | MISSING | Not mentioned |
| **Port security: EAP** | PARTIAL | EAP-TLS and PEAP defined for Wi-Fi auth but 802.1X port security not discussed |
| **Firewall types: WAF** | COVERED | Glossary sections 1 and 7 |
| **Firewall types: UTM** | MISSING | Not mentioned |
| **Firewall types: NGFW** | MISSING | Not mentioned |
| **Firewall types: Layer 4 / Layer 7** | MISSING | Not mentioned |
| **Secure communication: VPN** | COVERED | Glossary section 14 |
| **Secure communication: Tunneling (TLS, IPSec)** | PARTIAL | TLS mentioned in cert contexts. IPSec not mentioned |
| **Secure communication: SD-WAN** | PARTIAL | Mentioned in SASE context only |
| **Secure communication: SASE** | COVERED | Glossary section 2: defined as CASB + SWG + ZTNA + SD-WAN |
| **Secure baselines (establish, deploy, maintain)** | MISSING | Not discussed |
| **Hardening targets: Mobile, Workstations, Switches, Routers, Cloud, Servers, ICS/SCADA, Embedded, RTOS, IoT** | PARTIAL | ICS/SCADA hardening discussed (network monitoring, segmentation, air gapping). All other hardening targets missing |
| **Mobile solutions: MDM, BYOD, COPE, CYOD** | MISSING | Not mentioned |
| **Wireless security: WPA3, AAA/RADIUS** | COVERED | WPA3/SAE in glossary section 6. RADIUS in section 5 |
| **Application security: Input validation, Secure cookies, Static code analysis, Code signing** | PARTIAL | SAST defined (static code analysis). Input validation, secure cookies, code signing not mentioned |
| **Sandboxing** | MISSING | Not mentioned |
| **Monitoring** | PARTIAL | SIEM/SOC covered but not framed as infrastructure monitoring principle |

**Objective 3.2 verdict: PARTIAL.** IDS/IPS, WAF, VPN, SASE, wireless security well covered. Major gaps in infrastructure considerations (device placement, failure modes, attack surface), most network appliances (jump server, proxy, load balancer), firewall types (UTM, NGFW, Layer 4/7), port security (802.1X), secure baselines, hardening, mobile solutions, and sandboxing.

---

### 3.3 — Compare and Contrast Concepts and Strategies to Protect Data

| Sub-topic | Status | Notes |
|-----------|--------|-------|
| **Data types: Regulated** | PARTIAL | GDPR, HIPAA, PCI DSS mentioned but "regulated data" not defined as a category |
| **Data types: Trade secret** | MISSING | Not mentioned |
| **Data types: Intellectual property** | MISSING | Not mentioned |
| **Data types: Legal information** | MISSING | Not mentioned |
| **Data types: Financial information** | MISSING | Not mentioned |
| **Data types: Human- and non-human-readable** | MISSING | Not mentioned |
| **Data classifications: Sensitive, Confidential, Public, Restricted, Private, Critical** | MISSING | Not listed as a classification scheme. Data owner "decides classification" mentioned but the classification levels themselves are absent |
| **Data states: At rest** | MISSING | Not discussed |
| **Data states: In transit** | MISSING | Not discussed |
| **Data states: In use** | MISSING | Not discussed |
| **Data sovereignty** | MISSING | Not mentioned |
| **Geolocation** | MISSING | Not mentioned |
| **Methods: Geographic restrictions** | MISSING | Not mentioned |
| **Methods: Encryption** | PARTIAL | Encryption defined broadly but not discussed as a data protection method specifically |
| **Methods: Hashing** | PARTIAL | Defined for integrity but not framed as data protection |
| **Methods: Masking** | COVERED | Glossary section 13: data masking defined in de-identification methods |
| **Methods: Tokenization** | COVERED | Glossary section 13: defined with reversibility and use cases |
| **Methods: Obfuscation** | PARTIAL | Tokenization and masking covered under obfuscation umbrella but "obfuscation" as a general data protection concept not named |
| **Methods: Segmentation** | MISSING | Not discussed as a data protection method |
| **Methods: Permission restrictions** | MISSING | ACL defined in glossary but not discussed as data protection method |

**Objective 3.3 verdict: MISSING.** This objective has critical gaps. Data types, data classifications, data states (at rest/in transit/in use), data sovereignty, and geolocation are all absent. Only tokenization and masking have adequate coverage from the de-identification methods table.

---

### 3.4 — Explain the Importance of Resilience and Recovery in Security Architecture

| Sub-topic | Status | Notes |
|-----------|--------|-------|
| **High availability: Load balancing vs clustering** | MISSING | Neither load balancing nor clustering defined |
| **Site considerations: Hot site** | MISSING | Not mentioned |
| **Site considerations: Warm site** | MISSING | Not mentioned |
| **Site considerations: Cold site** | MISSING | Not mentioned |
| **Site considerations: Geographic dispersion** | MISSING | Not mentioned |
| **Platform diversity** | MISSING | Not mentioned |
| **Multi-cloud systems** | MISSING | Not mentioned |
| **Continuity of operations** | PARTIAL | BCP/DRP defined in glossary section 10 but COOP not explicitly named |
| **Capacity planning: People, Technology, Infrastructure** | MISSING | Not mentioned |
| **Testing: Tabletop exercises** | MISSING | Not mentioned |
| **Testing: Failover** | MISSING | Not mentioned |
| **Testing: Simulation** | MISSING | Not mentioned |
| **Testing: Parallel processing** | MISSING | Not mentioned |
| **Backups: Onsite/offsite** | MISSING | Not mentioned |
| **Backups: Frequency** | PARTIAL | RPO defined as driving backup frequency, but backup frequency itself not discussed |
| **Backups: Encryption** | MISSING | Not discussed in backup context |
| **Backups: Snapshots** | MISSING | Not mentioned |
| **Backups: Recovery** | PARTIAL | RTO/MTTR defined but backup recovery process not discussed |
| **Backups: Replication** | MISSING | Not mentioned |
| **Backups: Journaling** | MISSING | Not mentioned |
| **Power: UPS** | MISSING | Not mentioned |
| **Power: Generator** | MISSING | Not mentioned |
| **Power: Dual supply** | MISSING | Not mentioned |
| **Power: Managed PDU** | MISSING | Not mentioned |

**Objective 3.4 verdict: MISSING.** This objective is almost entirely absent. Only BCP/DRP and RPO/RTO provide tangential coverage. All site types, HA mechanisms, backup details, testing types, capacity planning, and power resiliency topics are missing.

---

## Domain 3 Summary

| Objective | Coverage | Priority |
|-----------|----------|----------|
| 3.1 Architecture models | PARTIAL | MEDIUM — Cloud/ICS strong, containers/microservices/virtualization missing |
| 3.2 Enterprise infrastructure | PARTIAL | HIGH — Most infrastructure considerations and appliance types missing |
| 3.3 Data protection | MISSING | HIGH — Data types, classifications, states all absent |
| 3.4 Resilience and recovery | MISSING | HIGH — Nearly entire objective absent |

---

## Top Priority Gaps (Across Both Domains)

These topics have ZERO coverage and are high-probability exam questions:

1. **Security control categories and types matrix** (1.1) — Foundational, guaranteed on exam
2. **Change management processes** (1.3) — Entire objective missing
3. **Physical security controls** (1.2) — All sub-topics missing
4. **Data types, classifications, and states** (3.3) — Core data protection concepts
5. **Resilience and recovery** (3.4) — Site types, HA, backups, power, testing
6. **Infrastructure considerations** (3.2) — Device placement, failure modes, attack surface
7. **Containerization and virtualization** (3.1) — Modern architecture basics
8. **Firewall types beyond WAF** (3.2) — UTM, NGFW, Layer 4/7
9. **Steganography, blockchain, encryption levels** (1.4) — Specific crypto gaps
10. **Zero Trust control plane details** (1.2) — Policy Administrator, Policy Engine, adaptive identity

---

*Analysis date: 2026-03-03*
*Sources: [CompTIA Security+ SY0-701 Exam Objectives v5.0 (PDF)](https://assets.ctfassets.net/82ripq7fjls2/6TYWUym0Nudqa8nGEnegjG/0f9b974d3b1837fe85ab8e6553f4d623/CompTIA-Security-Plus-SY0-701-Exam-Objectives.pdf), [Professor Messer SY0-701 Course](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/sy0-701-comptia-security-plus-course/), [InfoSec Institute Security+ Domains Overview](https://www.infosecinstitute.com/resources/securityplus/the-security-cbk-domains-information-and-updates/)*

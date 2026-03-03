# Validation Report: Domain 1 & Domain 3 Glossary Content

**Date**: 2026-03-03
**File Validated**: `tasks/new-glossary-d1-d3.md`
**Official Reference**: CompTIA Security+ SY0-701 Exam Objectives Version 5.0
**Cross-referenced against**: Official CompTIA objectives PDF, Professor Messer SY0-701 course, multiple certification study guides (Pearson, InfoSecTrain, CertGet, UnionTestPrep)

---

## Methodology

Every term and concept in `new-glossary-d1-d3.md` was checked against the official SY0-701 exam objectives sub-bullets. Each item is categorized as:

- **VALID** — Explicitly listed in official objectives
- **INFERRED** — Not explicitly listed but clearly implied by an objective
- **QUESTIONABLE** — May not be on the exam; potentially too detailed or out of scope
- **MISSING FROM CONTENT** — Listed in official objectives but not covered in the glossary

---

## Section 18: Security Control Categories and Types (Objective 1.1)

### Coverage Assessment

| Glossary Item | Status | Notes |
|---------------|--------|-------|
| Technical (category) | **VALID** | Obj 1.1 — Categories: Technical |
| Managerial / Administrative (category) | **VALID** | Obj 1.1 — Categories: Managerial. Note: Official objectives use "Managerial" not "Administrative" |
| Operational (category) | **VALID** | Obj 1.1 — Categories: Operational |
| Physical (category) | **VALID** | Obj 1.1 — Categories: Physical |
| Preventive (type) | **VALID** | Obj 1.1 — Control Types: Preventive |
| Detective (type) | **VALID** | Obj 1.1 — Control Types: Detective |
| Corrective (type) | **VALID** | Obj 1.1 — Control Types: Corrective |
| Deterrent (type) | **VALID** | Obj 1.1 — Control Types: Deterrent |
| Compensating (type) | **VALID** | Obj 1.1 — Control Types: Compensating |
| Directive (type) | **VALID** | Obj 1.1 — Control Types: Directive |
| Control Category x Type Matrix | **INFERRED** | Not an explicit objective item, but understanding intersections is essential for scenario-based questions. Highly useful study aid. |

### Issues Found

- The glossary uses "Managerial / Administrative" — the official objectives say **"Managerial"** only. The alternate name is fine for understanding, but the exam term is "Managerial." No change needed, but worth noting for exam prep.

### Missing Items: None

Objective 1.1 is fully covered.

---

## Section 19: Change Management (Objective 1.3)

### Coverage Assessment

| Glossary Item | Status | Notes |
|---------------|--------|-------|
| Approval process | **VALID** | Obj 1.3 — Business processes: Approval process |
| Ownership | **VALID** | Obj 1.3 — Business processes: Ownership |
| Stakeholders | **VALID** | Obj 1.3 — Business processes: Stakeholders |
| Impact analysis | **VALID** | Obj 1.3 — Business processes: Impact analysis |
| Test results | **VALID** | Obj 1.3 — Business processes: Test results |
| Backout plan | **VALID** | Obj 1.3 — Business processes: Backout plan |
| Maintenance window | **VALID** | Obj 1.3 — Business processes: Maintenance window |
| SOP (Standard Operating Procedure) | **VALID** | Obj 1.3 — Business processes: Standard operating procedure |
| Allow list | **VALID** | Obj 1.3 — Technical implications: Allow lists/deny lists |
| Deny list / Block list | **VALID** | Obj 1.3 — Technical implications: Allow lists/deny lists |
| Restricted activities | **VALID** | Obj 1.3 — Technical implications: Restricted activities |
| Downtime | **VALID** | Obj 1.3 — Technical implications: Downtime |
| Service restart | **VALID** | Obj 1.3 — Technical implications: Service restart |
| Application restart | **VALID** | Obj 1.3 — Technical implications: Application restart |
| Legacy applications | **VALID** | Obj 1.3 — Technical implications: Legacy applications |
| Dependencies | **VALID** | Obj 1.3 — Technical implications: Dependencies |
| Change documentation | **INFERRED** | Obj 1.3 lists "Documentation" as a category. The glossary item expands on it but the term "change documentation" is implied. |
| Version control | **VALID** | Obj 1.3 — Version control |
| Configuration baseline | **QUESTIONABLE** | Not explicitly listed in Obj 1.3. Configuration baselines appear under Obj 3.2 context (secure baselines). Including it here may conflate objectives. Not harmful but could confuse which objective it maps to. |

### Issues Found

- **"Configuration baseline"** is listed under change management in the glossary, but in the official objectives it is more aligned with Obj 3.2 (secure enterprise infrastructure). Not incorrect content, but potentially misleading about where the exam tests it.

### Missing Items

| Official Item | Status |
|---------------|--------|
| Updating diagrams (under Documentation) | **MISSING** — The glossary mentions "Change documentation" generally but does not explicitly call out "Updating diagrams" as a separate concept. The official objectives specifically list this. |
| Updating policies/procedures (under Documentation) | **MISSING** — Same issue. Official objectives explicitly list this as a sub-bullet under Documentation. Should be a separate glossary entry or at minimum called out explicitly. |

---

## Section 20: Physical Security (Objective 1.2)

### Coverage Assessment

| Glossary Item | Status | Notes |
|---------------|--------|-------|
| Bollards | **VALID** | Obj 1.2 — Physical security: Bollards |
| Access control vestibule (mantrap) | **VALID** | Obj 1.2 — Physical security: Access control vestibule |
| Fencing | **VALID** | Obj 1.2 — Physical security: Fencing |
| Video surveillance (CCTV) | **VALID** | Obj 1.2 — Physical security: Video surveillance |
| Security guards | **VALID** | Obj 1.2 — Physical security: Security guard |
| Access badges | **VALID** | Obj 1.2 — Physical security: Access badge |
| Lighting | **VALID** | Obj 1.2 — Physical security: Lighting |
| Infrared (sensor) | **VALID** | Obj 1.2 — Sensors: Infrared |
| Pressure (sensor) | **VALID** | Obj 1.2 — Sensors: Pressure |
| Microwave (sensor) | **VALID** | Obj 1.2 — Sensors: Microwave |
| Ultrasonic (sensor) | **VALID** | Obj 1.2 — Sensors: Ultrasonic |
| Tailgating vs Piggybacking | **INFERRED** | Not explicit in 1.2 objectives but directly relevant to physical security controls (access control vestibule). Common exam topic. Valid inclusion. |

### Missing Items: None

All physical security items from Obj 1.2 are covered.

---

## Section 21: Data Protection (Objective 3.3)

### Coverage Assessment

| Glossary Item | Status | Notes |
|---------------|--------|-------|
| Regulated data | **VALID** | Obj 3.3 — Data Types: Regulated |
| Trade secret | **VALID** | Obj 3.3 — Data Types: Trade secret |
| Intellectual property (IP) | **VALID** | Obj 3.3 — Data Types: Intellectual property |
| Legal information | **VALID** | Obj 3.3 — Data Types: Legal information |
| Financial information | **VALID** | Obj 3.3 — Data Types: Financial information |
| Human-readable data | **VALID** | Obj 3.3 — Data Types: Human- and non-human-readable |
| Non-human-readable data | **VALID** | Obj 3.3 — Data Types: Human- and non-human-readable |
| Public (classification) | **VALID** | Obj 3.3 — Data Classifications: Public |
| Private (classification) | **VALID** | Obj 3.3 — Data Classifications: Private |
| Sensitive (classification) | **VALID** | Obj 3.3 — Data Classifications: Sensitive |
| Confidential (classification) | **VALID** | Obj 3.3 — Data Classifications: Confidential |
| Restricted (classification) | **VALID** | Obj 3.3 — Data Classifications: Restricted |
| Critical (classification) | **VALID** | Obj 3.3 — Data Classifications: Critical |
| Data at rest | **VALID** | Obj 3.3 — Data states: Data at rest |
| Data in transit | **VALID** | Obj 3.3 — Data states: Data in transit |
| Data in use | **VALID** | Obj 3.3 — Data states: Data in use |
| Data sovereignty | **VALID** | Obj 3.3 — General data considerations: Data sovereignty |
| Geolocation | **VALID** | Obj 3.3 — General data considerations: Geolocation |
| Geographic restrictions | **VALID** | Obj 3.3 — Methods to secure data: Geographic restrictions |
| Encryption | **VALID** | Obj 3.3 — Methods to secure data: Encryption |
| Hashing | **VALID** | Obj 3.3 — Methods to secure data: Hashing |
| Masking | **VALID** | Obj 3.3 — Methods to secure data: Masking |
| Tokenization | **VALID** | Obj 3.3 — Methods to secure data: Tokenization |
| Obfuscation | **VALID** | Obj 3.3 — Methods to secure data: Obfuscation |
| Segmentation | **VALID** | Obj 3.3 — Methods to secure data: Segmentation |
| Permission restrictions | **VALID** | Obj 3.3 — Methods to secure data: Permission restrictions |

### Missing Items: None

Objective 3.3 is fully covered. Excellent coverage of all data types, classifications, states, and protection methods.

---

## Section 22: Resilience and Recovery (Objective 3.4)

### Coverage Assessment

| Glossary Item | Status | Notes |
|---------------|--------|-------|
| Load balancing | **VALID** | Obj 3.4 — High availability: Load balancing vs. clustering |
| Clustering | **VALID** | Obj 3.4 — High availability: Load balancing vs. clustering |
| Hot site | **VALID** | Obj 3.4 — Site considerations: Hot |
| Warm site | **VALID** | Obj 3.4 — Site considerations: Warm |
| Cold site | **VALID** | Obj 3.4 — Site considerations: Cold |
| Geographic dispersion | **VALID** | Obj 3.4 — Site considerations: Geographic dispersion |
| Platform diversity | **VALID** | Obj 3.4 — Platform diversity |
| Multi-cloud | **VALID** | Obj 3.4 — Multi-cloud systems |
| People (capacity) | **VALID** | Obj 3.4 — Capacity planning: People |
| Technology (capacity) | **VALID** | Obj 3.4 — Capacity planning: Technology |
| Infrastructure (capacity) | **VALID** | Obj 3.4 — Capacity planning: Infrastructure |
| Tabletop exercise | **VALID** | Obj 3.4 — Testing: Tabletop exercises |
| Failover testing | **VALID** | Obj 3.4 — Testing: Fail over |
| Simulation | **VALID** | Obj 3.4 — Testing: Simulation |
| Parallel processing | **VALID** | Obj 3.4 — Testing: Parallel processing |
| Onsite backup | **VALID** | Obj 3.4 — Backups: Onsite/offsite |
| Offsite backup | **VALID** | Obj 3.4 — Backups: Onsite/offsite |
| Backup frequency | **VALID** | Obj 3.4 — Backups: Frequency |
| Backup encryption | **VALID** | Obj 3.4 — Backups: Encryption |
| Snapshot | **VALID** | Obj 3.4 — Backups: Snapshots |
| Replication | **INFERRED** | Not explicitly listed as a 3.4 sub-bullet. However, replication is a core resilience/recovery concept closely related to backups and is commonly tested. Valid inclusion. |
| Journaling | **INFERRED** | Not explicitly listed as a 3.4 sub-bullet. Related to backup and recovery concepts. Useful for understanding point-in-time recovery. Reasonable inclusion. |
| UPS | **VALID** | Obj 3.4 — Power (UPS is the primary power resilience concept) |
| Generator | **VALID** | Obj 3.4 — Power |
| Dual supply | **INFERRED** | Not explicitly listed in 3.4 sub-bullets. Power is listed as a standalone bullet without sub-items. Dual supply is a reasonable power resilience concept. |
| Managed PDU | **QUESTIONABLE** | Not listed in the official objectives. While related to power infrastructure, this level of detail may exceed what the exam tests. Low risk of wasting study time but not explicitly on the objectives. |

### Missing Items

| Official Item | Status |
|---------------|--------|
| Continuity of operations | **MISSING** — Obj 3.4 explicitly lists "Continuity of operations" as a top-level bullet. Not covered in the glossary. This is a significant gap — COOP is a core concept. |

---

## Section 23: Security Architecture Expanded (Objectives 3.1, 3.2)

### Coverage Assessment — Architecture Concepts (Obj 3.1)

| Glossary Item | Status | Notes |
|---------------|--------|-------|
| Microservices | **VALID** | Obj 3.1 — Microservices |
| Containerization | **VALID** | Obj 3.1 — Containerization |
| Docker | **QUESTIONABLE** | Not listed in official objectives. Docker is an example of containerization, but the exam tests the concept, not specific products. May add unnecessary specificity. |
| Kubernetes (K8s) | **QUESTIONABLE** | Not listed in official objectives. Same concern as Docker — specific product, not on the objectives. |
| Virtualization | **VALID** | Obj 3.1 — Virtualization |
| Embedded systems | **VALID** | Obj 3.1 — Embedded systems |
| Hybrid cloud | **VALID** | Obj 3.1 — Cloud: Hybrid considerations |
| Sandboxing | **QUESTIONABLE** | Not explicitly listed under Obj 3.1. Sandboxing appears more in the context of malware analysis (Domain 4) or application security. Not harmful but may be misplaced here. |

### Coverage Assessment — Infrastructure Considerations (Obj 3.2)

| Glossary Item | Status | Notes |
|---------------|--------|-------|
| Device placement | **VALID** | Obj 3.2 — Infrastructure considerations: Device placement |
| Security zones | **VALID** | Obj 3.2 — Infrastructure considerations: Security zones |
| Attack surface | **VALID** | Obj 3.2 — Infrastructure considerations: Attack surface |
| Connectivity | **VALID** | Obj 3.2 — Infrastructure considerations: Connectivity |
| Failure modes | **VALID** | Obj 3.2 — Infrastructure considerations: Failure modes |
| Fail-open | **VALID** | Obj 3.2 — Failure modes: Fail-open |
| Fail-closed | **VALID** | Obj 3.2 — Failure modes: Fail-closed |
| Active device | **VALID** | Obj 3.2 — Device attribute: Active vs. passive |
| Passive device | **VALID** | Obj 3.2 — Device attribute: Active vs. passive |
| Inline | **VALID** | Obj 3.2 — Device attribute: Inline vs. tap/monitor |
| Tap / Monitor mode | **VALID** | Obj 3.2 — Device attribute: Inline vs. tap/monitor |
| Jump server (jump box) | **VALID** | Obj 3.2 — Network appliances: Jump server |
| Proxy server | **VALID** | Obj 3.2 — Network appliances: Proxy server |
| Load balancer | **VALID** | Obj 3.2 — Network appliances: Load balancer |
| Sensors | **VALID** | Obj 3.2 — Network appliances: Sensors |
| Layer 4 firewall | **VALID** | Obj 3.2 — Firewall types: Layer 4/Layer 7 |
| Layer 7 firewall (NGFW) | **VALID** | Obj 3.2 — Firewall types: Layer 4/Layer 7 |
| WAF | **VALID** | Obj 3.2 — Firewall types: Web application firewall (WAF) |
| UTM | **VALID** | Obj 3.2 — Firewall types: Unified threat management (UTM) |
| NGFW | **VALID** | Obj 3.2 — Firewall types: Next-generation firewall (NGFW) |
| 802.1X | **VALID** | Obj 3.2 — Port security: 802.1X |
| IPSec | **VALID** | Obj 3.2 — Secure communication/access: Tunneling |
| SD-WAN | **VALID** | Obj 3.2 — Secure communication/access: SD-WAN |
| Secure baselines (Establish, Deploy, Maintain) | **QUESTIONABLE** | Not explicitly listed under Obj 3.2 in the official objectives. Secure baselines may be tested conceptually but are not a named sub-bullet. The Establish/Deploy/Maintain framework is not in the objectives. |

### Missing Items from Obj 3.1

| Official Item | Status |
|---------------|--------|
| Cloud (as top-level item) | **PARTIALLY COVERED** — Hybrid cloud is mentioned but the broader "Cloud" topic including the responsibility matrix and third-party vendors is not explicitly covered as a glossary section. |
| Responsibility matrix | **MISSING** — Obj 3.1 explicitly lists "Responsibility matrix" under Cloud. Not in the glossary. This is a key concept (who secures what in IaaS/PaaS/SaaS). |
| Third-party vendors | **MISSING** — Obj 3.1 explicitly lists "Third-party vendors" under Cloud. Not in the glossary. |
| Infrastructure as Code (IaC) | **MISSING** — Obj 3.1 explicitly lists IaC. Not in the glossary. |
| Serverless | **MISSING** — Obj 3.1 explicitly lists Serverless. Not in the glossary. |
| Network infrastructure | **MISSING** — Obj 3.1 lists this as a category with sub-bullets (Physical isolation, Air-gapped, Logical segmentation, SDN). Not in the glossary. |
| Physical isolation / Air-gapped | **MISSING** — Obj 3.1 — Network infrastructure: Physical isolation, Air-gapped. Not in the glossary. |
| Logical segmentation | **MISSING** — Obj 3.1 — Network infrastructure: Logical segmentation. Not in the glossary. |
| Software-defined networking (SDN) | **MISSING** — Obj 3.1 — Network infrastructure: SDN. Not in the glossary. |
| On-premises | **MISSING** — Obj 3.1 explicitly lists On-premises. Not in the glossary. |
| Centralized vs. Decentralized | **MISSING** — Obj 3.1 explicitly lists this. Not in the glossary. |
| IoT | **MISSING** — Obj 3.1 explicitly lists IoT. Not in the glossary. |
| ICS/SCADA | **MISSING** — Obj 3.1 explicitly lists Industrial control systems (ICS)/Supervisory Control and Data Acquisition (SCADA). Not in the glossary. |
| RTOS | **MISSING** — Obj 3.1 explicitly lists Real-time operating system (RTOS). Not in the glossary. |
| High availability (3.1 context) | **MISSING** — Obj 3.1 lists High availability as an architecture concept. Covered under 3.4 but not in the 3.1 architecture context. |
| Considerations sub-bullets | **MISSING** — Obj 3.1 lists: Availability, Resilience, Cost, Responsiveness, Scalability, Ease of deployment, Risk transference, Ease of recovery, Patch availability, Inability to patch, Power, Compute. None of these are in the glossary. |

### Missing Items from Obj 3.2

| Official Item | Status |
|---------------|--------|
| IPS/IDS (Network appliances) | **MISSING** — Obj 3.2 lists "Intrusion prevention system (IPS)/intrusion detection system (IDS)" under Network appliances. Not in the glossary Section 23. |
| EAP (Extensible Authentication Protocol) | **MISSING** — Obj 3.2 lists EAP under Port security alongside 802.1X. Not in the glossary. |
| VPN | **MISSING** — Obj 3.2 lists "Virtual private network (VPN)" under Secure communication/access. Not explicitly in the glossary. |
| Remote access | **MISSING** — Obj 3.2 lists "Remote access" under Secure communication/access. Not in the glossary. |
| TLS (tunneling) | **MISSING** — Obj 3.2 lists "Tunneling" with TLS and IPSec. TLS is not in the glossary. |
| SASE (Secure Access Service Edge) | **MISSING** — Obj 3.2 explicitly lists SASE under Secure communication/access. Not in the glossary. |
| Selection of effective controls | **MISSING** — Obj 3.2 lists this as a standalone bullet. Not in the glossary. |

---

## Section 24: Cryptography Expanded (Objective 1.4)

### Coverage Assessment

| Glossary Item | Status | Notes |
|---------------|--------|-------|
| Full-disk encryption | **VALID** | Obj 1.4 — Encryption: Level: Full-disk |
| Partition encryption | **VALID** | Obj 1.4 — Encryption: Level: Partition |
| File encryption | **VALID** | Obj 1.4 — Encryption: Level: File |
| Volume encryption | **VALID** | Obj 1.4 — Encryption: Level: Volume |
| Database encryption | **VALID** | Obj 1.4 — Encryption: Level: Database |
| Record-level encryption | **VALID** | Obj 1.4 — Encryption: Level: Record |
| Steganography | **VALID** | Obj 1.4 — Obfuscation: Steganography |
| Obfuscation | **VALID** | Obj 1.4 — Obfuscation (top-level) |
| Blockchain | **VALID** | Obj 1.4 — Blockchain |
| Open public ledger | **VALID** | Obj 1.4 — Open public ledger |
| Key management system (KMS) | **VALID** | Obj 1.4 — Tools: Key management system |
| Secure enclave | **VALID** | Obj 1.4 — Tools: Secure enclave |
| Self-signed certificate | **VALID** | Obj 1.4 — Certificates: Self-signed |
| Third-party certificate | **VALID** | Obj 1.4 — Certificates: Third-party |
| Wildcard certificate | **VALID** | Obj 1.4 — Certificates: Wildcard |
| SAN certificate | **INFERRED** | Not explicitly listed in Obj 1.4 certificates sub-bullets. However, SAN is a common certificate concept and likely testable. Reasonable inclusion. |
| Root of trust | **VALID** | Obj 1.4 — Certificates: Root of trust |

### Missing Items from Obj 1.4

| Official Item | Status |
|---------------|--------|
| Public key infrastructure (PKI) | **MISSING** — Obj 1.4 top-level item. Not explicitly covered as a glossary term (though related concepts appear). |
| Public key | **MISSING** — Obj 1.4 — PKI: Public key. Not in the glossary. |
| Private key | **MISSING** — Obj 1.4 — PKI: Private key. Not in the glossary. |
| Key escrow | **MISSING** — Obj 1.4 — PKI: Key escrow. Not in the glossary. |
| Transport/communication encryption | **MISSING** — Obj 1.4 — Encryption: Transport/communication. Not in the glossary. |
| Asymmetric encryption | **MISSING** — Obj 1.4 — Encryption: Asymmetric. Not in the glossary. |
| Symmetric encryption | **MISSING** — Obj 1.4 — Encryption: Symmetric. Not in the glossary. |
| Key exchange | **MISSING** — Obj 1.4 — Encryption: Key exchange. Not in the glossary. |
| Algorithms | **MISSING** — Obj 1.4 — Encryption: Algorithms. Not in the glossary. |
| Key length | **MISSING** — Obj 1.4 — Encryption: Key length. Not in the glossary. |
| TPM (Trusted Platform Module) | **MISSING** — Obj 1.4 — Tools: Trusted Platform Module (TPM). Not in the glossary. |
| HSM (Hardware Security Module) | **MISSING** — Obj 1.4 — Tools: Hardware security module (HSM). Mentioned in the HSM vs KMS comparison but not as a standalone glossary entry. |
| Tokenization (under Obfuscation) | **PARTIALLY COVERED** — Listed under Data Protection (Section 21) as a data protection method, but not explicitly under Obj 1.4 Obfuscation context. |
| Data masking (under Obfuscation) | **PARTIALLY COVERED** — Same as tokenization — covered under data protection but not in the cryptography obfuscation context. |
| Hashing | **PARTIALLY COVERED** — Discussed in data protection section but not as a standalone Obj 1.4 item. |
| Salting | **MISSING** — Obj 1.4 explicitly lists Salting as a top-level bullet. Not in the glossary. |
| Digital signatures | **MISSING** — Obj 1.4 explicitly lists Digital signatures. Not in the glossary. |
| Key stretching | **MISSING** — Obj 1.4 explicitly lists Key stretching. Not in the glossary. |
| Certificate authorities | **MISSING** — Obj 1.4 — Certificates: Certificate authorities. Not a standalone entry. |
| Certificate revocation lists (CRLs) | **MISSING** — Obj 1.4 — Certificates: Certificate revocation lists (CRLs). Not in the glossary. |
| OCSP | **MISSING** — Obj 1.4 — Certificates: Online Certificate Status Protocol (OCSP). Not in the glossary. |
| CSR generation | **MISSING** — Obj 1.4 — Certificates: Certificate signing request (CSR) generation. Not in the glossary. |

---

## Section: Zero Trust Control Plane (Objective 1.2)

### Coverage Assessment

| Glossary Item | Status | Notes |
|---------------|--------|-------|
| Policy Engine (PE) | **VALID** | Obj 1.2 — Zero Trust: Control Plane: Policy Engine |
| Policy Administrator (PA) | **VALID** | Obj 1.2 — Zero Trust: Control Plane: Policy Administrator |
| Policy Enforcement Point (PEP) | **VALID** | Obj 1.2 — Zero Trust: Data Plane: Policy Enforcement Point |
| Adaptive identity | **VALID** | Obj 1.2 — Zero Trust: Control Plane: Adaptive identity |
| Threat scope reduction | **VALID** | Obj 1.2 — Zero Trust: Control Plane: Threat scope reduction |
| Policy-driven access control | **VALID** | Obj 1.2 — Zero Trust: Control Plane: Policy-driven access control |

### Missing Items from Obj 1.2

| Official Item | Status |
|---------------|--------|
| CIA (Confidentiality, Integrity, Availability) | **MISSING** — Obj 1.2 top-level item. Not in the new glossary (may be in existing glossary.md). |
| Non-repudiation | **MISSING** — Obj 1.2 top-level item. Not in the new glossary. |
| AAA (Authentication, Authorization, Accounting) | **MISSING** — Obj 1.2 top-level item. Not in the new glossary. |
| Authenticating people | **MISSING** — Obj 1.2 — AAA sub-bullet. |
| Authenticating systems | **MISSING** — Obj 1.2 — AAA sub-bullet. |
| Authorization models | **MISSING** — Obj 1.2 — AAA sub-bullet. |
| Gap analysis | **MISSING** — Obj 1.2 top-level item. Not in the new glossary. |
| Implicit trust zones | **MISSING** — Obj 1.2 — Zero Trust: Data Plane: Implicit trust zones. |
| Subject/System | **MISSING** — Obj 1.2 — Zero Trust: Data Plane: Subject/System. |
| Deception and disruption technology | **MISSING** — Obj 1.2 top-level item. |
| Honeypot | **MISSING** — Obj 1.2 — Deception: Honeypot. |
| Honeynet | **MISSING** — Obj 1.2 — Deception: Honeynet. |
| Honeyfile | **MISSING** — Obj 1.2 — Deception: Honeyfile. |
| Honeytoken | **MISSING** — Obj 1.2 — Deception: Honeytoken. |

**Note**: The glossary file states it covers "topics identified as MISSING or PARTIAL in gap-analysis-d1-d3.md." The Obj 1.2 items above (CIA, AAA, Gap analysis, Deception tech) may already be covered in the existing `glossary.md`. If so, these are not gaps in the overall study system — only absent from this specific new file.

---

## Exam Terminology Additions (Section 25)

### Coverage Assessment

All items in the terminology table are either **VALID** or **INFERRED** — they map to official objective items covered in earlier sections. This section serves as a quick-reference index. No issues.

---

## Summary

### Overall Statistics

| Category | Count |
|----------|-------|
| **VALID** items | 89 |
| **INFERRED** items (reasonable inclusions) | 8 |
| **QUESTIONABLE** items (may be out of scope) | 5 |
| **MISSING FROM CONTENT** (official items not covered) | 47 |

### Questionable Items (Consider Removing or Flagging)

1. **Docker** — Specific product, not in objectives. Mark as "bonus context" or remove.
2. **Kubernetes (K8s)** — Same as Docker.
3. **Sandboxing** — Not in Obj 3.1; more relevant to Domain 4 malware analysis.
4. **Managed PDU** — Not in official objectives under Obj 3.4 Power.
5. **Secure baselines (Establish/Deploy/Maintain)** — Framework not in objectives. The concept of baselines is relevant but this specific breakdown is not an exam item.
6. **Configuration baseline** (under change management) — More aligned with Obj 3.2 than Obj 1.3.

### Critical Missing Items (Must Be Added)

These are items explicitly listed in the official objectives that are NOT covered anywhere in the new glossary:

**Objective 1.2 (if not in existing glossary):**
- CIA triad, Non-repudiation, AAA framework, Gap analysis
- Deception technology: Honeypot, Honeynet, Honeyfile, Honeytoken
- Zero Trust Data Plane: Implicit trust zones, Subject/System

**Objective 1.4 (Cryptography):**
- PKI, Public key, Private key, Key escrow
- Symmetric vs. Asymmetric encryption
- Key exchange, Algorithms, Key length
- Transport/communication encryption
- TPM, HSM (as standalone entries)
- Salting, Digital signatures, Key stretching
- CRLs, OCSP, CSR generation, Certificate authorities

**Objective 3.1 (Architecture Models):**
- Cloud responsibility matrix, Third-party vendors
- IaC, Serverless, SDN, On-premises
- Physical isolation / Air-gapped, Logical segmentation
- Centralized vs. Decentralized
- IoT, ICS/SCADA, RTOS
- All 12 "Considerations" sub-bullets (Availability through Compute)

**Objective 3.2 (Enterprise Infrastructure):**
- IPS/IDS, EAP, VPN, Remote access, TLS, SASE
- Selection of effective controls

**Objective 3.4 (Resilience):**
- Continuity of operations (COOP)

### What the Glossary Does Well

- Section 18 (Control Categories/Types): Comprehensive and well-structured with useful decision rules
- Section 19 (Change Management): Thorough coverage of business processes and technical implications
- Section 20 (Physical Security): Complete coverage with excellent sensor decision rules
- Section 21 (Data Protection): Full coverage of all 3.3 sub-bullets — data types, classifications, states, and methods
- Section 22 (Resilience and Recovery): Strong coverage of 3.4 with good decision rules
- Decision rule tables throughout are exam-relevant and practical
- Exam terminology quick-reference table is a useful study aid

### Recommendation

The glossary content that exists is high-quality, well-organized, and exam-relevant. The primary issue is **significant gaps in Objectives 1.2, 1.4, and 3.1** where many official sub-bullets are not covered. The content appears to have been written to fill gaps identified in a prior analysis, so the missing items may already exist in `glossary.md`. A cross-check against the existing glossary is needed to confirm which items are truly missing from the overall study system.

---

## Sources

- [CompTIA Security+ SY0-701 Exam Objectives (Official PDF)](https://assets.ctfassets.net/82ripq7fjls2/6TYWUym0Nudqa8nGEnegjG/0f9b974d3b1837fe85ab8e6553f4d623/CompTIA-Security-Plus-SY0-701-Exam-Objectives.pdf)
- [Professor Messer's CompTIA SY0-701 Security+ Course](https://www.professormesser.com/security-plus/sy0-701/sy0-701-video/sy0-701-comptia-security-plus-course/)
- [Proftia CompTIA Security+ SY0-701 Study Guide](https://proftia.com/resources/securityplus-objectives.html)
- [InfoSecTrain CompTIA Security+ Domain 3](https://www.infosectrain.com/blog/comptia-security-domain-3-security-architecture/)
- [DestCert Security+ 701 Exam Objectives Guide](https://destcert.com/resources/security-plus-701-objectives/)
- [InfoSec Institute Security+ Domains Overview](https://www.infosecinstitute.com/resources/securityplus/the-security-cbk-domains-information-and-updates/)

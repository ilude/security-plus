# New Glossary Sections — Domain 1 & Domain 3 Gap Coverage

Continuing from section 17 in glossary.md. Covers all topics identified as MISSING or PARTIAL in gap-analysis-d1-d3.md.

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

## Exam Terminology Additions (Supplement to Section 17)

| Exam Says | Means |
|-----------|-------|
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

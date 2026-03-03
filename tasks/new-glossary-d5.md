# New Glossary Sections — Domain 5 Gap Fill

These sections extend the existing glossary. Add after section 17.

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

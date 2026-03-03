# Domain 2 New Glossary Sections

New content covering gaps identified in gap-analysis-d2.md. Add to glossary.md after section 17.

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

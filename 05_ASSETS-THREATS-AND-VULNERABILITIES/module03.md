# 🛡️ Course 5 — Module 3: Vulnerabilities in Systems

> Identifying system vulnerabilities, understanding vulnerability scanning and penetration testing, applying an attacker mindset, recognizing attack vectors and threat actors, and defending against brute-force attacks.

---

## 🔎 Identify System Vulnerabilities

### Vulnerability Assessment

A **vulnerability assessment** is the internal review process used to identify weaknesses in an organization's security systems.

### Vulnerability Assessment Process

1. **Identification** — Find vulnerabilities and weaknesses.
2. **Vulnerability Analysis** — Research and understand the vulnerabilities.
3. **Risk Assessment** — Determine severity, likelihood, and potential impact.
4. **Remediation** — Address the vulnerabilities and reduce the associated risk.

### 🧪 Hands-on Activity — Vulnerability Assessment

Completed a practical vulnerability assessment activity and created a **vulnerability assessment report** documenting findings and recommended remediation.

---

## 🔍 Vulnerability Scanning

### Vulnerability Scanner

A **vulnerability scanner** is software that automatically compares known vulnerabilities and exposures against technologies on a network.

Scanners commonly identify:
- Misconfigurations
- Known vulnerabilities
- Programming flaws
- Exposed services and systems

### Five Attack Surface Layers

1. **Perimeter layer** — authentication systems and externally exposed entry points
2. **Network layer** — firewalls and network infrastructure
3. **Endpoint layer** — laptops, desktops, servers, and other devices
4. **Application layer** — software users interact with
5. **Data layer** — information stored, in transit, or in use

### Types of Vulnerability Scans

#### External vs Internal

- **External scans** examine systems from outside the internal network, such as public websites, firewalls, ports, and servers.
- **Internal scans** examine weaknesses from within the organization's environment, such as application weaknesses or internal systems.

#### Authenticated vs Unauthenticated

- **Authenticated scans** use valid credentials to inspect systems with user or administrative access.
- **Unauthenticated scans** simulate an outsider without authorized access.

#### Limited vs Comprehensive

- **Limited scans** focus on specific devices or systems, such as checking a firewall for misconfigurations.
- **Comprehensive scans** examine all devices and technologies within the defined network scope.

### Discovery Scanning

**Discovery scanning** identifies computers, devices, services, and open ports before limited or comprehensive vulnerability scans are performed.

> Vulnerability scanners are designed to be non-intrusive, but scans can occasionally cause unexpected issues such as system instability or crashes.

---

## 🔄 The Importance of Updates

Updates are an important part of vulnerability remediation because they address security weaknesses in software and operating systems.

### Patch Update

A **patch** is a software or operating-system update that addresses bugs or security vulnerabilities.

Patches may address known vulnerabilities before attackers discover them. In some cases, patches are developed after a **zero-day** vulnerability becomes known.

### Manual Updates

Updates are obtained and installed manually by users or IT teams.

**Advantage:**
- Greater control over when updates are deployed

**Disadvantage:**
- Critical updates can be forgotten or delayed

### Automatic Updates

The system or application automatically finds, downloads, and installs available updates.

**Advantages:**
- Simplifies deployment
- Helps keep systems current

**Disadvantage:**
- Poorly tested patches can cause instability or compatibility issues

### End-of-Life (EOL) Software

Software becomes **end-of-life** when the manufacturer stops supporting it.

EOL software is risky because:
- Security patches may no longer be available
- Newly discovered vulnerabilities may remain unfixable
- Attackers can exploit outdated technology

> **Patch vs Upgrade:** A patch fixes or improves an existing version; an upgrade generally moves to a newer major version of the software or hardware.

### Example — WannaCry

The 2017 WannaCry ransomware outbreak demonstrated the importance of timely patching. Systems that had not installed an available security patch were exposed to a vulnerability that attackers could exploit.

---

## 🧪 Penetration Testing

A **penetration test (pen test)** is an authorized simulated attack used to identify vulnerabilities and determine their potential consequences.

### Vulnerability Assessment vs Penetration Test

| Vulnerability Assessment | Penetration Test |
|---|---|
| Finds weaknesses | Exploits weaknesses in an authorized test |
| Focuses on identifying vulnerabilities | Focuses on validating impact and attack paths |
| Helps prioritize remediation | Shows what an attacker could potentially achieve |

### Red, Blue & Purple Team Testing

- **Red team** — simulates attacks to identify weaknesses.
- **Blue team** — focuses on defense and incident response.
- **Purple team** — combines red and blue team efforts collaboratively to improve security.

### Penetration Testing Strategies

#### Open-Box / White-Box

The tester has extensive knowledge and privileged access, such as:
- System architecture
- Data flows
- Network diagrams

#### Closed-Box / Black-Box

The tester has little or no internal information, closely simulating an external attacker.

#### Partial-Knowledge / Gray-Box

The tester has limited knowledge or access, such as the level available to a normal internal user.

### Bug Bounty Programs

Organizations may reward ethical hackers for finding and responsibly reporting vulnerabilities in their products.

---

## 🧠 Cyber Attacker Mindset

An **attacker mindset** means analyzing systems from the perspective of someone trying to bypass defenses, gain access, or cause harm.

The goal is not to attack recklessly, but to understand how weaknesses could be exploited so they can be addressed proactively.

### Attack Simulations

#### Proactive Simulation

Assumes the role of an attacker and attempts to exploit vulnerabilities.

Often associated with **red team exercises**.

#### Reactive Simulation

Assumes the role of a defender responding to an attack and assessing weaknesses.

Often relies on vulnerability scanning and security analysis.

### Using Vulnerability Findings

A vulnerability assessment can be used to guide attacker-mindset analysis:

1. Identify a vulnerable asset.
2. Analyze the vulnerability.
3. Assess its risk and potential impact.
4. Determine how it could be exploited.
5. Remediate the weakness.

---

## 🎯 Attack Surface & Security Hardening

### Attack Surface

An **attack surface** is the collection of all possible entry points and weaknesses that a threat actor could exploit to gain unauthorized access or affect an organization's assets.

Attack surfaces can be:

- **Digital** — applications, networks, accounts, cloud services, endpoints, APIs, and data
- **Physical** — offices, devices, server rooms, ports, removable media, and other physical access points

### Security Hardening

**Security hardening** is the process of reducing vulnerabilities and minimizing an asset's attack surface by strengthening configurations, access controls, software, and security controls.

### Protect All Entry Points

Security teams should think beyond obvious network boundaries and protect every possible entry point, including:
- Physical access
- Network access
- Applications
- User accounts
- Removable media
- Wireless networks
- Cloud services
- Third-party systems

---

## 👤 Threat Actors

A **threat actor** is a person or group that presents a security risk to an organization's assets. Threat actors may be intentional or accidental.

### Common Threat Actor Categories

- **Competitors** — rival organizations that may benefit from leaked information
- **State actors** — government intelligence agencies or state-sponsored groups
- **Criminal syndicates** — organized groups motivated by financial or criminal gain
- **Insider threats** — current or former authorized users who intentionally or accidentally put assets at risk
- **Shadow IT** — use of technologies outside official IT governance

### Types of Hackers

#### Unauthorized / Malicious Hackers

Use computer skills to gain unauthorized access or commit crimes.

**Script kiddies** are less-skilled attackers who rely heavily on pre-written tools or code.

#### Authorized / Ethical Hackers

Use hacking skills with permission to identify and improve security weaknesses.

Examples:
- Internal security testers
- External penetration testers
- Bug bounty researchers

#### Semi-Authorized Hackers

May violate ethical or legal boundaries without necessarily being primarily motivated by malicious intent.

**Example:** Hacktivists may exploit systems to promote a political or social cause.

---

## 🕵️ Advanced Persistent Threats (APTs)

An **Advanced Persistent Threat (APT)** occurs when a threat actor maintains unauthorized access to a system for an extended period.

APTs are commonly associated with:
- Nation states
- State-sponsored actors
- Long-term surveillance
- Intelligence gathering

Targets may include:
- Government
- Defense
- Financial organizations
- Telecommunications
- Private companies that provide a path toward larger targets

---

## 🚪 Attack Vectors

An **attack vector** is a pathway, technique, or entry point that a threat actor can use to gain unauthorized access to a system, network, application, or data.

Common attack vectors include:
- Direct physical access
- Removable media such as USB drives
- Email
- Social media
- Wireless networks
- Cloud services
- Supply-chain and third-party vendors

### Practicing an Attacker Mindset

1. **Identify a target**
2. **Determine how the target can be accessed**
3. **Evaluate which attack vectors can be exploited**
4. **Identify the tools and methods that could be used**

### Defending Attack Vectors

- Educate employees and users
- Apply the Principle of Least Privilege
- Use appropriate security tools and controls
- Build a diverse security team with different perspectives and skills

---

## 🥊 Brute Force Attacks

A **brute force attack** is a trial-and-error process used to discover private information, most commonly credentials or cryptographic keys.

### Types of Brute Force Attacks

#### Simple Brute Force

Attempts different username and password combinations until a valid combination is found.

#### Dictionary Attack

Uses a list of commonly used passwords or credentials.

#### Reverse Brute Force

Starts with one known or commonly used password and tries it against many usernames or systems.

#### Credential Stuffing

Uses stolen credentials from previous breaches to attempt access to accounts on another service.

### Pass the Hash

A specialized credential-reuse technique that uses stolen password hashes to authenticate without needing to know the original plaintext password.

### Exhaustive Key Search

Attempts possible cryptographic keys until the correct key is found.

---

## 🛠️ Brute Force Tools

Common tools used by security professionals for authorized testing include:

- Aircrack-ng
- Hashcat
- John the Ripper
- Ophcrack
- THC Hydra

These tools have different purposes and should only be used against systems where testing is authorized.

---

## 🛡️ Brute Force Prevention

Organizations use multiple controls to make brute-force attacks more difficult.

### Hashing & Salting

Strong password hashing and unique salts make stolen password databases significantly harder to crack using precomputed or brute-force techniques.

### Multi-Factor Authentication (MFA)

Requires additional authentication factors, reducing the usefulness of a stolen password alone.

### CAPTCHA

A challenge-response mechanism designed to distinguish human users from automated programs.

### Password Policies

Organizations can enforce:
- Strong passwords/passphrases
- Protection against common passwords
- Appropriate account lockout or throttling controls
- Secure password management practices

---

## 🧪 Hands-on Activities Completed

### Activity 1 — Vulnerability Assessment

- Performed a vulnerability assessment
- Identified system vulnerabilities
- Analyzed findings
- Assessed risk
- Recommended remediation
- Created a vulnerability assessment report

### Activity 2 — Identify Attack Vectors of a USB Drive

Analyzed how a USB drive can act as an attack vector and how removable media can expose systems to security risks.

---

## 📌 Module Takeaways

- Vulnerability assessments identify and prioritize weaknesses before attackers exploit them.
- Vulnerability scanners automate the discovery of known vulnerabilities and misconfigurations.
- Penetration testing validates vulnerabilities by safely simulating real attacks.
- Keeping software patched reduces exposure to known vulnerabilities.
- Security professionals should think like attackers while operating within authorized and controlled environments.
- Every possible entry point contributes to an organization's attack surface.
- Threat actors have different motivations, capabilities, and preferred attack vectors.
- Brute-force attacks can be reduced through layered controls such as MFA, strong password practices, hashing and salting, CAPTCHA, and login protections.

---

## ➡️ Next Module

[**Module 4 — Threats to Asset Security →**](./module04.md)

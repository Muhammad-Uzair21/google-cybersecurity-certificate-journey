# 📘 Module 4 — Threats to Asset Security

This module focuses on understanding common threats to organizational assets, the techniques used by threat actors, and how security professionals can proactively identify and mitigate those threats.

---

## 🧠 Social Engineering

### Social Engineering

A manipulation technique that exploits human error and human behavior to gain private information, access, or valuables.

### Stages of a Social Engineering Attack

1. **Prepare** — Research the target and gather useful information.
2. **Establish Trust (Pretexting)** — Create a believable identity, story, or situation.
3. **Use Persuasion Tactics** — Manipulate the target into providing information, access, or taking an action.
4. **Disconnect** — End the interaction while avoiding detection.

### Preventing Social Engineering Attacks

- Implement managerial and security controls
- Stay informed about emerging social engineering trends
- Educate employees, users, and others
- Share security knowledge and best practices

---

## 🎭 Social Engineering Tactics

Social engineering attacks exploit human behavior rather than relying solely on technical vulnerabilities.

### Common Tactics

| Tactic | Description |
|---|---|
| **Baiting** | Tempts a target into compromising their security, such as plugging in an unknown USB drive |
| **Phishing** | Uses digital communication to trick users into revealing information or installing malware |
| **Quid Pro Quo** | Offers a benefit or reward in exchange for information, access, or money |
| **Tailgating** | An unauthorized person follows an authorized person into a restricted area |
| **Watering Hole** | Compromises a website frequently visited by a specific group of users |

### Reducing Social Engineering Risks

- Stay alert to suspicious communications
- Verify unexpected emails and sender information
- Be cautious when sharing information
- Control curiosity around suspicious links and attachments
- Use security controls such as:
  - Firewalls
  - Multi-Factor Authentication (MFA)
  - Block lists
  - Email filtering
- Provide security awareness training

---

## 🎣 Phishing Attacks

### Phishing

A social engineering attack that uses digital communication to trick users into revealing sensitive information or deploying malicious software.

### Phishing Toolkit

Common tools and techniques used in phishing include:

- Malicious attachments
- Fake data collection forms
- Fraudulent web links

### Types of Phishing

#### Smishing

Phishing attacks conducted through SMS or text messages.

#### Vishing

Phishing attacks conducted through voice communication or phone calls.

#### Spear Phishing

A targeted phishing attack directed at a specific person or group while appearing to originate from a trusted source.

### Phishing Security Measures

- Anti-phishing policies
- Employee security awareness training
- Email filtering
- Intrusion Detection Systems (IDS)

### 🧪 Activity — Investigate a Spear-Phishing Email

Investigated a suspicious spear-phishing email received by an executive at an investment firm.

The email appeared to originate from the organization's board and requested installation of new collaboration software.

The activity involved analyzing the message to determine whether it was legitimate and whether it should be quarantined.

---

## 🦠 Malware

### Malware

Malicious software designed to harm devices or networks, steal information, gain unauthorized access, or disrupt operations.

### Common Ways Malware Spreads

- Phishing emails
- Malicious links
- Malicious attachments
- Fake or malicious software downloads
- Infected files
- Removable media
- Compromised websites
- Bundled software

### Types of Malware

#### Virus

Malicious code that interferes with computer operations and causes damage to data or software.

A virus requires user interaction or installation before it can spread and cause damage.

#### Worm

Malware that can duplicate and spread itself across systems.

Worms can target shared devices, drives, and files across a network.

#### Trojan

Malware disguised as a legitimate file or program.

It relies on users believing that the software or file is harmless.

#### Adware

Software that displays advertisements.

Malicious adware can appear as a **Potentially Unwanted Application (PUA)** and may slow devices or install additional software.

#### Spyware

Malware used to gather information without consent.

It can be hidden inside bundled software.

#### Scareware

Malware or unwanted software that frightens users with fake warnings in order to trick them into taking an unsafe action.

#### Fileless Malware

Malware that uses legitimate programs already installed on a system and resides primarily in memory rather than traditional files on disk.

#### Rootkit

Malware that provides remote administrative access and can create a backdoor into a system.

#### Dropper

Malware that contains and delivers malicious code onto a target system.

#### Loader

Malware that downloads and installs additional malicious code from an external source.

#### Botnet

A collection of malware-infected computers controlled by a threat actor known as a **bot-herder**.

#### Ransomware

Malware that encrypts an organization's data and demands payment to restore access.

---

## ⛏️ Cryptojacking

### Cryptojacking

The unauthorized use of a device's computing resources to mine cryptocurrency.

### Signs of Cryptojacking

- Device slowdown
- Frequent crashes
- Fast battery drain
- Increased electricity costs
- Unusually high CPU usage

### Preventing Cryptojacking

- Intrusion Detection Systems (IDS)
- Browser security extensions
- Ad blockers
- Disabling JavaScript where appropriate
- Staying updated on emerging cryptojacking trends

---

## 🌐 Web-Based Exploits

Web-based exploits target vulnerabilities in websites and web applications.

### Common Web-Based Exploits

- Injection attacks
- Cross-Site Scripting (XSS)
- SQL Injection

---

## ⚠️ Cross-Site Scripting (XSS)

Cross-Site Scripting is a web-based attack where malicious scripts are injected into content that is delivered to users.

### Types of XSS

#### Reflected XSS

Malicious input is reflected immediately back to the user through a web application.

#### Stored XSS

Malicious script is permanently stored by the vulnerable application and later delivered to users.

#### DOM-Based XSS

The vulnerability occurs through manipulation of the Document Object Model (DOM) in the user's browser.

---

## 💉 SQL Injection

### SQL Injection

An attack that exploits vulnerable application input fields to execute unexpected SQL queries against a database.

SQL injection can be used to:

- Modify information
- Delete information
- Steal sensitive data
- Gain unauthorized access
- Potentially take control of vulnerable applications

### Common Injection Points

SQL injection can occur anywhere an application accepts user input, such as:

- Login forms
- Search bars
- Comment boxes
- Other input fields

### SQL Injection Categories

#### In-Band SQL Injection

The attacker uses the same communication channel to launch the attack and receive its results.

#### Out-of-Band SQL Injection

The attacker uses a different communication channel to launch the attack and receive the results.

#### Inferential SQL Injection

The attacker cannot directly see the results and instead analyzes the application's behavior to infer information.

### SQL Injection Prevention

#### Prepared Statements

A coding technique that executes SQL statements before passing them to the database.

#### Input Sanitization

Removes user input that could be interpreted as code.

#### Input Validation

Ensures user input matches the expected format or requirements.

Using these techniques together helps reduce SQL injection risks.

---

## 🧠 Threat Modeling

### Threat Modeling

The process of identifying assets, vulnerabilities, and how those assets are exposed to threats.

It provides a proactive way to identify and reduce security risks.

Threat modeling can be:

- **Generic** — Applied to broader systems or environments
- **Specific** — Focused on a particular application, network, or system

Threat modeling is an advanced security skill and is especially important in application security and secure software development.

### Threat Modeling Process

#### 1. Define the Scope

Determine what system, application, network, or business process is being analyzed.

#### 2. Identify Threats

Identify possible threat actors, attack vectors, and ways the system could be attacked.

Tools such as attack trees can help visualize possible attack paths.

#### 3. Characterize the Environment

Understand the system's architecture, data flows, users, technologies, and surrounding environment.

#### 4. Analyze Threats

Evaluate identified threats and determine how likely and impactful they could be.

#### 5. Mitigate Risks

Determine security controls and actions that can reduce or eliminate identified risks.

#### 6. Evaluate

Review the results and determine whether the security measures adequately address the identified threats.

---

## 🔎 Threat Modeling Frameworks

Common threat modeling frameworks include:

- **STRIDE**
- **PASTA**
- **Trike**
- **VAST**

### STRIDE

A threat-modeling framework developed by Microsoft.

It focuses on six categories:

- Spoofing
- Tampering
- Repudiation
- Information Disclosure
- Denial of Service
- Elevation of Privilege

### PASTA

**Process for Attack Simulation and Threat Analysis**

A risk-centric threat modeling framework that focuses on identifying viable threats and understanding their potential impact.

### Trike

An open-source, security-centric threat modeling methodology that focuses on areas such as permissions, use cases, and privilege models.

### VAST

**Visual, Agile, and Simple Threat Modeling**

A framework designed to make threat modeling more scalable, automated, and streamlined.

---

## 🧪 PASTA Threat Modeling

### PASTA Framework

PASTA is a seven-stage threat modeling process used to analyze the risk profile of an application or environment.

### PASTA Steps

1. **Define Security Objectives**
2. **Define Technical Scope**
3. **Decompose the Application**
4. **Perform a Threat Analysis**
5. **Perform a Vulnerability Analysis**
6. **Conduct Attack Modeling**
7. **Analyze Risks and Impact**

### Example — Fitness App

Imagine a company is preparing to launch a new fitness application.

The security team wants to determine whether the application can safely protect customer information.

**1. Define Security Objectives**

Determine what needs to be protected, such as customer accounts and personal fitness information.

**2. Define Technical Scope**

Identify the application's technologies, infrastructure, databases, APIs, and other technical components.

**3. Decompose the Application**

Break the application into its components and understand how data moves between them.

**4. Perform a Threat Analysis**

Identify possible threat actors and the ways they could target the application.

**5. Perform a Vulnerability Analysis**

Look for weaknesses that could allow those threats to succeed.

**6. Conduct Attack Modeling**

Model possible attack paths using techniques such as testing or attack trees.

**7. Analyze Risks and Impact**

Determine the likelihood and impact of successful attacks and decide whether the application's risks are acceptable.

---

## 🧪 Hands-on Activities

### Activity 1 — Filter Malicious Emails

Investigated a suspicious spear-phishing email to determine whether it was legitimate and whether it should be quarantined.

### Activity 2 — Apply the PASTA Threat Model Framework

Practiced applying the PASTA framework to determine whether a new shopping application was safe to launch.

The activity involved identifying potential vulnerabilities and evaluating the application's overall risk profile before deployment.

---

# 🎯 Module 4 Complete

Module 4 focused on understanding common threats to organizational assets and developing an attacker mindset to proactively identify and mitigate security risks.

Key areas covered:

- Social engineering
- Phishing
- Malware
- Cryptojacking
- Web-based exploits
- XSS
- SQL injection
- Threat modeling
- PASTA
- Attack simulation
- Risk analysis

---

⬅️ [Back to Course README](./README.md)
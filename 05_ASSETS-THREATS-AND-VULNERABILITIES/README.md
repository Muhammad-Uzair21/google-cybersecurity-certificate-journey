# 🛡️ Course 5 — Assets, Threats, and Vulnerabilities

![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Platform](https://img.shields.io/badge/Platform-Coursera-0056D2)
![Issuer](https://img.shields.io/badge/Issuer-Google-4285F4)

> Learning how organizations identify, classify, and protect their assets while understanding threats, vulnerabilities, risk management, security controls, privacy, and cryptographic protections.

---

# 📑 Module Index

- Module 1 — Introduction to Asset Security ✅
- Module 2 — Protect Organizational Assets *(In Progress)*
- Module 3 — Vulnerabilities in systems *(Coming Soon)*
- Module 4 — Threats to asset security *(Coming Soon)*

---

# 📘 Module 1 — Introduction to Asset Security

## What This Module Covers

Understanding organizational assets, risk management fundamentals, asset classification, security planning, cybersecurity frameworks, and performing practical risk assessments.

<details>
<summary><strong>📖 Module 1 </strong></summary>

---

### 🎯 Core Security Concepts

#### Risk

- Anything that impacts the **Confidentiality, Integrity, or Availability (CIA)** of an asset
- Risk is commonly calculated as:

```
Likelihood × Impact = Risk
```

Risk management helps organizations:

- Prevent costly incidents
- Prioritize critical assets
- Improve systems and processes
- Determine acceptable levels of risk

---

#### Threat

Any circumstance or event capable of negatively impacting an asset.

**Types**

- Intentional
- Unintentional

---

#### Vulnerability

A weakness that can be exploited by a threat.

**Categories**

- Technical vulnerabilities
- Human vulnerabilities

---

### 📦 Asset Management

Process of tracking organizational assets and the risks affecting them.

Includes:

- Asset Inventory
- Asset Classification

---

### 🏷️ Asset Classification

Common classification levels:

| Classification | Description |
|---------------|-------------|
| Restricted | Highest sensitivity |
| Confidential | Significant impact if disclosed |
| Internal Only | Accessible internally |
| Public | Safe for public release |

Classification considers:

- What the asset is
- Where it is
- Who owns it
- Its business importance

---

### ⚠️ Risk Classifications

Common impacts of security incidents:

- Damage
- Disclosure
- Loss of Information

---

### 📋 Elements of a Security Plan

Every security plan is built around:

- Policies
- Standards
- Procedures

---

### 🛡️ NIST Cybersecurity Framework (CSF)

A voluntary framework consisting of standards, guidelines, and best practices for managing cybersecurity risks.

Components:

- **Core** — Security functions and activities
- **Tier** — Security maturity level
- **Profile** — Aligns security controls with business requirements

---

### 🧪 Portfolio Activity Completed

#### Risk Assessment

**Scenario**

Worked as a cybersecurity analyst for a banking organization.

Created a **Risk Register** by:

- Identifying risks
- Determining likelihood
- Assessing severity
- Calculating overall priority

This activity introduced practical risk analysis and prioritization used in real security operations.

</details>

---

# 📘 Module 2 — Protect Organizational Assets

<details>
<summary><strong> Module 2 — Protect Organizational Assets </strong></summary>

This module focuses on protecting organizational assets through security controls, information privacy, identity and access management (IAM), authentication and authorization mechanisms, encryption, hashing, and regulatory compliance. It emphasizes how organizations safeguard sensitive information using layered security practices.

</details>

---

<details>
<summary><strong>🛡️ Security Controls</strong></summary>

### Security Controls

Safeguards implemented to reduce security risks and protect organizational assets.

### Types of Security Controls

#### Technical Controls

Implemented using technology.

Examples:

- Firewalls
- Antivirus
- Encryption
- Multi-Factor Authentication (MFA)

#### Operational Controls

Processes and procedures carried out by people.

Examples:

- Security awareness training
- Incident response
- Backup procedures
- Access reviews

#### Managerial Controls

Administrative policies and governance.

Examples:

- Security policies
- Risk assessments
- Compliance programs
- Security planning

</details>

---

<details>
<summary><strong>🔒 Information Privacy & Least Privilege</strong></summary>

### Information Privacy

Protecting personal and sensitive information from unauthorized access, disclosure, or misuse.

### Information Security vs Privacy

| Information Security | Information Privacy |
|----------------------|---------------------|
| Protects data from threats | Gives users control over their personal information |

---

### Principle of Least Privilege (PoLP)

Users should receive only the minimum permissions required to perform their job.

Benefits:

- Limits unauthorized access
- Reduces attack surface
- Minimizes accidental changes
- Supports CIA Triad

---

### Separation of Duties (SoD)

Critical responsibilities are divided among multiple users.

Purpose:

- Prevent fraud
- Reduce insider threats
- Increase accountability

---

### Data Governance Roles

#### Data Owner

Determines:

- Who can access data
- Who can edit data
- Who can use data
- When data is destroyed

#### Data Custodian

Responsible for:

- Storage
- Security
- Transport
- Protection of data

#### Data Steward

Maintains and enforces organizational data governance policies.

</details>

---

<details>
<summary><strong>📊 Data Lifecycle & Governance</strong></summary>

### Data Lifecycle

Five stages:

1. Collect
2. Store
3. Use
4. Archive
5. Destroy

---

### Data Governance

Framework that defines how an organization manages information throughout its lifecycle.

Goals:

- Privacy
- Integrity
- Availability
- Compliance
- Security

---

### Protected Information

#### PII

Personally Identifiable Information

Examples:

- Name
- Address
- Phone number

---

#### SPII

Sensitive Personally Identifiable Information

Examples:

- Login credentials
- National ID
- Bank account information

---

#### PHI

Protected Health Information

Protected under HIPAA (US) and GDPR (EU).

</details>

---

<details>
<summary><strong>📜 Security Regulations & Compliance</strong></summary>

### Major Regulations

#### GDPR

General Data Protection Regulation

- European Union
- Protects personal information
- Gives users control over their data

---

#### PCI DSS

Payment Card Industry Data Security Standard

Protects payment card information.

---

#### HIPAA

Health Insurance Portability and Accountability Act

Protects medical and healthcare information.

---

### Security Audit

Reviews:

- Policies
- Procedures
- Security controls
- Compliance

Usually performed annually.

---

### Security Assessment

Evaluates:

- Security posture
- Existing vulnerabilities
- Effectiveness of controls

Performed more frequently than audits.

</details>

---

<details>
<summary><strong>🔐 Encryption & Cryptography</strong></summary>

### Cryptography

The practice of securing information through mathematical techniques.

---

### Encryption

Converts plaintext into ciphertext.

---

### Decryption

Converts ciphertext back into plaintext.

---

### Cipher

Algorithm used to encrypt or decrypt information.

---

### Cryptographic Key

Secret value used during encryption and decryption.

---

### Brute Force Attack

Attempts every possible key until the correct one is found.

Longer keys provide stronger protection.

---

### Symmetric Encryption

Uses one shared secret key.

Common Algorithms:

- AES (128/192/256-bit)
- Triple DES (3DES)

Advantages:

- Fast
- Efficient

---

### Asymmetric Encryption

Uses two keys:

- Public Key
- Private Key

Common Algorithms:

- RSA
- DSA

Advantages:

- Secure key exchange
- Digital signatures

---

### Public Key Infrastructure (PKI)

Framework used to establish trust through digital certificates.

Process:

1. Exchange encrypted information
2. Verify identity using Digital Certificates

---

### Digital Certificate

Verifies identity and ownership of a public key.

</details>

---

<details>
<summary><strong>📝 Hashing & Non-Repudiation</strong></summary>

### Hash Function

One-way mathematical algorithm that converts data into a fixed-length hash.

Properties:

- Deterministic
- One-way
- Fast
- Unique output

---

### Advantages of Hashing

- Verify integrity
- Password protection
- Detect file modifications
- Digital signatures

---

### Common Hash Algorithms

- MD5 *(legacy & vulnerable)*
- SHA-1 *(deprecated)*
- SHA-224
- SHA-256
- SHA-384
- SHA-512

---

### Hash Collision

Two different inputs produce the same hash value.

---

### Rainbow Table

Collection of precomputed password hashes used to crack weak passwords.

---

### Salting

Random value added before hashing.

Benefits:

- Prevents rainbow table attacks
- Produces unique hashes

---

### Non-Repudiation

Ensures that a sender cannot deny sending a message or performing an action.

Achieved using:

- Hash functions
- Digital signatures
- Public Key Infrastructure (PKI)

</details>

---

<details>
<summary><strong>🔑 Authentication, Authorization & Accounting (AAA)</strong></summary>

### AAA Framework

- Authentication
- Authorization
- Accounting

---

### Authentication

Verifies user identity.

Authentication Factors:

- Knowledge (Password, PIN)
- Ownership (OTP, Smart Card)
- Characteristic (Fingerprint, Face ID)

---

### Single Sign-On (SSO)

One login grants access to multiple services.

Benefits:

- Better user experience
- Fewer passwords
- Reduced password fatigue

Protocols:

- LDAP
- SAML

---

### Multi-Factor Authentication (MFA)

Requires two or more authentication factors.

Examples:

- Password + OTP
- Password + Fingerprint

---

### Authorization

Determines what authenticated users are allowed to access.

Access Control Models:

#### MAC

Mandatory Access Control

- Strictest model
- Administrator-controlled

#### DAC

Discretionary Access Control

- Resource owner grants permissions

#### RBAC

Role-Based Access Control

- Permissions assigned by job role

---

### OAuth

Authorization protocol that allows third-party applications to access user resources without exposing passwords.

---

### HTTP Authentication

Authentication mechanism built into the HTTP protocol for verifying users.

---

### Accounting

Tracks user activities after successful authentication.

Purpose:

- Monitoring
- Auditing
- Incident investigations

---

### Sessions

Temporary authenticated connection between a user and a service.

---

### Session ID

Unique identifier assigned after authentication.

---

### Session Cookies

Store Session IDs inside the browser.

---

### Session Hijacking

Attack where an attacker steals a valid session ID to impersonate a user.

</details>

---

<details>
<summary><strong>🆔 Identity & Access Management (IAM)</strong></summary>

### Identity & Access Management (IAM)

Framework of processes and technologies used to manage digital identities and access to resources.

Goals:

- Right User
- Right Resource
- Right Time
- Right Reason

---

### IAM vs AAA

| AAA | IAM |
|------|-----|
| Authentication, Authorization, Accounting | Complete identity management framework |

---

### User Provisioning

Creating and maintaining user identities.

Includes:

- Creating accounts
- Assigning permissions

---

### Deprovisioning

Removing user access when it is no longer required.

---

### IAM Technologies

- User directories
- Authentication systems
- Authorization systems
- Auditing systems

Organizations may use:

- In-house IAM solutions
- Third-party IAM platforms

</details>

---

<details>
<summary><strong>🧪 Hands-on Activities Completed</strong></summary>

### Activity 1 — Assess Organizational Access Controls

- Evaluated an organization's access control process
- Identified weaknesses in authentication and authorization
- Applied Least Privilege and Separation of Duties
- Recommended IAM security improvements

---

### Activity 2 — Caesar Cipher Decryption

- Used Linux commands to decrypt encrypted files
- Broke a Caesar Cipher
- Recovered hidden messages from encrypted files

---

### Activity 3 — Generate Hash Values

- Generated hashes for multiple files
- Compared file hashes
- Verified file integrity
- Determined whether files had been modified

</details>

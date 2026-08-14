# 🛡️ Course 5 — Module 2: Protect Organizational Assets

> Protecting organizational assets through security controls, privacy, identity and access management, authentication and authorization, cryptography, hashing, and compliance.

---

## 🛡️ Security Controls

Security controls are safeguards implemented to reduce security risks and protect organizational assets.

### Technical Controls

Controls implemented using technology.

Examples:
- Firewalls
- Antivirus
- Encryption
- Multi-Factor Authentication (MFA)

### Operational Controls

Processes and procedures carried out by people.

Examples:
- Security awareness training
- Incident response
- Backup procedures
- Access reviews

### Managerial Controls

Administrative policies and governance mechanisms.

Examples:
- Security policies
- Risk assessments
- Compliance programs
- Security planning

---

## 🔒 Information Privacy & Access Principles

### Information Privacy

Protecting personal and sensitive information from unauthorized access, disclosure, or misuse.

| Information Security | Information Privacy |
|---|---|
| Protects data from threats | Gives users control over their personal information |

### Principle of Least Privilege (PoLP)

Users should receive only the minimum permissions required to perform their job.

**Benefits:**
- Limits unauthorized access
- Reduces attack surface
- Minimizes accidental changes
- Supports the CIA Triad

### Separation of Duties (SoD)

Critical responsibilities are divided among multiple users.

**Purpose:**
- Prevent fraud
- Reduce insider threats
- Increase accountability

---

## 👥 Data Governance Roles

### Data Owner

Determines:
- Who can access data
- Who can edit data
- Who can use data
- When data is destroyed

### Data Custodian

Responsible for:
- Storage
- Security
- Transport
- Protection of data

### Data Steward

Maintains and enforces organizational data governance policies.

---

## 📊 Data Lifecycle & Governance

### Data Lifecycle

Five stages:

1. Collect
2. Store
3. Use
4. Archive
5. Destroy

### Data Governance

A framework that defines how an organization manages information throughout its lifecycle.

**Goals:**
- Privacy
- Integrity
- Availability
- Compliance
- Security

### Protected Information

#### PII — Personally Identifiable Information

Examples:
- Name
- Address
- Phone number

#### SPII — Sensitive Personally Identifiable Information

Examples:
- Login credentials
- National ID
- Bank account information

#### PHI — Protected Health Information

Health-related information protected by regulations such as HIPAA.

---

## 📜 Security Regulations & Compliance

### GDPR

**General Data Protection Regulation**

- European Union regulation
- Protects personal information
- Gives individuals greater control over their data

### PCI DSS

**Payment Card Industry Data Security Standard**

Protects payment card information.

### HIPAA

**Health Insurance Portability and Accountability Act**

Protects medical and healthcare information.

### Security Audit

Reviews:
- Policies
- Procedures
- Security controls
- Compliance

### Security Assessment

Evaluates:
- Security posture
- Existing vulnerabilities
- Effectiveness of controls

Security assessments are generally performed more frequently than formal audits.

---

## 🔐 Encryption & Cryptography

### Cryptography

The practice of securing information through mathematical techniques.

### Encryption

Converts **plaintext → ciphertext**.

### Decryption

Converts **ciphertext → plaintext**.

### Cipher

An algorithm used to encrypt or decrypt information.

### Cryptographic Key

A value used during encryption and decryption.

### Brute Force

Attempts possible keys until the correct key is found.

Longer keys generally provide stronger protection against exhaustive key-search attacks.

### Symmetric Encryption

Uses one shared secret key.

Examples:
- AES (128/192/256-bit)
- Triple DES (3DES)

**Advantages:**
- Fast
- Efficient

### Asymmetric Encryption

Uses two related keys:
- Public key
- Private key

Examples:
- RSA
- DSA

**Uses:**
- Secure key exchange
- Digital signatures

### Public Key Infrastructure (PKI)

A framework used to establish trust through digital certificates.

### Digital Certificate

Verifies the identity of a subject and binds that identity to a public key.

---

## 📝 Hashing & Non-Repudiation

### Hash Function

A one-way mathematical algorithm that converts data into a fixed-length hash.

**Properties:**
- Deterministic
- One-way
- Fast
- Designed to make finding collisions difficult

### Uses of Hashing

- Verify integrity
- Password protection
- Detect file modifications
- Support digital signatures

### Common Hash Algorithms

- MD5 — legacy and cryptographically broken
- SHA-1 — deprecated for security-sensitive uses
- SHA-224
- SHA-256
- SHA-384
- SHA-512

### Hash Collision

Occurs when two different inputs produce the same hash value.

### Rainbow Table

A collection of precomputed password hashes used to help crack weak password hashes.

### Salting

A random value added to password data before hashing.

**Benefits:**
- Makes precomputed rainbow tables less effective
- Produces different hashes for identical passwords

### Non-Repudiation

Provides evidence that helps prevent a sender from denying an action or message.

Common mechanisms include:
- Digital signatures
- Cryptographic hashing
- PKI

---

## 🔑 Authentication, Authorization & Accounting (AAA)

### AAA Framework

- **Authentication** — Who are you?
- **Authorization** — What are you allowed to do?
- **Accounting** — What did you do?

### Authentication

Verifies a user's identity.

**Authentication factors:**
- **Knowledge** — password, PIN
- **Ownership** — OTP, smart card
- **Characteristic** — fingerprint, Face ID

### Single Sign-On (SSO)

One authentication event grants access to multiple services.

**Benefits:**
- Better user experience
- Fewer passwords
- Reduced password fatigue

**Protocols/technologies encountered:**
- LDAP
- SAML

### Multi-Factor Authentication (MFA)

Requires two or more authentication factors.

Examples:
- Password + OTP
- Password + fingerprint

### Authorization

Determines what an authenticated user is allowed to access.

**Access control models:**

#### MAC — Mandatory Access Control
- Strictly controlled
- Administrator/system determines permissions

#### DAC — Discretionary Access Control
- Resource owner can grant permissions

#### RBAC — Role-Based Access Control
- Permissions are assigned according to job roles

### OAuth

An authorization framework that allows applications to access user resources without exposing the user's password to the application.

### HTTP Authentication

Authentication mechanisms provided through HTTP for verifying users.

### Accounting

Tracks user activity after successful authentication.

**Purpose:**
- Monitoring
- Auditing
- Incident investigation

### Sessions

A temporary authenticated connection between a user and a service.

### Session ID

A unique identifier associated with an authenticated session.

### Session Cookies

Browser cookies can store session identifiers.

### Session Hijacking

An attack in which an attacker obtains a valid session identifier and uses it to impersonate the user.

---

## 🆔 Identity & Access Management (IAM)

**IAM** is a framework of processes and technologies used to manage digital identities and access to resources.

### IAM Goals

- Right user
- Right resource
- Right time
- Right reason

### IAM vs AAA

| AAA | IAM |
|---|---|
| Authentication, Authorization, Accounting | Broader identity and access management framework |

### User Provisioning

Creating and maintaining user identities.

Includes:
- Creating accounts
- Assigning permissions

### Deprovisioning

Removing or disabling access when it is no longer required.

### IAM Technologies

- User directories
- Authentication systems
- Authorization systems
- Auditing systems

Organizations may use:
- In-house IAM solutions
- Third-party IAM platforms

---

## 🧪 Hands-on Activities Completed

### Activity 1 — Assess Organizational Access Controls

- Evaluated an organization's access control process
- Identified weaknesses in authentication and authorization
- Applied Least Privilege and Separation of Duties
- Recommended IAM security improvements

### Activity 2 — Caesar Cipher Decryption

- Used Linux commands to decrypt encrypted files
- Broke a Caesar cipher
- Recovered hidden messages from encrypted files

### Activity 3 — Generate Hash Values

- Generated hashes for multiple files
- Compared file hashes
- Verified file integrity
- Determined whether files had been modified

---

## 📌 Module Takeaways

- Security controls reduce risk through technical, operational, and managerial measures.
- Least privilege and separation of duties reduce unnecessary access and insider risk.
- Data must be protected throughout its lifecycle.
- Encryption protects confidentiality, while hashing is primarily used for integrity and password-related protection.
- AAA separates identity verification, permissions, and activity tracking.
- IAM manages identities and access across the organization.

---

## ➡️ Next Module

[**Module 3 — Vulnerabilities in Systems →**](./module03.md)

# 📘 Module 1 — Introduction to Detection and Incident Response

> Understanding how security teams detect, investigate, contain, and recover from security incidents.

---

## 📑 Module Sections

- The Incident Response Lifecycle
- Incident Response Operations
- Incident Response Plans
- Incident Response Tools
- SIEM Technology
- Portfolio Activity — Incident Handler's Journal

---

<details>
<summary><strong>🚨 The Incident Response Lifecycle</strong></summary>

### Event

An **event** is an observable occurrence within a system, network, or environment.

Examples include:
- A user logging in
- A file being modified
- A network connection being established
- A system generating an alert

### Incident

An **incident** is an event that results in, or could result in, harm to an organization's information or systems.

---

### 🔎 The 5 W's of an Incident

When investigating an incident, analysts can ask:

- **Who** — Who was involved?
- **What** — What happened?
- **When** — When did it happen?
- **Where** — Where did it happen?
- **Why** — Why did it happen?

These questions help security teams understand and investigate an incident.

---

### 🔄 Incident Response Lifecycle

Incident response is the process of identifying, investigating, containing, and recovering from security incidents.

The lifecycle **isn't strictly linear**. Steps can overlap because new information may be discovered during an investigation, requiring responders to revisit earlier steps.

The lifecycle supports the final three functions of the **NIST Cybersecurity Framework (CSF)**:

- **Detect**
- **Respond**
- **Recover**

---

### NIST Incident Response Lifecycle

The NIST incident response framework consists of four phases:

1. **Preparation**
2. **Detection & Analysis**
3. **Containment, Eradication & Recovery**
4. **Post-Incident Activity**

#### 1. Preparation

Establish the processes, resources, tools, and procedures needed to respond to incidents.

#### 2. Detection & Analysis

Identify potential incidents, analyze alerts and evidence, and determine whether an actual security incident has occurred.

#### 3. Containment, Eradication & Recovery

- **Containment** — Limit the impact and prevent further damage.
- **Eradication** — Remove the root cause and malicious elements.
- **Recovery** — Restore affected systems and return operations to normal.

#### 4. Post-Incident Activity

Review the incident, document findings, identify lessons learned, and improve future incident response.

</details>

---

<details>
<summary><strong>👥 Incident Response Operations</strong></summary>

### CSIRT

A **Computer Security Incident Response Team (CSIRT)** is a specialized group of security professionals trained to manage and respond to security incidents.

CSIRTs help provide:

- **Command** — Leadership and direction during the response.
- **Control** — Management of technical activities, resources, and tasks.
- **Communication** — Keeping relevant stakeholders informed.

A CSIRT isn't always a permanent dedicated team. Organizations may use different structures or names, such as:

- **CSIRT**
- **SIRT (Security Incident Response Team)**
- **IHT (Incident Handling Team)**

---

### CSIRT Roles

#### Security Analyst

Continuously monitors the environment for security threats.

Responsibilities include:

- Analyzing and triaging alerts
- Investigating root causes
- Escalating or resolving alerts

#### Technical Lead

Manages the technical aspects of incident response.

Responsibilities include:

- Determining the root cause
- Developing containment strategies
- Managing eradication and recovery
- Applying patches or updates
- Coordinating technical response activities

#### Incident Coordinator

Coordinates communication between the security team and other departments.

Responsibilities include:

- Keeping communication clear
- Coordinating relevant departments
- Maintaining awareness of incident status
- Connecting security and non-security stakeholders

---

### 🏢 Security Operations Center (SOC)

A **Security Operations Center (SOC)** is an organizational unit dedicated to monitoring networks, systems, and devices for security threats and attacks.

A SOC performs activities such as:

- Network monitoring
- Alert analysis
- Threat detection
- Incident response

SOC structures commonly include analysts across three tiers.

#### Tier 1 — SOC Analyst

- Monitors and reviews alerts
- Prioritizes alerts based on severity
- Creates and closes tickets
- Escalates alerts to Tier 2 or Tier 3

#### Tier 2 — SOC Analyst

- Investigates escalated alerts
- Performs deeper analysis
- Configures and refines security tools
- Reports to the SOC Lead

#### Tier 3 — SOC Lead

- Manages SOC operations
- Performs advanced detection
- Conducts malware and forensic analysis
- Reports to the SOC Manager

#### SOC Manager

- Manages and evaluates the SOC team
- Develops performance metrics
- Creates incident, compliance, and audit reports
- Communicates findings to stakeholders

---

### Other Security Roles

**Forensic Investigators**

Collect, preserve, and analyze digital evidence to determine what happened during an incident.

**Threat Hunters**

Proactively search for new and advanced threats using threat intelligence and other detection techniques.

> Organizational structures, job titles, and responsibilities can vary between companies.

</details>

---

<details>
<summary><strong>📋 Incident Response Plans</strong></summary>

### Incident Response Plan

An **incident response plan** provides an organization with documented procedures for responding to security incidents.

Plans are **organization-specific** and can change depending on:

- Business requirements
- Systems and infrastructure
- Types of threats
- Organizational structure
- Available resources

---

### Elements of an Incident Response Plan

Common elements include:

- **Procedures** — Steps to follow during an incident
- **System information** — Details about systems, infrastructure, and resources
- **Other supporting documents** — Additional information needed during incident response

---

### 🧪 Incident Response Exercises

Organizations can test their incident response plans through exercises.

Examples include:

- **Tabletop exercises**
- Other simulated incident response exercises

These exercises help teams practice their responsibilities and identify weaknesses in their response plans.

</details>

---

<details>
<summary><strong>🛠️ Incident Response Tools</strong></summary>

Security teams rely on different tools to detect, investigate, and respond to threats.

### Intrusion Detection System (IDS)

An **Intrusion Detection System (IDS)** monitors system or network activity and generates alerts when potential malicious activity is detected.

An IDS:

- Detects malicious activity
- Logs activity
- Generates alerts
- Does **not** automatically prevent the intrusion

Common IDS tools include:

- **Zeek**
- **Suricata**
- **Snort**
- **Sagan**
- **Kismet**

---

### Intrusion Prevention System (IPS)

An **Intrusion Prevention System (IPS)** monitors activity for malicious behavior and takes action to prevent or stop the activity.

Unlike an IDS, an IPS can automatically respond to detected threats.

Some tools, including **Suricata, Snort, and Sagan**, can operate as both IDS and IPS.

---

### Endpoint Detection and Response (EDR)

An **Endpoint Detection and Response (EDR)** solution monitors endpoints for malicious or suspicious activity.

Endpoints can include:

- Computers
- Phones
- Tablets
- Other network-connected devices

EDR tools:

- Monitor endpoint activity
- Record activity
- Analyze behavior
- Generate alerts
- Respond to suspicious activity
- Can use automation to stop threats

Unlike IDS and IPS, EDR performs **behavioral analysis** of endpoint activity.

---

### Detection Results

Security alerts can be categorized into four outcomes:

| Result | Meaning |
|---|---|
| **True Positive** | A threat exists and the system correctly detects it |
| **True Negative** | No threat exists and no alert is generated |
| **False Positive** | An alert is generated even though no threat exists |
| **False Negative** | A real threat exists but the system fails to detect it |

**False positives** consume investigation time and resources.

**False negatives** are especially dangerous because legitimate attacks can go undetected.

</details>

---

<details>
<summary><strong>📊 SIEM & SOAR</strong></summary>

### SIEM

A **Security Information and Event Management (SIEM)** tool collects and analyzes log data to monitor critical activities within an organization.

SIEM tools help security analysts perform **log analysis**, which involves examining logs to identify events of interest.

### SIEM Advantages

- **Access to event data** — Centralizes activity from systems and devices.
- **Monitoring, detection & alerting** — Continuously analyzes activity and generates alerts when detection rules are matched.
- **Log storage** — Retains historical event data for investigations and other organizational requirements.

---

### 🔄 SIEM Process

The SIEM process consists of three main stages:

#### 1. Collect & Aggregate

SIEM tools collect logs from sources such as:

- Firewalls
- Servers
- Routers
- Other systems and devices

The collected data is aggregated into a centralized location.

##### Parsing

**Parsing** extracts fields and their corresponding values from raw log data.

**Example raw log:**

```text
April 3 11:01:21 server sshd[1088]: Failed password for user nuhara from 218.124.14.105 port 5023

Parsed fields:

Plaintext
host = server
process = sshd
source_user = nuhara
source_ip = 218.124.14.105
source_port = 5023

```

#### 2. Normalize Data
Normalization converts data from different sources into a standard, structured format.
This makes the data easier for SIEM systems to process and search.

#### 3. Analyze Data
The SIEM analyzes normalized data using detection logic, such as rules and conditions.
When activity matches a detection rule, an alert can be generated for security teams.

---

# Correlation
Correlation compares multiple log events to identify patterns that may indicate security threats.

# Common SIEM Tools

- AlienVault OSSIM

- Chronicle

- Elastic

- Exabeam

- IBM QRadar

- LogRhythm

- Splunk

# SOAR
Security Orchestration, Automation, and Response (SOAR) tools help security teams coordinate and automate security operations and response activities.

---

# 📓 Document an Incident with an Incident Handler's Journal
The module includes a portfolio activity involving an incident handler's journal:

- The activity starts with a security incident scenario and initial journal entries.

- As the course progresses, additional information and investigation details can be added to the journal.

- The goal is to practice documenting incidents throughout the detection and response process.

- This activity develops into a complete, portfolio-worthy incident documentation exercise as additional course material is completed.

</details>
---

## 🎯 Key Takeaways
Incident response follows a lifecycle, but the process is not strictly linear.

- The NIST lifecycle consists of Preparation, Detection & Analysis, Containment/Eradication/Recovery, and Post-Incident Activity.

- CSIRTs provide structured command, control, and communication during incidents.

- SOC teams monitor, investigate, and respond to security alerts across different analyst tiers.

- Incident response plans provide organization-specific procedures and supporting information.

- IDS detects, IPS prevents, and EDR monitors and responds at endpoints.

- Detection results can be true positive, true negative, false positive, or false negative.

- SIEM tools centralize, normalize, and analyze security logs.

- SOAR tools help automate and coordinate security response activities.

- Effective incident response depends on both technical tools and coordinated people/processes.

---
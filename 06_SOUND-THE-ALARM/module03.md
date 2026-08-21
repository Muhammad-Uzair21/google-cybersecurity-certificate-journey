# Module 3 — Incident Investigation and Response

## Overview

This module focused on the **Detection and Analysis** and **Response and Recovery** phases of the incident response lifecycle.

The module covered how security analysts detect and validate incidents, investigate indicators of compromise, document evidence, use playbooks, perform incident triage, contain and eradicate threats, recover affected systems, and maintain business continuity.

---

## 1. Incident Detection and Verification

### Detection and Analysis Phase

The **Detection and Analysis Phase** is where security teams are notified of possible incidents and investigate them to determine whether an actual security incident has occurred.

- **Detection:** Prompt discovery of security events.
- **Analysis:** Investigation and validation of alerts.

### Detection Challenges

Security teams cannot detect everything. Some challenges include:

- Detection tools can only detect activity that they have been configured to monitor.
- Large organizations can generate a very high volume of alerts.
- Broad detection configurations can generate **false positives**.
- Attackers continuously evolve their tactics and techniques.
- Poorly configured detection tools can miss suspicious activity.

Because of these limitations, organizations should use multiple detection methods.

---

## 2. Cybersecurity Incident Detection Methods

### Threat Hunting

**Threat hunting** is the proactive search for threats on a network.

Threat hunting combines human analysis with technology to discover threats that automated detection tools may have missed.

Threat hunters can use:

- Threat intelligence
- Indicators of compromise (IoCs)
- Indicators of attack (IoAs)
- Machine learning
- Research into emerging threats

Threat hunting can help identify threats before they cause significant damage.

### Fileless Malware

**Fileless malware** is malware that uses techniques such as hiding in memory instead of relying on traditional files or applications.

Because it can evade traditional signature-based detection, human-driven threat hunting can help identify it.

### Threat Intelligence

**Threat intelligence** is evidence-based threat information that provides context about existing or emerging threats.

Sources can include:

- Industry reports
- Government advisories
- Threat data feeds

Threat intelligence can contain information about attacker:

- Tactics
- Techniques
- Procedures (TTPs)
- IP addresses
- Domains
- File hashes

A **Threat Intelligence Platform (TIP)** can collect, centralize, and analyze threat intelligence from multiple sources.

> Threat intelligence feeds should add context to detections rather than completely drive detections without further assessment.

### Cyber Deception

**Cyber deception** uses techniques that deliberately deceive malicious actors to improve detection and defensive strategies.

#### Honeypots

A **honeypot** is a system or resource designed as a decoy to attract potential attackers.

Example:

A fake file labeled `Client Credit Card Information - 2022` could attract an attacker. An alert can be generated when the attacker attempts to access it.

---

## 3. Ongoing Monitoring of CI/CD

CI/CD pipelines can introduce security risks because attackers who compromise them may be able to:

- Inject malicious code
- Steal sensitive information
- Disrupt software releases
- Compromise the software supply chain

Continuous monitoring can automatically identify unusual pipeline activity and potential **Indicators of Compromise (IoCs)**.

### Common CI/CD IoCs

#### Unauthorized Code Changes

- Changes made by unauthorized users
- Changes from unexpected locations
- Changes at unusual times
- Suspicious or confusing code
- Very large unexplained deletions

#### Suspicious Deployment Patterns

- Deployments to unapproved systems
- Production deployments directly from developer branches
- Deployments at unusual times
- Deployments initiated by unusual accounts

#### Compromised Dependencies

- Dependencies containing known CVEs
- Unexpected new dependencies
- Dependencies downloaded from untrusted sources

#### Unusual Pipeline Execution

- Unexpected pipeline failures
- Significant increases in pipeline execution time
- Unexpected changes in pipeline step order

#### Secrets Exposure Attempts

- Attempts to access secrets from unauthorized pipeline locations
- Secrets accidentally or intentionally hardcoded in code

### CI/CD Monitoring

Important sources of monitoring data include:

- Pipeline execution logs
- Code commit logs
- Access logs
- Deployment logs

SIEM integration can help identify anomalies and known IoCs at scale.

### Automated Alerting

Alerts can be configured for:

- Repeated unusual build failures
- Suspicious code changes
- Attempts to expose secrets
- Unusual outbound network traffic

### Performance Monitoring

Performance problems can act as **Indicators of Attack (IoAs)** and may lead to further investigation that uncovers IoCs.

### Continuous Vulnerability Scanning

CI/CD infrastructure should be regularly checked for vulnerabilities such as **CVEs** in:

- CI/CD tools
- Plugins
- Containers

---

## 4. Indicators of Compromise (IoCs)

An **Indicator of Compromise (IoC)** is observable evidence that suggests a potential security incident.

Examples include:

- Malicious file hashes
- IP addresses
- Domains
- File names
- Network artifacts
- Host artifacts

### IoC vs IoA

**IoC:**

Evidence associated with something that may have already happened.

**IoA:**

A series of observed events or behaviors indicating an ongoing or real-time attack.

> **IoC = What / Who**  
> **IoA = How / Why**

IoCs do not always confirm an incident because they can sometimes result from human error, system malfunctions, or other non-malicious activity.

---

## 5. Pyramid of Pain

The **Pyramid of Pain**, created by security researcher David J. Bianco, describes different types of indicators and how difficult they are for attackers to overcome when blocked.

From lower to higher levels:

1. **Hash values**
   - Hashes associated with known malicious files.
   - Easy for attackers to overcome by changing the file.

2. **IP addresses**
   - IP addresses associated with malicious activity.
   - Attackers can potentially switch IP addresses.

3. **Domain names**
   - Domains associated with malicious activity.

4. **Network artifacts**
   - Observable evidence created by attackers on a network.
   - Example: User-Agent strings.

5. **Host artifacts**
   - Observable evidence created by attackers on a host.
   - Example: Malicious file names.

6. **Tools**
   - Software used by attackers to achieve their objectives.
   - Example: password-cracking tools.

7. **Tactics, Techniques, and Procedures (TTPs)**
   - The behavior and methods used by attackers.
   - TTPs are the most difficult for attackers to change and therefore represent the highest level of the Pyramid of Pain.

> The higher an indicator is on the Pyramid of Pain, the more difficult it generally becomes for attackers to adapt when defenders block it.

---

## 6. Investigating IoCs

A single IoC often does not provide enough information to understand an entire incident.

Security analysts should add **context** to IoCs by investigating related artifacts and activity.

For example, instead of only blocking a suspicious IP address, an analyst could investigate:

- Other network communications involving the IP
- Processes communicating with the IP
- Related domains
- Files associated with the activity
- Other systems affected by the same IoC

This helps analysts build a broader picture of the incident.

### Crowdsourcing

**Crowdsourcing** involves gathering information through public input and collaboration.

Threat intelligence platforms can use information shared by:

- Security professionals
- Security vendors
- Government agencies
- Cloud providers
- Other organizations

### OSINT

**Open-source intelligence (OSINT)** is the collection and analysis of information from publicly available sources to generate useful intelligence.

### Information Sharing

**Information Sharing and Analysis Centers (ISACs)** collect and share sector-specific threat intelligence with organizations within particular industries.

---

## 7. Investigative Tools

### VirusTotal

**VirusTotal** can be used to investigate suspicious:

- Files
- File hashes
- Domains
- URLs
- IP addresses

Important VirusTotal report sections include:

### Detection

Shows security vendors and their verdicts for an IoC.

### Details

Provides information from static analysis, such as:

- Hashes
- File type
- File size
- Headers
- Creation time
- Submission information

### Relations

Shows related IoCs such as:

- URLs
- Domains
- IP addresses
- Dropped files

### Behavior

Shows observed activity from controlled or sandboxed execution, including:

- Tactics and techniques
- Network communications
- Registry activity
- File system actions
- Processes

### Community

Contains comments and insights from members of the VirusTotal community.

### Vendors' Ratio and Community Score

The vendors' ratio indicates how many security vendors have identified the IoC as malicious.

The community score provides additional information based on the VirusTotal community.

> Data submitted to VirusTotal may be publicly shared. Sensitive or private information should not be uploaded.

### Other Investigative Tools

- **Jotti Malware Scan:** Scans suspicious files using multiple antivirus programs.
- **URLScan.io:** Scans and analyzes URLs.
- **MalwareBazaar:** Repository of malware samples used for research and threat intelligence.

### Malware Analysis Activity

A malware investigation activity was completed using:

- A SHA-256 malware hash
- VirusTotal
- Detection results
- Malware details
- Related IoCs
- Behavioral information
- Community information
- Pyramid of Pain analysis

The malware was identified as malicious based on its security-vendor detections and community information.

This activity provided practical experience with **IoC investigation, threat intelligence, malware analysis, and the Pyramid of Pain**.

---

## 8. Documentation in Incident Response

Documentation is an important part of incident response.

### Benefits of Documentation

Documentation provides:

- **Transparency** — creates a clear record of what happened and what actions were taken.
- **Standardization** — helps teams follow consistent processes.
- **Clarity** — makes investigations and decisions easier to understand.

### Chain of Custody

A **chain of custody** is the documented record of how evidence is collected, handled, transferred, and stored.

It helps establish the:

- **Accuracy** of evidence
- **Integrity** of evidence
- **Reliability** of evidence

### Broken Chain of Custody

A **broken chain of custody** occurs when there is an unexplained gap or failure in the documented handling of evidence.

This can raise questions about whether the evidence was altered, mishandled, or compromised.

---

## 9. Playbooks

A **playbook** is a documented set of procedures that guides security teams through responding to a specific type of security incident.

Playbooks help ensure that analysts:

- Follow a consistent process.
- Know what actions to take.
- Avoid missing important investigation steps.
- Respond efficiently.
- Document their actions consistently.

### Types of Playbooks

#### Non-automated

The analyst manually performs the actions described in the playbook.

#### Semi-automated

Some actions are automated while the analyst performs other actions manually.

#### Automated

The response process is largely performed automatically by security tools.

### Phishing Playbook Activity

A phishing incident response activity was completed using an organizational playbook.

The scenario involved:

- A phishing alert
- A suspicious file downloaded to an employee workstation
- Investigation of the attachment hash
- Verification that the attachment was malicious
- Following the organization's phishing response process
- Documenting findings in an incident handler's journal
- Updating the incident ticket

---

## 10. Incident Handler's Journal

An **Incident Handler's Journal** is used to document observations, investigation findings, and actions taken during incident response activities.

The journal serves as a chronological record of investigations completed during training.

The journal entries completed throughout the course can also serve as **portfolio evidence** demonstrating practical exposure to incident investigation and response.

---

## 11. Response and Recovery

### Triage

**Triage** is the process of quickly evaluating and prioritizing security incidents to determine what needs attention first and how urgently it should be handled.

### Importance of Triage

Security teams can receive many alerts simultaneously. Triage helps analysts:

- Identify the most important incidents.
- Prioritize incidents based on risk.
- Allocate appropriate resources.
- Prevent critical incidents from being overlooked.
- Make incident response more efficient.

Triage does not necessarily involve fully investigating an incident. Instead, it determines the appropriate next step and priority.

### Triage Process

#### 1. Receive & Assess

The analyst receives an alert or incident report and performs an initial assessment.

They may review:

- Alert type
- Affected user or system
- Time of activity
- IoCs
- Initial evidence
- Potential impact

#### 2. Assign Priority

Priority can be based on:

- **Severity**
- **Impact**
- **Urgency**
- **Scope**

Higher-risk incidents receive greater priority and may be escalated or investigated sooner.

#### 3. Collect & Analyze

The analyst collects and analyzes relevant evidence, such as:

- Logs
- Network traffic
- System information
- User activity
- IoCs
- Files or malware
- Authentication records
- Alert data

This helps validate the incident, determine its scope, and decide on the appropriate response.

---

## 12. Containment, Eradication, and Recovery

### Containment

**Containment** limits the damage caused by an incident and prevents the threat from spreading.

Examples:

- Isolating an infected device.
- Blocking malicious IP addresses or domains.
- Disabling compromised accounts.
- Restricting access to affected systems.
- Blocking malicious files or processes.

> **Containment = Stop or limit the spread.**

### Eradication

**Eradication** removes the threat and its root cause from the environment.

Examples:

- Removing malware.
- Deleting malicious files.
- Removing unauthorized accounts or access.
- Patching exploited vulnerabilities.
- Removing persistence mechanisms.
- Rebuilding compromised systems.

> **Eradication = Remove the threat.**

### Recovery

**Recovery** restores affected systems and operations to normal after the threat has been contained and eradicated.

Examples:

- Restoring systems from clean backups.
- Rebuilding compromised systems.
- Restoring normal network access.
- Resetting credentials.
- Monitoring restored systems.
- Confirming systems are functioning normally.

> **Recovery = Restore normal operations.**

---

## 13. Business Continuity Planning

A **Business Continuity Plan (BCP)** is a document that outlines procedures for sustaining business operations during and after a significant disruption.

A BCP helps ensure that critical business functions can continue or be quickly restored.

Security incidents can cause:

- Legal damage
- Financial damage
- Reputational damage
- Disruption of critical operations

### BCP vs Disaster Recovery Plan

**Business Continuity Plan (BCP):**

Focuses on maintaining and restoring critical **business operations** during and after a disruption.

**Disaster Recovery Plan (DRP):**

Focuses specifically on recovering **information systems** after a major disaster.

> **BCP = Keep the business operating.**  
> **DRP = Recover information systems.**

### Ransomware and Business Continuity

Ransomware can disrupt business operations by encrypting data and making critical systems unavailable.

For example, ransomware targeting healthcare organizations could prevent access to medical records and disrupt essential healthcare services.

BCPs help organizations minimize interruptions and maintain access to critical services.

---

## 14. Recovery Strategies

Organizations need recovery strategies to restore systems and return to normal operations following an outage or security incident.

### Resilience

**Resilience** is the ability to prepare for, respond to, and recover from disruptions.

### Site Resilience

**Site resilience** helps maintain the availability of networks, data centers, and other infrastructure during disruptions.

There are three types of recovery sites:

| Recovery Site | Description |
|---|---|
| **Hot site** | A fully operational duplicate of the primary environment that can be activated immediately. |
| **Warm site** | A configured and updated facility that is not immediately operational but can quickly be brought online. |
| **Cold site** | A backup facility with some necessary infrastructure that requires additional setup before becoming operational. |

### Easy way to remember

- 🔥 **Hot = Ready now**
- 🌡️ **Warm = Needs some preparation**
- ❄️ **Cold = Needs significant setup**

---

## Key Takeaways

Module 3 developed the incident response mindset required of a security analyst.

Key concepts include:

- Detecting and validating security incidents.
- Understanding limitations of automated detection.
- Using threat hunting and threat intelligence.
- Identifying and investigating IoCs and IoAs.
- Understanding the Pyramid of Pain.
- Adding context to IoCs using investigative tools.
- Using VirusTotal and other threat intelligence resources.
- Documenting investigations and maintaining evidence integrity.
- Following security playbooks.
- Performing incident triage.
- Containing and eradicating threats.
- Recovering affected systems.
- Understanding business continuity and resilience.

The overall incident response flow can be remembered as:

**Detect → Analyze → Triage → Contain → Eradicate → Recover → Maintain Continuity**
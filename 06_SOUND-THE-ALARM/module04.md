# Module 4 — Network Traffic and Logs Using IDS and SIEM Tools

## 1. Overview of Intrusion Detection Systems

### Intrusion Detection System (IDS)

An **IDS** monitors system or network activity and generates alerts when potential malicious activity is detected.

### Telemetry

**Telemetry** is the collection of data about activity occurring on systems, hosts, and networks. Security tools analyze this data to identify suspicious behavior.

### Host-Based IDS (HIDS)

A **HIDS** is installed on an individual endpoint/host and monitors activity on that host.

Can monitor:
- Inbound/outbound traffic
- File systems
- System resources
- User activity
- Unauthorized applications or changes

**Scope:** One host.

### Network-Based IDS (NIDS)

A **NIDS** monitors network traffic and network data across multiple devices.

It:
- Inspects network traffic
- Detects suspicious/malicious traffic
- Logs activity
- Generates alerts

**Scope:** Network traffic.

> **HIDS = individual host | NIDS = network**

Using both provides a more comprehensive view of an environment.

---

## 2. IDS Detection Techniques

### Signature-Based Analysis

Detects known threats by matching activity against predefined **signatures**.

A signature is a pattern associated with malicious activity, such as:
- IP addresses
- Byte sequences
- Malicious scripts
- Known attack patterns

**Advantages**
- Effective against known threats
- Generally low false-positive rate

**Limitations**
- Can be bypassed by modifying attack behavior
- Requires regular signature updates
- Cannot reliably detect unknown threats/zero-days

### Anomaly-Based Analysis

Detects activity that deviates from a baseline of normal behavior.

**Process:**
1. **Training:** Establish a baseline of normal activity.
2. **Detection:** Compare current activity against the baseline.
3. Deviations are logged and may generate alerts.

**Advantage**
- Can detect new/evolving threats.

**Limitations**
- Higher false-positive rate
- Existing compromises during training may become part of the baseline.

---

# 3. NIDS Rule Components

A NIDS signature/rule consists of three main components:

### Action
Defines what happens when traffic matches the rule.

Examples:
- `alert`
- `pass`
- `drop`
- `reject`

### Header
Contains traffic information such as:
- Source IP
- Destination IP
- Source port
- Destination port
- Protocol
- Traffic direction

### Rule Options
Provide additional conditions and customization for the signature.

> **Rule = Action + Header + Rule Options**

---

# 4. Suricata

**Suricata** is an open-source:
- Intrusion Detection System (IDS)
- Intrusion Prevention System (IPS)
- Network Security Monitoring (NSM) tool

### Suricata Modes

**IDS:** Monitors traffic and alerts on suspicious activity.

**IPS:** Detects and can block malicious traffic.

**NSM:** Collects and stores network activity/logs for monitoring, forensics, and incident response.

Suricata can analyze:
- Live network traffic
- Existing packet captures
- Network logs

---

# 5. Suricata Rules / Signatures

Suricata uses **rules/signatures** to identify suspicious patterns and conditions in network traffic.

The terms **rule** and **signature** are often used interchangeably.

### Predefined Rules

Suricata provides pre-written/template rules that detect known threats.

### Custom Rules

Security teams can modify or create rules based on their organization's environment.

Benefits:
- Tailored detection
- Better visibility
- Reduced false positives
- Detection specific to organizational requirements

> There is no one-size-fits-all rule set. Rules should be tested and customized.

### Rule Order

Suricata processes rules according to rule evaluation order.

Default action priority:

`pass → drop → reject → alert`

Rule order can affect the final verdict when multiple rules match the same packet.

---

# 6. Suricata Configuration

Suricata's main configuration file is:

`suricata.yaml`

It uses **YAML** syntax and controls how Suricata operates within the environment.

---

# 7. Suricata Logs

Suricata commonly generates two important log files:

### `eve.json`

The standard, detailed Suricata log.

Uses **EVE JSON** format and contains detailed event and alert metadata.

Useful for:
- Detailed analysis
- Incident response
- Threat hunting
- SIEM ingestion
- Correlating events using fields such as `flow_id`

### `fast.log`

A legacy, minimal alert log.

Contains basic information such as:
- Source/destination IP
- Ports
- Alert information

Less useful for detailed investigation compared with `eve.json`.

> **eve.json = detailed | fast.log = minimal/legacy**

---

# 8. EVE JSON Log Types

### Alert Logs

Record alerts generated when Suricata rules detect matching activity.

Useful for identifying:
- Triggered signatures
- Source/destination information
- Alert metadata

### Network Telemetry Logs

Record information about network activity and communications.

Useful for understanding:
- Network connections
- Protocol activity
- Traffic flows
- Communication patterns

---

# 9. Suricata Activity

In the Suricata lab:

- Examined the components of Suricata signatures.
- Used predefined/template signatures.
- Triggered a Suricata rule.
- Examined the resulting logs.
- Analyzed the generated alert/network information.

---

# 10. Security Information and Event Management (SIEM)

A **SIEM** collects, centralizes, and analyzes security logs and event data from multiple sources.

### SIEM Process

**Log Sources → Log Collection/Ingestion → Normalization/Processing → Centralized Storage → Search & Analysis → Detection/Alerts → Investigation & Response**

### Log Sources

Examples include:
- Servers
- Endpoints
- Network devices
- Applications
- Firewalls
- IDS/IPS
- Authentication systems

### Log Ingestion

**Log ingestion** is the process of collecting and sending logs from different sources into the SIEM for centralized analysis.

---

# 11. Splunk

**Splunk** is a SIEM/security analytics platform that uses **Search Processing Language (SPL)** to search and analyze events.

### Basic SPL Search

`index=main fail`

- `index=main` → searches the `main` index.
- `fail` → searches for events containing `fail`.

### Pipes

The `|` character chains SPL commands together.

Example:

`index=main fail | chart count by host`

The output of one command becomes the input for the next.

### Wildcards

`*` can match variable characters.

Example:

`index=main fail*`

Can match terms such as:
- `fail`
- `failed`
- `failure`

### Exact Phrase Search

Use quotation marks for an exact phrase:

`"login failure"`

This searches for the exact phrase rather than the individual words separately.

---

# 12. Google Security Operations (Chronicle)

Google SecOps provides different ways to search security events.

Two important search types are:

1. **UDM Search**
2. **Raw Log Search**

---

# 13. UDM Search

**Unified Data Model (UDM)** search queries security data that has been:

- Ingested
- Parsed
- Normalized
- Indexed

UDM searches are generally faster because they operate on structured data.

### Important UDM Fields

**Entities**
- Device
- User
- Process
- IP address

**Event Metadata**
- Event type
- Timestamp
- Other event information

**Network Metadata**
- Network and protocol information

**Security Results**
- Security outcomes such as malware detection or quarantine

### Example

`metadata.event_type = "USER_LOGIN"`

Searches for user login events.

---

# 14. Raw Log Search

Raw Log Search searches the original **unparsed logs**.

Useful when required information is not available through normalized/UDM data.

Can search for:
- Usernames
- Filenames
- Hashes
- Other raw log information

Raw searches are generally slower than UDM searches.

Raw Log Search also supports **regular expressions (regex)** for more specific pattern matching.

> **UDM Search = structured/normalized/faster**
>
> **Raw Log Search = unparsed/more flexible/slower**

---

# Key Revision Points

- **HIDS** monitors an individual host.
- **NIDS** monitors network traffic.
- **Signature analysis** detects known patterns.
- **Anomaly analysis** detects deviations from normal behavior.
- Suricata can operate as **IDS, IPS, and NSM**.
- Suricata rules contain **action, header, and rule options**.
- `suricata.yaml` is Suricata's main configuration file.
- `eve.json` provides detailed Suricata logs in **EVE JSON** format.
- `fast.log` provides minimal/legacy alert information.
- SIEMs **collect, centralize, search, and analyze logs**.
- **Splunk → SPL**
- **Google SecOps → UDM Search / Raw Log Search**
- **UDM = normalized structured data**
- **Raw Log = original unparsed data**
- SPL uses `|` to chain commands and `*` as a wildcard.
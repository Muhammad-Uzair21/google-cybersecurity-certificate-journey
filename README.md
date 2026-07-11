# 🛡️ Google Cybersecurity Professional Certificate Journey

![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Courses](https://img.shields.io/badge/Courses%20Completed-2%2F9-blue)
![Platform](https://img.shields.io/badge/Platform-Coursera-0056D2)
![Issuer](https://img.shields.io/badge/Issuer-Google-4285F4)

> Documenting my hands-on journey through the Google Cybersecurity Professional Certificate —
> course by course, concept by concept. I'm a final-year Software Engineering student
> transitioning into cybersecurity. My IT background means some courses move fast —
> but I'm here for the ones that don't.

---

---

## 📖 Disclaimer

These notes are my own summaries, explanations, and reflections while completing the Google Cybersecurity Professional Certificate. They are written in my own words for personal learning, interview revision, and knowledge sharing, and are **not** a replacement for or reproduction of the official course materials.

---

## 📑 Course Index

| #   | Course                                             | Status         | Key Topics                                     |
| --- | -------------------------------------------------- | -------------- | ---------------------------------------------- |
| 1   | Foundations of Cybersecurity                       | ✅ Complete    | CIA Triad, Security Domains, Threat History    |
| 2   | Play It Safe: Manage Security Risks                | ✅ Complete    | NIST, CISSP, SIEM, Playbooks, SOC Analyst Role |
| 3   | Connect and Protect: Networks and Network Security | 🟡 In Progress | —                                              |
| 4   | Tools of the Trade: Linux and SQL                  | 🔴 Not Started | —                                              |
| 5   | Assets, Threats, and Vulnerabilities               | 🔴 Not Started | —                                              |
| 6   | Sound the Alarm: Detection and Response            | 🔴 Not Started | —                                              |
| 7   | Automate Cybersecurity Tasks with Python           | 🔴 Not Started | —                                              |
| 8   | Put It to Work: Prepare for Cybersecurity Jobs     | 🔴 Not Started | —                                              |
| 9   | Accelerate Your Job Search with AI                 | 🔴 Not Started | —                                              |

**Legend:** ✅ Complete &nbsp; 🟡 In Progress &nbsp; 🔴 Not Started

---

## 📘 Course 1 — Foundations of Cybersecurity

<details>
<summary><b>Click to expand</b></summary>

### What This Course Covers

An entry-level overview of the cybersecurity landscape — who security analysts are,
what they do, and the foundational concepts that underpin the entire field.

### Key Concepts Learned

**🔐 The CIA Triad**
The three core principles every security decision is measured against:

- **Confidentiality** — only authorized people access the data
- **Integrity** — data is accurate and untampered
- **Availability** — systems and data are accessible when needed

**🏛️ The 8 CISSP Security Domains**
The eight domains that define the scope of cybersecurity work:
`Security & Risk Management` · `Asset Security` · `Security Architecture` ·
`Communication & Network Security` · `Identity & Access Management` ·
`Security Assessment & Testing` · `Security Operations` · `Software Development Security`

**⚔️ A Brief History of Cyber Attacks**

- Early attacks were curiosity-driven (Morris Worm, 1988)
- Evolved into financially and politically motivated threats
- Today's landscape: ransomware, state-sponsored attacks, social engineering at scale

**🧰 Core Toolkit of an Entry-Level Analyst**

- SIEM tools (Security Information and Event Management)
- Network protocol analyzers (e.g. Wireshark)
- Playbooks — step-by-step incident response guides

**📋 Security Frameworks & Controls**

- **NIST Cybersecurity Framework** — identify, protect, detect, respond, recover
- Controls exist at three levels: physical, technical, and administrative

### Honest Reflection

> This course is explicitly designed for people with zero IT background.
> My software engineering foundation meant I moved through it faster than the recommended pace —
> concepts like networking, OS structure, and programming references landed immediately.
> That said, I didn't skip it. Fundamentals explained clearly are worth revisiting,
> especially when you're about to teach them to someone else.

### Certificate

![Course 1 Certificate](certificates/course1.png)

</details>

---

## 📘 Course 2 — Play It Safe: Manage Security Risks

<details>
<summary><b>Click to expand</b></summary>

### What This Course Covers

A deeper look at how security professionals think about and manage risk — the frameworks
they follow, the tools they use, and what the day-to-day reality of a SOC analyst
actually looks like.

### Key Concepts Learned

**🏗️ Security Frameworks**

- **CISSP's 8 Security Domains** revisited in depth — understanding how risk maps across each domain
- **NIST Cybersecurity Framework (CSF)** — the industry standard for managing and reducing cybersecurity risk: Identify → Protect → Detect → Respond → Recover
- **NIST RMF (Risk Management Framework)** — the 7-step process organizations use to manage security risk formally

**📊 SIEM Tools**

- What Security Information and Event Management tools do — aggregate and analyze log data from across an organization in real time
- How analysts use SIEM dashboards to detect threats, monitor activity, and investigate incidents
- Introduction to tools like Splunk and Chronicle

**📋 Playbooks**

- What playbooks are — step-by-step guides analysts follow during specific incident types
- Why consistency matters in incident response — human error under pressure is a real threat
- How playbooks connect to the broader incident response lifecycle

**👤 Life of a SOC Analyst**

- What entry-level analysts actually do day-to-day — triaging alerts, investigating events, escalating incidents, documenting findings
- The tools, communication protocols, and decision frameworks they rely on
- Insights from Google security professionals — real stories, early mistakes, and what they wish they knew

### Honest Reflection

> Course 1 was familiar territory. Course 2 was the first time I felt genuinely challenged —
> not technically, but in how I think. Security at this level is less about code and more
> about judgment: what matters, what doesn't, and what you do when you're not sure.
> Hearing directly from people working security at Google made the career path feel real
> in a way that a textbook never could.

### Certificate

![Course 2 Certificate](certificates/course2.png)

</details>

---

## 📘 Course 3 — Connect and Protect: Networks and Network Security

<details>
<summary><b>Module 1 — Network Architecture & Fundamentals (click to expand)</b></summary>

### What This Module Covers
The foundational layer of how networks are designed, structured, and communicated across —
the concepts every security professional needs before they can understand how attacks travel
and where defences live.

### Key Concepts Learned

**🏗️ Network Architecture, Structure & Design**
- How networks are physically and logically organised — LANs, WANs, and the relationships between them
- Network topologies: how devices are arranged and how that affects performance and security
- The principle that how a network is *designed* directly determines how easy or hard it is to defend

**🛠️ Networking Tools & Devices**
- **Hub** — broadcasts to all devices; no intelligence, no segmentation
- **Switch** — sends data only to the intended device; operates at Layer 2
- **Router** — directs traffic between networks; operates at Layer 3
- **Firewall** — monitors and filters traffic based on rules; first line of network defence
- **Modem** — converts signal types to connect a local network to the internet
- Key insight: understanding what each device *does* tells you what an attacker targets and why

**☁️ Cloud Networks**
- Cloud computing moves network infrastructure off-premises — storage, servers, and services accessed remotely
- Three models: **IaaS** (infrastructure), **PaaS** (platform), **SaaS** (software)
- Security implication: the attack surface expands when resources live outside your physical control

**📦 TCP/IP Model**
The four-layer model that governs how data actually moves across the internet:
| Layer | Name | What happens here |
|---|---|---|
| 4 | Application | User-facing protocols — HTTP, HTTPS, DNS, SMTP |
| 3 | Transport | Breaks data into segments; TCP (reliable) vs UDP (fast) |
| 2 | Internet | IP addressing and routing — where packets go |
| 1 | Network Access | Physical transmission — cables, Wi-Fi, MAC addresses |

**🔷 OSI Model**
The seven-layer conceptual model used to troubleshoot and understand where in a network something breaks — or where an attack occurs:
| Layer | Name | Key concept |
|---|---|---|
| 7 | Application | What the user sees — browsers, email clients |
| 6 | Presentation | Data formatting, encryption, compression |
| 5 | Session | Opens, manages, and closes communication sessions |
| 4 | Transport | End-to-end delivery — TCP/UDP, ports |
| 3 | Network | IP addressing and routing |
| 2 | Data Link | MAC addresses, switches, frames |
| 1 | Physical | Cables, signals, bits |
> Security tip: attackers operate at specific OSI layers. Knowing the model tells you *where* in the stack a threat lives.

**🔑 IP vs MAC Addresses**
- **IP Address** — logical address assigned to a device on a network; can change; used for routing across networks (Layer 3)
- **MAC Address** — physical address burned into a network interface card; unique to the hardware; used for communication within a local network (Layer 2)
- Key distinction: IP gets the packet to the right *network*, MAC gets it to the right *device*

### Honest Reflection
> The OSI and TCP/IP models look like memorisation exercises until you realise they're
> actually a map of where things go wrong — and where attacks happen. Every layer is
> a potential entry point. That reframe made this module click.

</details>

<details>
<summary><b>Module 2 — Network Operations (click to expand)</b></summary>

### What This Module Covers
How data actually moves across networks, the protocols that govern it, and the security
tools organisations use to monitor, segment, and protect that traffic.

### Key Concepts Learned

**📡 Network Protocols**
Rules that govern how devices communicate — structure, order, and delivery of data.

| Protocol | Full Name | What it does |
|---|---|---|
| **TCP** | Transmission Control Protocol | Reliable, connection-based data streaming between two devices |
| **ARP** | Address Resolution Protocol | Translates IP addresses → MAC addresses on a local network |
| **DNS** | Domain Name System | Translates domain names → IP addresses |
| **HTTP** | Hypertext Transfer Protocol | Client-server communication for web traffic (unsecured) |
| **HTTPS** | HTTP Secure | Same as HTTP but encrypted — use this, always |
| **SSH** | Secure Shell | Encrypted remote access to another system's command line |
| **SFTP** | Secure File Transfer Protocol | Encrypted file transfers between devices |
| **SNMP** | Simple Network Management Protocol | Monitors and manages network devices |

> 🎯 **Interview tip:** Know TCP vs UDP — TCP is reliable (confirms delivery), UDP is fast (no confirmation). DNS uses UDP by default. HTTPS = HTTP + TLS encryption.

**📶 Wireless Protocols**
- **IEEE 802.11 (Wi-Fi)** — the standard defining wireless LAN communication
- **WPA / WPA2 / WPA3** — Wi-Fi Protected Access; each generation stronger than the last
- WPA3 is current gold standard; WPA (original) is broken and exploitable

**🔥 Firewalls**
Network security devices that monitor and filter incoming/outgoing traffic based on rules.

| Type | How it works |
|---|---|
| **Stateless** | Operates on predefined rules only — no memory of past packets |
| **Stateful** | Tracks ongoing connections — smarter, proactively filters threats |
| **Cloud-based** | Hosted by cloud provider — scales with your infrastructure |

- **Port filtering** — blocks or allows specific port numbers to control what traffic gets through

> 🎯 **Interview tip:** Stateful > Stateless. Stateful firewalls *remember* — they can detect anomalies mid-session. Stateless just checks rules and moves on.

**🔒 VPNs & Encapsulation**
- **VPN** — masks your public IP, encrypts your traffic, makes public networks safer
- **Encapsulation** — VPNs wrap your sensitive data *inside* other data packets to protect it in transit
- Common VPN protocols: OpenVPN, WireGuard, IPSec

**🗂️ Network Segmentation & Security Zones**

| Zone | What it is |
|---|---|
| **Uncontrolled zone** | Everything outside the organisation — the internet |
| **Controlled zone** | Internal subnet protected from the uncontrolled zone |
| **Security zone** | Segment of a network that isolates and protects internal resources |

- **Subnetting** — divides a network into logical groups (subnets) for organisation and security
- **CIDR** (Classless Inter-Domain Routing) — notation for defining subnet ranges e.g. `192.168.1.0/24`

> 🎯 **Interview tip:** Segmentation limits blast radius. If an attacker breaches one segment, they can't automatically move laterally to everything else.

**🔁 Proxy Servers**
Sit between a client and the internet — act as intermediaries.

| Type | Direction | Purpose |
|---|---|---|
| **Forward proxy** | Client → Internet | Controls/restricts what users can access |
| **Reverse proxy** | Internet → Internal server | Protects internal servers from direct exposure |

### Quick-Reference Glossary
> For fast revision before interviews

- **ARP** — IP → MAC translation on local network
- **CIDR** — subnet range notation (`/24` = 256 addresses)
- **DNS** — domain name → IP
- **Encapsulation** — VPN wraps data inside other packets
- **Firewall** — monitors + filters network traffic
- **HTTPS** — HTTP + encryption
- **Port filtering** — blocks/allows traffic by port number
- **Segmentation** — divides network into isolated zones
- **SFTP** — encrypted file transfer
- **SSH** — encrypted remote shell access
- **Stateful firewall** — tracks connections, smarter filtering
- **Stateless firewall** — rule-based only, no memory
- **Subnetting** — splitting a network into logical subnets
- **TCP** — reliable, connection-based protocol
- **VPN** — encrypts traffic, masks IP

### Honest Reflection
> Module 2 is where networking stops being abstract and starts being security-relevant.
> Every protocol is a potential attack surface. Every firewall type is a tradeoff.
> The segmentation concept alone — limit the blast radius — is something that comes up
> in every security conversation worth having.

</details>

<details>
<summary><b>Module 3 — Secure against network intrusions (click to expand)</b></summary>

### What This Module Covers
How attackers abuse network communication, the common techniques used to disrupt or intercept
traffic, and the tools security analysts use to inspect packets and investigate suspicious
network activity.

### Key Concepts Learned

**💥 Denial-of-Service (DoS) Attacks**

A **Denial-of-Service (DoS)** attack attempts to make a system or network unavailable by
overwhelming it with excessive traffic or requests.

| Attack | How it works |
|---|---|
| **SYN Flood** | Exploits TCP's three-way handshake by leaving many connections half-open |
| **ICMP Flood** | Overwhelms a target with ICMP (ping) requests |
| **Ping of Death** | Sends malformed or oversized ping packets to crash vulnerable systems (largely historical) |

> 🎯 **Interview tip:** DoS = one attacker targets one victim. DDoS = many compromised devices attack simultaneously.

---

**📦 Network Protocol Analyzers**

Security analysts inspect packets to understand how devices communicate and identify
malicious activity.

**Common Tool**
- **tcpdump** — lightweight command-line packet analyzer for capturing live network traffic

Typical packet output includes:
- **Timestamp** — when the packet was captured
- **Source IP : Port** — sender
- **Destination IP : Port** — receiver

Common uses:
- Monitor network traffic
- Troubleshoot connectivity issues
- Investigate suspicious activity
- Verify network configurations

> 🎯 **Interview tip:** Packet analyzers don't generate traffic—they observe existing traffic.

---

**🕵️ Packet Sniffing**

Packet sniffing captures and inspects network traffic. While commonly used for troubleshooting,
attackers can also use it to steal sensitive information.

| Type | Description |
|---|---|
| **Passive Sniffing** | Silently listens to traffic without modifying it |
| **Active Sniffing** | Manipulates network traffic (such as ARP spoofing) to intercept packets |

> 🎯 **Interview tip:** Passive = listens. Active = manipulates.

---

**🎭 IP Spoofing**

IP spoofing is the practice of forging the source IP address of packets to disguise the attacker
or impersonate another device.

| Attack | Description |
|---|---|
| **On-path Attack** | Attacker positions themselves between communicating devices to intercept or modify traffic |
| **Replay Attack** | Previously captured legitimate packets are resent to gain unauthorized access |
| **Smurf Attack** | Victim's spoofed IP is used to trigger massive ICMP replies from multiple devices |

---

**🛡️ Protecting Network Traffic**

Common defensive measures include:

- **Encryption** — protects data in transit from packet sniffing
- **Firewall configuration** — blocks suspicious or spoofed traffic (e.g., rejecting incoming packets claiming to originate from the local network)
- Traffic monitoring using packet analyzers
- Network segmentation to reduce attack impact

### 🧪 Hands-On Activities

<details>
<summary><b>Activity 1 — Analyze Network Layer Communication</b></summary>

**Scenario:**
Security analyst at a company. A client calls reporting users can't access `yummyrecipesforme.com` — the page returns: *"Port 23 unreachable."*

**Task:** Analyze tcpdump logs and produce a findings report.

**What I did:**
- Reviewed tcpdump packet capture logs to trace the communication failure
- Identified that traffic was being directed to **Port 23** (Telnet) — an unencrypted, legacy protocol that should not be in use
- Traced the issue to a misconfiguration at the **network layer** — packets were not reaching their intended destination

**Key Finding:**
Port 23 (Telnet) was unreachable — either blocked by a firewall or not listening on the server. The error surfaced at the **Internet layer** of the TCP/IP model, where routing and addressing determine whether a packet reaches its destination.

**Takeaway:**
> Reading tcpdump output tells you *where* a failure lives in the stack. "Port unreachable" = the packet arrived at the right IP but no service was listening on that port — a network/transport layer issue, not an application one.

</details>

<details>
<summary><b>Activity 2 — Analyze a Network Attack</b></summary>

**Scenario:**
Cybersecurity analyst at a travel agency. Employees use the company website to manage deals and discounts. Monitoring system fires an alert — website is unreachable. Browser returns: *"Unable to reach server."*

**Task:** Analyze Wireshark logs, identify the attack type, explain the damage, and propose a mitigation.

**What I found in the logs:**
A single IP address was repeatedly sending **SYN packets** to the server. After each SYN, the server responded with a **SYN-ACK** (as expected in a normal TCP handshake) — but the client never sent the final **ACK** to complete the connection. This cycle repeated continuously, filling the server's connection table with half-open connections until it was exhausted and unable to serve legitimate users.

**Attack identified: SYN Flood (DoS)**

| Stage | Normal handshake | What happened |
|---|---|---|
| 1 | Client sends SYN | ✅ Attacker sends SYN |
| 2 | Server responds SYN-ACK | ✅ Server responds SYN-ACK |
| 3 | Client sends ACK | ❌ Attacker never completes — connection left half-open |

**Damage caused:**
- Server's connection queue filled with half-open connections
- Legitimate users could not establish connections
- Website effectively taken offline — full denial of service

**Mitigation applied (optional task):**
1. Configured firewall to **block the attacking IP address** immediately
2. Enabled a rule to **automatically block IPs** that send repeated SYN requests without completing the handshake — preventing future SYN flood attempts and reducing manual response time

**Takeaway:**
> A SYN flood doesn't need to "hack" anything — it just exploits how TCP works. The fix isn't just blocking one IP; it's building a firewall rule that detects and drops the pattern automatically. That's the difference between reacting and defending.

</details>

### Quick-Reference Glossary

> Fast interview refresh

- **DoS** — overwhelm one target to deny service
- **DDoS** — distributed DoS using many compromised devices
- **SYN Flood** — exhausts TCP connections
- **ICMP Flood** — excessive ping requests
- **Ping of Death** — oversized/malformed ICMP packets
- **tcpdump** — command-line packet analyzer
- **Packet Sniffing** — capturing network traffic
- **Passive Sniffing** — listens only
- **Active Sniffing** — intercepts by manipulating traffic
- **IP Spoofing** — forged source IP address
- **On-path Attack** — attacker sits between two communicating devices
- **Replay Attack** — resend captured legitimate packets
- **Smurf Attack** — spoofed ICMP amplification attack
- **Encryption** — protects intercepted data
- **Firewall Filtering** — blocks unauthorized or spoofed traffic

### Honest Reflection

> This module felt like the turning point of Course 3. Earlier modules explained *how*
> networks work; this one focused on *how attackers abuse them*. Learning to read packet
> captures and recognize attacks like SYN floods or spoofing made networking feel much
> more practical from a defender's perspective.

</details>

## 🗂️ Certificates

| Course                                         | Certificate                      |
| ---------------------------------------------- | -------------------------------- |
| Course 1 — Foundations of Cybersecurity        | [View](certificates/course1.png) |
| Course 2 — Play It Safe: Manage Security Risks | [View](certificates/course2.png) |

---

## 👤 About Me

Final-year Software Engineering student pivoting into cybersecurity.
Background in networking, OS, and programming — now building on top of it with
hands-on security skills, teaching experience, and public documentation of everything I learn.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5)](https://www.linkedin.com/in/muhammad-uzair-j21/)

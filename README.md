# 🛡️ Google Cybersecurity Professional Certificate Journey

![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Courses](https://img.shields.io/badge/Courses%20Completed-1%2F9-blue)
![Platform](https://img.shields.io/badge/Platform-Coursera-0056D2)
![Issuer](https://img.shields.io/badge/Issuer-Google-4285F4)

> Documenting my hands-on journey through the Google Cybersecurity Professional Certificate —
> course by course, concept by concept. I'm a final-year Software Engineering student
> transitioning into cybersecurity. My IT background means some courses move fast —
> but I'm here for the ones that don't.

---

## 📑 Course Index

| #   | Course                                             | Status         | Key Topics                                     |
| --- | -------------------------------------------------- | -------------- | ---------------------------------------------- |
| 1   | Foundations of Cybersecurity                       | ✅ Complete    | CIA Triad, Security Domains, Threat History    |
| 2   | Play It Safe: Manage Security Risks                | 🟡 In Progress | NIST, CISSP, SIEM, Playbooks, SOC Analyst Role |
| 3   | Connect and Protect: Networks and Network Security | 🔴 Not Started | —                                              |
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
<summary><b>Module 2 — updating after completion</b></summary>

*Coming soon...*

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

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5)](<(https://www.linkedin.com/in/muhammad-uzair-j21/)>)

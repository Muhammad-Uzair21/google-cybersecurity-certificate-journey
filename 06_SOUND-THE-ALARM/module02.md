# Module 02 | Network Monitoring and Analysis

## 📌 Overview

Network monitoring and analysis is a core cybersecurity skill used to understand network traffic, identify suspicious activity, investigate indicators of compromise (IoCs), and detect potential attacks.

This module focused heavily on practical packet analysis using **Wireshark** and **tcpdump**, including capturing, filtering, and investigating network traffic.

---

## 🌐 Understanding Network Traffic

### Network Traffic
**Network traffic** is the amount of data moving across a network. It can also describe the type of data being transferred, such as HTTP traffic.

### Network Data
**Network data** is the information transmitted between devices on a network.

### Network Flow
**Network flow** describes the movement of network communications and includes information such as:
- Packets
- Protocols
- Ports
- Source and destination IP addresses
- Amount of data transferred
- Time of communication

### Network Baseline
A **baseline** is a reference point representing normal or expected network behavior.

Security analysts compare current network activity against the baseline to identify unusual behavior.

Examples of deviations include:
- Unusually large data transfers
- Traffic occurring outside normal business hours
- Unexpected protocols or ports
- Unusual source or destination IP addresses

### Indicators of Compromise (IoCs)
**Indicators of compromise (IoCs)** are signs that may indicate a security incident or malicious activity.

Examples include:
- Unusual network connections
- Unexpected IP addresses
- Abnormal traffic patterns
- Suspicious data transfers

### Command and Control (C2)
**Command and control (C2)** refers to techniques used by threat actors to maintain communication with compromised systems.

Attackers may use unusual combinations of protocols and ports to maintain C2 communication.

---

## 📤 Data Exfiltration

**Data exfiltration** is the unauthorized transfer of sensitive data from an organization or system to an external location controlled by an attacker.

### Data Exfiltration Process
From an attacker's perspective, the general process involves:
1. Gain access to the target environment.
2. Identify valuable or sensitive data.
3. Collect and prepare the data.
4. Establish a method for transferring the data.
5. Transfer the data outside the organization.
6. Attempt to avoid detection.

### Defensive Measures

**Prevent Attacker Access** — reduce the likelihood of attackers gaining initial access through controls such as:
- Multi-factor authentication (MFA)
- Strong security policies
- Employee security awareness training
- Access controls
- Regular software updates

**Monitor Network Activity** — look for unusual network behavior, such as:
- Multiple logins from unusual IP addresses
- Unexpected connections to external systems
- Large or unusual data transfers
- Traffic outside normal operating hours

**Protect Assets** — maintain an accurate **asset inventory** so security teams know:
- What systems and devices exist
- Where sensitive information is stored
- Which systems require additional protection
- What should be monitored

**Detect and Stop Exfiltration** — security teams can use:
- IDS/IPS
- Network monitoring
- Data Loss Prevention (DLP)
- Firewall rules
- SIEM alerts
- Traffic analysis
- Access controls

---

# 📡 Capture and View Network Traffic

## Packets

A **data packet** is a basic unit of information transmitted between devices on a network.

Packets contain three main components:

- **Header** — Contains information used to route and process the packet, such as source/destination addresses, protocol, packet length, identification information, and other control information.
- **Payload** — Contains the actual data being transmitted.
- **Footer / Trailer** — May contain error-checking information. Ethernet uses a footer/trailer, while most protocols such as IP do not.

---

## IPv4 Header

IPv4 uses **13 header fields**:

1. **Version** — Indicates the IP version.
2. **Internet Header Length (IHL)** — Specifies the length of the IPv4 header.
3. **Type of Service (ToS)** — Provides information about packet priority.
4. **Total Length** — Total length of the IP packet.
5. **Identification** — Identifies fragments belonging to the same original packet.
6. **Flags** — Provides information about fragmentation.
7. **Fragment Offset** — Identifies the correct sequence of fragments.
8. **Time to Live (TTL)** — Limits how long a packet can travel through a network.
9. **Protocol** — Specifies the protocol used for the packet's data.
10. **Header Checksum** — Used for error-checking the header.
11. **Source Address** — Address of the sender.
12. **Destination Address** — Address of the receiver.
13. **Options** — Optional additional information.

---

## IPv6 Header

IPv6 uses **8 header fields**:

1. **Version** — Indicates IPv6.
2. **Traffic Class** — Provides packet priority/class information.
3. **Flow Label** — Identifies packets belonging to the same flow.
4. **Payload Length** — Specifies the length of the packet's data.
5. **Next Header** — Indicates the type of header that follows.
6. **Hop Limit** — Limits how long the packet can travel.
7. **Source Address** — Address of the sender.
8. **Destination Address** — Address of the receiver.

---

## 🔎 Network Protocol Analyzers

**Network protocol analyzers**, also called **packet sniffers**, are tools used to capture and analyze network traffic.

Examples:
- Wireshark
- tcpdump
- TShark

Uses include:
- Investigating suspicious network activity
- Monitoring network communications
- Troubleshooting network problems
- Collecting network statistics
- Analyzing packet captures

### Promiscuous / Monitoring Mode

A network interface normally listens only for traffic addressed to it.

**Promiscuous mode** allows a NIC to access visible network packets on applicable interfaces. For wireless interfaces, this is commonly referred to as **monitoring mode**.

> These modes do not automatically provide visibility into all network traffic. The analyzer must be positioned appropriately within the network.

---

## 📦 Packet Capture (P-cap)

**Packet sniffing** is the practice of capturing and inspecting network packets.

A **packet capture (p-cap)** is a file containing captured network packets from a network interface or network. P-caps can be filtered and analyzed later using network protocol analyzers.

### Packet Capture Libraries and Formats

| Library / Format | Description |
|---|---|
| **Libpcap** | Packet capture library commonly used on Unix-like systems |
| **WinPcap** | Older packet capture library for Windows |
| **Npcap** | Modern packet capture library commonly used on Windows |
| **PCAPng** | Modern "next generation" packet capture format |

---

# 🦈 Wireshark

**Wireshark** is an open-source graphical network protocol analyzer used to capture and investigate network traffic. It provides detailed packet dissection and allows analysts to inspect different protocol and data layers.

## Display Filters

Wireshark display filters allow analysts to isolate packets relevant to an investigation.

Filters can be based on:
- Protocols
- IP addresses
- MAC addresses
- Ports
- Packet fields
- Specific text
- Regular expressions

### Comparison Operators

| Operation | Symbol | Abbreviation |
|---|---|---|
| Equal | `==` | `eq` |
| Not equal | `!=` | `ne` |
| Greater than | `>` | `gt` |
| Less than | `<` | `lt` |
| Greater than or equal | `>=` | `ge` |
| Less than or equal | `<=` | `le` |

Comparison operators can be combined with Boolean operators such as `and`, `or`, `not`. Parentheses can be used to group expressions.

### Common Protocol Filters

```
dns
http
ftp
ssh
arp
telnet
icmp
```

### IP Address Filters

Filter packets containing an IP address:
```
ip.addr == 172.21.224.2
```

Filter by source IP:
```
ip.src == 10.10.10.10
```

Filter by destination IP:
```
ip.dst == 4.4.4.4
```

### MAC Address Filter

```
eth.addr == 00:70:f4:23:18:c4
```

### Port Filters

UDP port:
```
udp.port == 53
```

TCP port:
```
tcp.port == 25
```

### Contains Operator
The **contains** operator filters packets containing a specified string of text.

### Matches Operator
The **matches** operator filters packets using a specified **regular expression (regex)**.

### Follow Streams
Wireshark's **Follow Stream** feature reconstructs a protocol conversation so analysts can examine the exchanged data in a readable format. This can be useful for investigating conversations such as HTTP requests and responses.

---

## 🧪 Wireshark Activity — Investigate Network Traffic

A packet capture containing web-browsing traffic was analyzed using Wireshark. The activity involved:
- Opening and exploring a packet capture
- Inspecting the Wireshark interface
- Examining individual packets and their protocol layers
- Identifying source and destination IP addresses
- Identifying protocols used during the connection
- Applying display filters
- Investigating UDP/DNS traffic
- Filtering TCP traffic
- Searching packet payloads for specific text

This provided hands-on practice with **packet capture investigation and Wireshark filtering**.

---

# 🐧 Packet Inspection with tcpdump

## What is tcpdump?

**tcpdump** is a command-line network protocol analyzer used to capture and view network communications. It can:
- Capture live network traffic
- Display packets in the terminal
- Save traffic to packet capture files
- Read previously captured packets
- Filter traffic
- Support network troubleshooting and security investigations

tcpdump is commonly available on Linux and other Unix-based systems.

---

## tcpdump Syntax

```bash
sudo tcpdump [-i interface] [option(s)] [expression(s)]
```

**`-D`** — Lists available network interfaces.
```bash
sudo tcpdump -D
```

**`-i`** — Specifies the interface to capture from.
```bash
sudo tcpdump -i any
```

**`-w`** — Writes captured packets to a packet capture file.
```bash
sudo tcpdump -i any -w packetcapture.pcap
```

**`-r`** — Reads packets from an existing capture file.
```bash
sudo tcpdump -r packetcapture.pcap
```

**`-v`** — Enables verbose output.
```bash
sudo tcpdump -r packetcapture.pcap -v
```
Verbosity can be increased with `-v`, `-vv`, `-vvv`.

**`-c`** — Controls the number of packets captured.
```bash
sudo tcpdump -i any -c 3
```

**`-n`** — Disables hostname resolution.
```bash
sudo tcpdump -r packetcapture.pcap -v -n
```

**`-nn`** — Disables both hostname and port-name resolution. Using `-n` or `-nn` can help preserve accurate numerical information during analysis and avoid unnecessary name-resolution activity.

**Combining Options** — options can be combined:
```bash
sudo tcpdump -r packetcapture.pcap -vn
```

---

## tcpdump Filter Expressions

Expressions allow analysts to isolate specific traffic.

Filter IPv6 traffic:
```
ip6
```

Filter IPv4 traffic on port 80:
```bash
sudo tcpdump -r packetcapture.pcap -n 'ip and port 80'
```

Multiple conditions can be combined with `and`, `or`, `not`. Parentheses can be used to group expressions.

Example:
```
ip and (port 80 or port 443)
```

---

## Interpreting tcpdump Output

A tcpdump output line typically contains:
1. **Timestamp** — Time the packet was captured.
2. **Source IP** — Origin of the packet.
3. **Source port** — Port from which the packet originated.
4. **Destination IP** — Destination of the packet.
5. **Destination port** — Port receiving the packet.
6. **TCP details** — Information such as flags and sequence numbers.
7. **Options** — Additional packet information shown with verbose output.

---

## 🧪 tcpdump Activity — Capture and Analyze Live Network Traffic

A Linux virtual machine was used to practice tcpdump. The activity involved:
- Identifying available network interfaces
- Filtering live network traffic
- Capturing packets with tcpdump
- Filtering captured packet data
- Analyzing a provided packet capture file

This provided hands-on experience with **command-line packet capture and analysis**.

---

# ⚖️ Wireshark vs. tcpdump

| Feature | Wireshark | tcpdump |
|---|---|---|
| Interface | GUI | CLI |
| Packet analysis | Detailed | Lightweight/basic |
| Traffic capture | ✓ | ✓ |
| Packet filtering | ✓ | ✓ |
| Automation | Limited compared to CLI workflows | Strong |
| Resource usage | Generally heavier | Lightweight |
| Main strength | Detailed visual investigation | Fast command-line capture and filtering |

### Similarities

Both tools:
- Are network protocol analyzers
- Capture and analyze network traffic
- Are open-source and free
- Support packet capture through **libpcap**
- Can be used for security investigations and troubleshooting

---

## 🧪 Research Activity — Wireshark vs. tcpdump Comparison

A comparison chart was created to research the similarities and differences between Wireshark and tcpdump. The research compared:
- Interface and usability
- Packet analysis capabilities
- Resource requirements
- Capture capabilities
- Filtering
- Automation
- Common security use cases

The activity reinforced the difference between **GUI-based packet analysis with Wireshark** and **CLI-based packet analysis with tcpdump**.

---

# 🧠 Key Learnings

By completing this module, I developed an understanding of:
- Network traffic and network flow
- Network monitoring and baselines
- Indicators of compromise (IoCs)
- Data exfiltration and defensive measures
- Packets and packet structure
- IPv4 and IPv6 headers
- Packet captures and p-cap formats
- Network protocol analyzers
- Wireshark packet analysis
- Wireshark display filters
- Following network streams
- tcpdump packet capture
- tcpdump filtering and command-line analysis
- Interpreting packet data
- Comparing Wireshark and tcpdump

---

## 🛠️ Practical Skills

- Capturing network traffic
- Analyzing packet captures
- Filtering network traffic
- Investigating DNS and TCP traffic
- Identifying source and destination addresses
- Inspecting packet headers and payloads
- Using Wireshark for network investigations
- Using tcpdump from the Linux command line
- Identifying suspicious network behavior
- Comparing network analysis tools

---

## ➡️ Next Module

[Module 03 | Incident Investigation and Response](module03.md)
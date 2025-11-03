# 🧠 Threat Intelligence Investigation & Attack Simulation
### Real-World Profiling of a Threat Actor Against a Chosen Domain

**Author:** Bernard Mbata
**Role:** Cybersecurity Analyst | Threat Intelligence & SOC Operations
**Date:** 2025

---

## 🕵️ Project Overview
This project performs a **threat intelligence investigation and simulated cyberattack** against a chosen target domain (**samsung.com**) using **Open-Source Intelligence (OSINT)** tools and **MITRE ATT&CK Framework** mapping.

The objective was to:
1. Profile a **real-world threat actor** (Andariel, a North-Korean state-sponsored group).
2. Simulate the attacker’s potential behavior and tactics using legitimate threat intelligence techniques.
3. Recommend **defensive countermeasures** and **mitigation strategies** for enterprise environments.

---

## ⚙️ Tools & Frameworks Used
| Category | Tools / Frameworks |
|-----------|--------------------|
| Threat Intelligence | MITRE ATT&CK, Wazuh SIEM, IBM QRadar |
| OSINT Reconnaissance | TheHarvester, Whois, Shodan, Google Dorking, SSLScan |
| Malware Analysis | Amadey (Trojan Bot), DTrack RAT |
| Visualization | Kill Chain Model, Attack Simulation Diagram |

---

## 🎯 Threat Actor Profile — *Andariel*
- **Affiliation:** North Korean, subset of the **Lazarus Group**
- **Active Since:** 2009
- **Operations:** Cyber espionage, destructive attacks, and financial theft targeting South Korea’s government, banks, ATMs, and cryptocurrency exchanges.
- **Notable Campaigns:** *Operation Black Mine*, *GoldenAxe*, *Campaign Rifle*
- **Associated Malware:**
- **Amadey** (Trojan bot for initial infection & persistence)
- **DTrack** (used for data exfiltration & reconnaissance)
- **RATs** (for lateral movement and C2 access)

---

## 🧩 Mapped MITRE ATT&CK Techniques (TTPs)
| ID | Technique | Description |
|----|------------|-------------|
| **T1016** | System Network Configuration Discovery | Adversary collects network configuration and MAC/IP details. |
| **T1033** | System Owner/User Discovery | Identifies user accounts and privileges for lateral movement. |
| **T1082** | System Information Discovery | Gathers OS version, architecture, and hardware data for exploitation. |
| **T1003** | OS Credential Dumping | Extracts stored credentials for privilege escalation. |
| **S1028** | Amadey | Malware enabling data collection and persistence. |

🔗 References: [MITRE ATT&CK](https://attack.mitre.org/techniques/T1082)

---

## 🔗 Attack Simulation Overview
The simulation follows the **Lockheed Martin Cyber Kill Chain**, demonstrating each stage of a potential Andariel-style attack.

| Phase | Description | Tools Used |
|-------|--------------|------------|
| **Reconnaissance** | Identified domains, subdomains, DNS data, and open ports | TheHarvester, Shodan, Whois |
| **Weaponization** | Crafted malware payload similar to *Amadey* | Controlled simulation |
| **Delivery** | Email phishing & watering hole attack simulation | Google Dorking & OSINT scenario |
| **Exploitation** | Target vulnerability exploited for access | Simulated |
| **Installation** | Malware installs persistence mechanism | Modeled via Amadey behavior |
| **Command & Control (C2)** | Maintained remote access | RAT simulation |
| **Actions on Objectives** | Data exfiltration or destruction | Simulated through MITRE mapping |

📊 *A visual diagram of the attack path was included in the presentation.*

---

## 📋 Executive Summary
The research profiled **Andariel**, a **state-sponsored APT** known for its espionage operations and destructive malware campaigns.
Through OSINT, sandbox analysis, and MITRE mapping, the simulation demonstrated how adversaries infiltrate enterprise networks, gain persistence, and exfiltrate sensitive data.

**Key Findings:**
- Spear-phishing and watering-hole attacks remain primary entry points.
- Use of **DTrack**, **Amadey**, and RATs for lateral movement and credential theft.
- Exploitation of **unpatched systems** and **weak credentials** for long-term persistence.

---

## 🧰 Recommendations
### 1️⃣ Strengthen Endpoint Detection & Response (EDR)
- Deploy EDR platforms integrated with **SIEM** (e.g., Wazuh, QRadar).
- Detect and isolate abnormal behavior in real time.

### 2️⃣ Harden Email & Web Gateways
- Enforce attachment/link sandboxing and phishing filters.
- Block high-risk MIME types and inspect outbound traffic.

### 3️⃣ Access Control & Authentication
- Enable **Multi-Factor Authentication (MFA)** for all remote and privileged accounts.
- Apply the **Principle of Least Privilege (PoLP)**.

### 4️⃣ Patch Management & Vulnerability Scanning
- Schedule weekly patch cycles.
- Prioritize vulnerabilities with known exploits.

### 5️⃣ Employee Awareness
- Conduct regular phishing simulations and cyber hygiene training.
- Promote compliance awareness (GDPR, CCPA, NIST).

### 6️⃣ Threat Intelligence Integration
- Correlate Indicators of Compromise (IOCs) with threat feeds.
- Automate alerts through **SIEM** and **Threat Intelligence Platforms (TIPs)**.

---

## 🧠 Lessons Learned
- OSINT and ATT&CK mapping help visualize real-world attacker workflows.
- Threat simulation improves defensive readiness without real exploitation.
- Continuous intelligence and monitoring are critical for proactive defense.

---

## 📁 Repository Contents
| File | Description |
|------|--------------|
| `Threat_Intelligence_Project.pdf` | Full report presentation |
| `README.md` | Project summary (this file) |
| `/images/` | Diagrams: Kill Chain, MITRE mapping, and simulation visuals |

---

## 👨‍💻 Author
**Bernard Mbata**
Cybersecurity Analyst | Ethical Hacker | Incident Response
📫 [LinkedIn](https://linkedin.com/in/bernard-mbata)
🌐 GitHub: [@mbatabernard](https://github.com/mbatabernard)

---

> ⚠️ **Disclaimer:** This project was conducted in a *controlled academic environment* for educational and ethical cybersecurity research.
> No real systems were targeted or exploited.

## Active Directory (In Progress)
### On TryHackMe Platform
* **What I learned today:** I am progressing through my Active Directory rooms on TryHackMe.
* **Next Steps:** I am going to move on to Module 4 in the next session.

## Google Cybersecurity Certificate (Day 3/60)
### Today I successfully completed Module 1
* **Today's Progress:** As of now, I successfully completed my Foundations chapter and am heading to "Play It Safe".
* **Milestone:** I completed my very first module inside "Play It Safe".

## Hack The Box Academy 
### Introduction to Academy (Completed)
* **Today's Progress:** Successfully completed the entire introductory module.
* **Skills Learned:** Learned how to navigate the platform, spawn interactive target instances, and interact with live cloud labs using the built-in Pwnbox terminal.
* **Next Steps:** Moving on to the **Web Requests** module next to study cloud communication fundamentals.  

## WHAT I LEARN TODAY  Frameworks and security (completed the module) 
###  On  Google cybersecurity 
* **what i learn today (Day4) :** Frameworks and security and i succuesfully completed my module * **
* **Next steps:** Entering module 3* **
### The Main Goal:** The CIA Triad
* **Confidentiality:** Keeping data private so only the right people can see it.
*  **Integrity:** Making sure data doesn’t get messed with or changed
*  **vailability:** Ensuring systems actually work when someone needs them.
### The 6 Functions of NIST CSF 2.0
* **Govern,
* ** Identfy
* ** Protect
* **Detect
* **Respond
* **Recover

  # TryHackMe: Active Directory Basics - Write-up & Reference

A comprehensive breakdown and documentation of core Active Directory (AD) concepts, completed via TryHackMe.

## 🎯 Key Concepts Mast

### 🔹 1. Windows Domains & Architecture
* **Domain Controllers (DC):** Understood the role of DCs as the central authority managing security authentication and requests.
* **Trees, Forests & Trusts:** Learnt how multi-domain environments establish trust boundaries and handle cross-domain resource access.

### 🔹 2. Active Directory Infrastructure
* **Objects & OUs:** Explored how Users, Groups, and Computers are organized inside Organizational Units (OUs).
* **Database (NTDS.dit):** Understood where AD stores its directory data, cryptographic hashes, and group memberships.

### 🔹 3. Identity & Access Management (IAM)
* **User & Computer Lifecycle:** Documented the provisioning, management, and de-provisioning of accounts within a domain.
* **Authentication Protocols:** Studied how **Kerberos** (tickets, TGT, TGS) and **NTLM** function to authenticate users securely.

### 🔹 4. Enterprise Administration & Security
* **Group Policy Objects (GPOs):** Analyzed how administrators enforce security baselines, software deployment, and registry settings across thousands of endpoints.
* **Privileged Access:** Examined the differences between Domain Admins, Enterprise Admins, and standard users.

# Module 3: Introduction to Cybersecurity On Google Cybersecurity Certificate
* **Knowledge:** SIEM-and-Log-Analysis
* **Tools Studied:** Learn about open source tools like Linux & Suricata

## SIEM Deployment Models Looked At:
* **Cloud-Native:** Fully managed in the cloud (e.g., Google Chronicle, Splunk Cloud). Offers fast scaling and low maintenance.
* **Self-Hosted / On-Premises:** Installed on an organization's private servers (e.g., Splunk Enterprise) for maximum data control.
* **Hybrid:** Combines on-premise log collection with cloud-based analytics to balance security and scalability.

## MODULE 4: Use playbooks to Respond Incidents
* **Core Focus:** I Actually learned the phases of "INCIDENT RESPONSE"
* **PREPARATION:** Establishing tools, resources, training necessary to respond to incidents before they actually happen
* **Detection and Analysis:** monitoring security alerts and logs using SIEM tools, identify a threat
* **Containment:** Taking immediate action to isolate the threat and prevent it from spreading and causing further damage to the network
* **Incident response [Eradication&Recovery]:** Completely removing the rootcause of incident and restoring affected systems back
* **Post-Incident activity:** Reviewing what happened to improve our defenses for next time
* **Coordination:** Keeping everyone informed and working together smoothly.

# 🛡️ My Cybersecurity Learning Journey & Portfolio

Hi there! 👋 I am a student who recently completed my 12th standard, and I am building my foundations in computer networks and defensive security. I am documenting my progress here as I work through the **Google Cybersecurity Professional Certificate**.

---

## 🎓 Completed Courses & Concepts

### 🔹 Course 2: Play It Safe: Manage Security Risks 
Learned how organizations identify, manage, and mitigate security risks using modern defensive tools:
*   **SIEM Tools (Security Information and Event Management):** Understanding how to collect and analyze centralized log data to find security threats.
*   **SOAR Tools (Security Orchestration, Automation, and Response):** Understanding how to automate playbook responses to handle security incidents faster.

---

## 📖 Current Learning (Course 3)

### 🔸 Course 3: Connect & Protect: Network and Network Security
I am diving deep into network architecture, foundational protocols, and traffic analysis:
*   **Network Infrastructure:** Learning about networking tools, cloud networks, cloud computing, and software-defined networks (SDN).
*   **Protocols & Segmentation:** Currently moving into lessons covering wireless security, firewalls, VPNs, Security Zones, and **Subnetting/CIDR**.

---

## ✍️ My Technical Study Notes & Insights

### ⚡ Network Speed & Traffic Monitoring
*   **Speed & Bandwidth:** Speed refers to the rate at which data packets are received or downloaded. Security professionals track network bandwidth and speed because irregular patterns or sudden drops can indicate a network attack.
*   **Packet Sniffing:** The practice of capturing and inspecting data packets as they travel across a network.

### 🏎️ Transport Protocols: TCP vs. UDP
*   **TCP (Transmission Control Protocol):** A connection-oriented protocol that allows two devices to form a reliable connection and stream data. It includes a specific set of instructions to organize data and ensures packets reach their appropriate destination.
*   **UDP (User Datagram Protocol):** A connectionless protocol that does not establish a formal connection between devices before transmitting data, prioritizing speed over verification.

### 🗺️ Network Architectural Models
Data flows across networks through layered stacks:
*   **TCP/IP Model Layers:**
    *   *Application Layer:* Contains protocols like HTTPS, TLS, DNS.
    *   *Transport Layer:* Manages host communication using TCP or UDP.
    *   *Internet Layer:* Manages routing using IPv4 or IPv6.
*   **The OSI Model (7 Layers):**
    *   *Layer 7: Application Layer* — Connects everyday user apps (browsers, email clients) directly to the network.
    *   *Layer 6: Presentation Layer* — Acts as the data translator; handles formatting, encryption, and compression.
    *   *Layer 5: Session Layer* — Opens, manages, and closes communication connections between devices.
    *   *Layer 4: Transport Layer* — Breaks data into smaller pieces, delivers them reliably, and ensures correct reassembly.
    *   *Layer 3: Network Layer* — Finds the best physical path for data across different networks using logical IP addresses.
    *   *Layer 2: Data Link Layer* — Handles the direct transfer of data between devices on the *same* local network using MAC addresses.
    *   *Layer 1: Physical Layer* — Transmits raw, unstructured binary data (0s and 1s) as electrical, optical, or radio signals over physical cables and hardware.

### 📦 IPv4 Packet Structure
*   **Packet Size:** Ranges from **20 to 60 bytes**. The first 20 bytes are fixed and contain routing data.
*   **The 13 Header Fields:** Security professionals analyze these exact fields during packet analysis:

# 💻 My Cybersecurity & Windows PowerShell Portfolio

Welcome to my portfolio! This space documents my hands-on technical journey in cybersecurity, system administration, and security automation. Here, I showcase the foundational mechanics I have mastered to navigate, audit, and secure Windows environments.

---

## 🚀 Core Technical Competencies: Windows PowerShell

While solving complex labs on platforms like **TryHackMe**, I deeply analyzed the core structure of Windows PowerShell. Below are the foundational concepts I have mastered and can confidently apply in active security operations:

### 1. The Verb-Noun Architecture
PowerShell relies on a strict, predictable naming convention: `Verb-Noun`. 
* **The Verb** dictates the precise action (e.g., `Get`, `Set`, `Stop`, `New`).
* **The Noun** represents the singular target system object (e.g., `Process`, `Service`, `Content`).
* *Why it matters:* This standardization allows a security analyst to accurately predict tool usage without relying heavily on external documentation.

### 2. Live Command Discovery & Auditing
In a real-world incident response or penetration testing scenario, a defender or attacker must discover what tools are available natively on a machine (Living off the Land). I utilize:
* **`Get-Command` with Wildcards (`*`):** To aggressively hunt for capabilities when only a keyword is known.
  * *Example:* Finding all native host-firewall configuration utilities:
    ```powershell
    Get-Command *Firewall*
    ```
* **`Get-Help`:** To parse internal documentation and extract actionable usage syntax via the `-Examples` flag.

### 3. Object-Oriented Pipeline Filtering
Unlike legacy command prompts (like CMD or Linux Bash) which manipulate raw text string streams, PowerShell manages actual structural **Objects**. This allows for sophisticated data carving:

* **Isolating Columns (`Select-Object`):** Used to trim down massive datasets and display *only* the specific properties needed for an audit trail.
  * *Example (Viewing only service health states):*
    ```powershell
    Get-Service | Select-Object -Property Status
    ```
* **Filtering Rows (`Where-Object`):** Used to isolate specific targets based on strict logical conditions (e.g., catching processes consuming abnormal memory or identifying unauthorized running services).

---

## 🏆 Hands-On Lab Experience
* **TryHackMe Platform Training:** Actively working through defensive and offensive rooms to practice live system enumeration, registry auditing, and permission mapping using native Windows tools.
* **Self-Directed Problem Solving:** Developed a strong troubleshooting mindset by shifting away from copy-pasting lab solutions to independently designing pipeline expressions using native help utilities.


    1. Version | 2. IP Header Length (IHL) | 3. Type of Service (ToS) | 4. Total Length | 5. Identification | 6. Flags | 7. Fragmentation Offset | 8. Time to Live (TTL) | 9. Protocol | 10. Header Checksum | 11. Source IP Address | 12. Destination IP Address | 13. Options

---


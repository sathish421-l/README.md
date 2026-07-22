# Cybersecurity Portfolio

Cybersecurity & Blockchain student building foundations in defensive security, systems administration, and secure network architecture. Below are project write-ups from hands-on labs and coursework — not a running log, just the finished work.

---

## 1. Corporate Security Controls Alignment Framework
*Based on CompTIA Security+ (SY0-701) — Domain 1: General Security Concepts*

A reference architecture mapping how security controls are categorized and how they function within an enterprise environment.

### Control Categories (How Controls Are Implemented)

| Category | Definition | Implementation Examples |
| :--- | :--- | :--- |
| **Technical (Logical)** | Defenses configured within hardware, software, or firmware. | Next-Gen Firewalls, AES-256 encryption at rest, Intrusion Prevention Systems |
| **Managerial** | Strategic oversight and policy set by leadership to guide risk mitigation. | Information Security Policies, Business Impact Analysis, Vendor Risk Assessments |
| **Operational** | Day-to-day procedures executed by personnel to maintain security baselines. | Security awareness training, scheduled backups, continuous log reviews |
| **Physical** | Tangible barriers protecting facilities, hardware, and personnel. | Biometric mantraps, CCTV, security guards |

### Functional Control Types (What Controls Achieve)

- **Preventive** — blocks unauthorized activity before it occurs (e.g. a firewall ACL)
- **Deterrent** — discourages an attacker psychologically (e.g. visible monitoring signage)
- **Corrective** — repairs and restores after an incident (e.g. restoring from backup)
- **Compensating** — a temporary safeguard when the primary control isn't feasible (e.g. isolating a legacy server in its own VLAN)
- **Directive** — mandates specific behavior through policy (e.g. a mandatory MFA policy)

### Scenario Matrix

| Functional Type | Technical | Managerial | Operational | Physical |
| :--- | :--- | :--- | :--- | :--- |
| **Preventive** | Firewall blocking ports | Signing an NDA | Offboarding checklist | Deadbolt lock |
| **Deterrent** | Login banner warnings | Threat of termination | Security audits | Warning signs |
| **Corrective** | Antivirus quarantining files | Incident response plan | Restoring backups | Repairing a broken fence |
| **Compensating** | Custom application firewall | Budget exceptions | Extra manual audits | Temporary security guard |
| **Directive** | System-enforced passwords | Acceptable use policy | Employee onboarding | ID badge policy |

**Takeaway:** A secure architecture never relies on one control category alone — technical protections need managerial oversight and physical barriers backing them up. Cryptographic controls (hashing, encryption) protect integrity and confidentiality, but only work in tandem with operational processes like key lifecycle management.

---

## 2. PowerShell: Verb-Noun Architecture & Object Pipeline Filtering

Core PowerShell concepts applied while working through Windows-focused labs on TryHackMe.

### The Verb-Noun Convention
PowerShell commands follow a strict `Verb-Noun` structure — the verb defines the action (`Get`, `Set`, `Stop`, `New`), the noun defines the target object (`Process`, `Service`, `Content`). This predictability means a security analyst can often guess the right command without external documentation.

### Live Command Discovery
For incident response or enumeration, discovering what's natively available on a machine matters (living-off-the-land techniques):

```powershell
# Hunt for all native firewall-related commands
Get-Command *Firewall*
```

`Get-Help -Examples` is used to pull actionable usage syntax directly from built-in documentation.

### Object-Oriented Pipeline Filtering
Unlike CMD or Bash, which pass raw text, PowerShell pipes structured objects — enabling precise data extraction:

```powershell
# Isolate just the status column across all services
Get-Service | Select-Object -Property Status
```

`Where-Object` filters rows by logical condition — useful for isolating abnormal processes or unauthorized running services during an audit.

---

## 3. Active Directory Basics — Reference Write-up
*TryHackMe — Active Directory rooms*

### Windows Domains & Architecture
- **Domain Controllers (DC):** central authority managing authentication and security requests.
- **Trees, Forests & Trusts:** how multi-domain environments establish trust boundaries and cross-domain resource access.

### Active Directory Infrastructure
- **Objects & OUs:** Users, Groups, and Computers organized inside Organizational Units.
- **NTDS.dit:** where AD stores directory data, cryptographic hashes, and group memberships.

### Identity & Access Management
- **Account lifecycle:** provisioning, management, and de-provisioning of users/computers within a domain.
- **Authentication protocols:** Kerberos (tickets, TGT, TGS) and NTLM, and how each authenticates users.

### Enterprise Administration & Security
- **Group Policy Objects (GPOs):** enforce security baselines, software deployment, and registry settings across endpoints.
- **Privileged access tiers:** the distinction between Domain Admins, Enterprise Admins, and standard users.

---

## 4. Linux Shell & Scripting Fundamentals

Hands-on bash scripting practice covering shell architecture, automation, and permissions.

### Skills Covered
- Structural differences between user interfaces, system shells, and the Linux kernel
- Shell environments across distributions (Bash, Zsh, Dash)
- Automation with variables, loops, positional arguments, and conditionals
- File permission management with `chmod`

### Scripts

**Interactive input handling** (`first_script.sh`):
```bash
#!/bin/bash
echo "Hey, what's your name?"
read name
echo "Welcome, $name"
```

**Numerical iteration** (`loop_script.sh`):
```bash
#!/bin/bash
for i in {1..10}
do
    echo "This is loop number $i"
done
```

**Conditional logic** (`conditional_script.sh`): simulates a credential validation flow using `if/else` branching on parsed string input.

> *Link your GitHub repo or gist with the full scripts here.*

---

## 5. Incident Response Playbook
*Based on Google Cybersecurity Certificate — Course 2*

A condensed reference for how organizations respond to a security incident, phase by phase:

1. **Preparation** — building the tools, training, and resources needed before an incident happens.
2. **Detection & Analysis** — monitoring alerts and logs via SIEM tooling to identify a genuine threat.
3. **Containment** — isolating the threat immediately to stop it from spreading further.
4. **Eradication & Recovery** — removing the root cause completely and restoring affected systems.
5. **Post-Incident Activity** — reviewing what happened to strengthen defenses going forward.
6. **Coordination** — keeping stakeholders informed and response efforts synchronized throughout.

**Applied context:** SIEM tools (Splunk, Chronicle) support the Detection & Analysis phase by centralizing log data; SOAR tools support Containment and Eradication by automating playbook-driven responses.

---

## In Progress
- Active Directory (TryHackMe) — Module 4 next
- Hack the Box Academy — Web Requests module
- Google Cybersecurity Certificate — Course 3: Connect & Protect (Network Security)

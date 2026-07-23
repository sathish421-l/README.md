# Cybersecurity Portfolio

Cybersecurity & Blockchain student. Project write-ups from hands-on labs and coursework, updated weekly.

---

## 1. Security Controls Framework
*Based on CompTIA Security+ (SY0-701)*

**What it is:** A reference mapping how security controls are categorized and what each type is meant to achieve.

**Control categories** (how a control is implemented):
- **Technical** — firewalls, encryption, IPS
- **Managerial** — policies, risk assessments
- **Operational** — training, backups, log reviews
- **Physical** — cameras, locks, security guards

**Control types** (what a control achieves):
- **Preventive** — stops an incident before it happens (e.g. a firewall rule)
- **Deterrent** — discourages an attempt (e.g. warning signage)
- **Corrective** — fixes things after an incident (e.g. restoring from backup)
- **Compensating** — a stand-in when the ideal control isn't possible (e.g. isolating a legacy server)
- **Directive** — a policy that mandates behavior (e.g. mandatory MFA)

**Takeaway:** No single control category is enough on its own — real security combines technical, managerial, operational, and physical layers together.

---

## 2. PowerShell Basics for Security

**What it is:** Core PowerShell skills for auditing and enumerating a Windows system.

- Commands follow a `Verb-Noun` pattern (`Get-Process`, `Stop-Service`) — predictable and easy to guess.
- `Get-Command *Firewall*` finds all commands related to a keyword.
- `Get-Help -Examples` shows real usage syntax for any command.
- PowerShell pipes actual objects, not text — so you can filter cleanly:

```powershell
Get-Service | Select-Object -Property Status
Get-Process | Where-Object { $_.CPU -gt 50 }
```

**Takeaway:** The same commands used for legitimate system audits are what an attacker uses to explore a system after gaining access — knowing them matters on both sides.

---

## 3. Active Directory Basics
*TryHackMe — Active Directory rooms*

**What it is:** Core concepts behind how most enterprise networks manage identity and access.

- **Domain Controller (DC):** the central server that handles authentication.
- **Trees, Forests, Trusts:** how multiple domains connect and share access.
- **Organizational Units (OUs):** how users, groups, and computers are organized inside a domain.
- **Kerberos & NTLM:** the two main protocols used to authenticate users.
- **Group Policy Objects (GPOs):** how admins push security settings across every machine in the domain.

**Takeaway:** AD's biggest risk isn't one flaw — it's how access quietly builds up across domains and groups if nobody audits it regularly.

---

## 4. Linux Shell Scripting

**What it is:** Basic bash scripting for automating simple tasks.

```bash
# Interactive input
echo "What's your name?"
read name
echo "Welcome, $name"
```

```bash
# Loop
for i in {1..10}
do
    echo "This is loop number $i"
done
```

Also covered: file permissions with `chmod`, conditional logic (`if/else`), and the difference between shells (Bash, Zsh, Dash).

> 🔗 *[Add your GitHub link with the full scripts here]*

**Takeaway:** These basics — loops, conditionals, input parsing — are the same building blocks used in real enumeration and exploitation scripts.

---

## 5. Incident Response Playbook
*Based on Google Cybersecurity Certificate*

The 6 phases of responding to a security incident:

1. **Preparation** — have the right tools and training ready beforehand
2. **Detection & Analysis** — spot the threat using logs and SIEM tools
3. **Containment** — isolate it so it can't spread
4. **Eradication & Recovery** — remove the cause, restore systems
5. **Post-Incident Review** — learn from it to prevent a repeat
6. **Coordination** — keep everyone informed throughout

**Takeaway:** Weak preparation is usually why real incidents take longer to contain than they should.

---

## 6. Networking & Protocol Reference

**What it is:** A quick-lookup guide for network layers, common protocols, and packet-level commands.

**OSI vs TCP/IP layers:**

| Layer | OSI | TCP/IP | Examples |
| :--- | :--- | :--- | :--- |
| 7 | Application | Application | HTTP, FTP, SMTP, SSH |
| 4 | Transport | Transport | TCP, UDP |
| 3 | Network | Internet | IP, ICMP |
| 2 | Data Link | Link | Ethernet, Wi-Fi |
| 1 | Physical | Link | Cables, radio signals |

**Common protocols and ports:**

| Protocol | Port | Use |
| :--- | :--- | :--- |
| FTP | 21 | File transfer |
| SMTP | 25 | Sending mail |
| DNS | 53 | Resolving domain names to IPs |
| HTTP | 80 | Unencrypted web traffic |
| POP3 | 110 | Downloading mail locally |
| IMAP | 143 | Syncing mail across devices |
| HTTPS | 443 | Encrypted web traffic |

**Useful commands:**
- `ping <target>` — check if a host is up
- `traceroute <target>` — map the path to a host
- `nslookup <domain>` — resolve a domain to an IP
- `tshark -r file.pcapng -Nn` — read a saved packet capture

**DHCP (DORA) — how a device gets an IP automatically:**
1. **Discover** — client asks for an IP
2. **Offer** — server proposes one
3. **Request** — client accepts
4. **Acknowledge** — server confirms

**Takeaway:** This one is reference material, not original analysis — good to have, but pair it with entries like #1 and #3 that show applied thinking, not just recall.

---

## In Progress
- Active Directory (TryHackMe) — Module 4
- Hack The Box Academy — Web Requests module
- Google Cybersecurity Certificate — Course 3
- Cybersecurity 101 (TryHackMe) — next up

---

## How This Portfolio Is Maintained

Daily learning (rooms, scripts, notes) stays in a private log. Once a week, the best entry from that log gets rewritten here using the template below.

**Entry template:**
```
## [Project Name]
Source: [platform/course]

What it is: one line on what this covers or solves.

[Key points, code, or tables]

Takeaway: why it matters or what it connects to.
```

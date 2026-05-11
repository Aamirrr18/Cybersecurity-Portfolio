# 🛡️ Cybersecurity & VAPT Portfolio
**Mohammad Aamir Siddique** | Aspiring Security Analyst & Threat Hunter

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](Https://www.linkedin.com/in/mohammad-aamir-siddique-b990ab3b5)

## 👤 About Me
I completed my Bachelor of Technology in Mechanical Engineering in 2024, which gave me a strong foundation in analytical problem-solving and systems thinking. I have since pivoted to pursue my passion for digital defense, recently completing the **Advanced Executive Program in Cybersecurity at IIIT Bangalore**. 

I am highly passionate about system defense, threat hunting, and infrastructure auditing. Below is a complete log of my hands-on academic projects demonstrating my practical experience in Vulnerability Assessment, Penetration Testing (VAPT), Digital Forensics, and Enterprise Network Defense.

---

## 🛠️ Core Competencies
* **Methods:** VAPT, Incident Remediation, Threat Auditing & Logging, Malware Behavior Analysis, IAM & RBAC, Digital Forensics.
* **Tools:** Kali Linux, Metasploit, OpenVAS, Nikto, Wireshark, Nmap, DVWA, Rsyslog, TCPView, Foremost, PowerShell.
* **Security Frameworks:** OWASP Top 10, Zero Trust Architecture, CompTIA Security+ (SY0-701) Principles.

---

## 📂 Complete Project Log (11-Part Cybersecurity Sprint)

### 1. Vulnerability Exploitation & Remediation (MS17-010 Capstone)
**Objective:** Simulate a real-world penetration test by identifying, exploiting, and remediating a critical vulnerability on a Windows 10 target.
* **Execution:** Conducted network reconnaissance using `Nmap` to identify exposed SMB ports. Exploited the MS17-010 (EternalBlue) vulnerability using the **Metasploit Framework** and a custom reverse TCP payload.
* **Evasion:** Bypassed modern host-based firewalls and Windows Defender by utilizing PowerShell to establish an exclusion directory.
* **Outcome:** Captured a Meterpreter session to extract local NTLM hashes. Authored a remediation report requiring immediate patching and the deactivation of the SMBv1 protocol.

### 2. Enterprise Infrastructure Auditing & Access Control (Linux)
**Objective:** Build a highly secure, monitored file storage system for a corporate finance team to mitigate insider risks.
* **Execution:** Secured the directory using granular **Linux Access Control Lists (ACLs)**, overriding standard group permissions to enforce strict Role-Based Access Control (RBAC). 
* **Monitoring:** Configured the `Rsyslog` daemon to trap unauthorized access attempts.
* **Outcome:** Routed localized terminal errors into a custom PHP web dashboard, providing the IT Security team with a real-time stream of security alerts.

### 3. Malware Analysis & Cyber Intrusion Defense
**Objective:** Simulate an end-to-end cyber intrusion to demonstrate how attackers bypass perimeter defenses, and how defenders track malicious traffic.
* **Execution:** Established a secure Command and Control (C2) tunnel utilizing **Ngrok** and a spoofed reverse TCP executable to bypass inbound corporate firewalls.
* **Analysis:** Pivoted to defense, utilizing live endpoint monitoring tools like **TCPView**. 
* **Outcome:** Traced the active outbound connection from the payload to the remote attacker infrastructure, proving the critical importance of endpoint monitoring and strict egress filtering.

### 4. Digital Forensics & Steganography
**Objective:** Recover highly sensitive financial data intentionally hidden and "permanently" deleted by a malicious insider.
* **Execution:** Investigated a corrupted hard drive where standard automated forensic tools failed due to file system destruction.
* **Recovery:** Executed manual "raw disk carving" utilizing the Linux `grep` utility on the unallocated space (`/dev/sda`).
* **Outcome:** Successfully bypassed the broken file system and extracted the hidden steganographic text straight from the raw binary sectors.

### 5. Windows Security Logon Monitoring & Automation
**Objective:** Configure a Windows Server to detect brute-force password attacks and automate incident response reporting.
* **Execution:** Enabled advanced system tracking via the Windows Local Security Policy manager, enforcing strict Audit Logon event rules to capture Event ID 4625.
* **Automation:** Engineered a **PowerShell** script (`Get-WinEvent`) to filter through thousands of raw logs.
* **Outcome:** Automatically extracted targeted threat data and generated a clean, readable HTML security report, significantly reducing alert fatigue for analysts.

### 6. Securing Linux Servers (SSH Hardening & Honeypots)
**Objective:** Deploy a proactive defense strategy to protect a public-facing Linux server from automated hacking bots.
* **Execution:** Hardened remote access via the SSH configuration file, altering default ports and applying strict `MaxAuthTries` limitations.
* **Defense:** Deployed a decoy system utilizing the `vsftpd` service to open an attractive, monitored FTP port.
* **Outcome:** Created a functional "Honeypot" that successfully diverted automated network scanners away from actual production services, allowing for early threat detection.

### 7. Active Directory & Group Policy Management
**Objective:** Centralize network security by building a Windows Domain Controller to enforce corporate security policies network-wide.
* **Execution:** Provisioned a Windows Server 2022 environment, structuring logical Organizational Units (OUs) for secure user authentication.
* **Enforcement:** Engineered a global **Group Policy Object (GPO)** targeting endpoint defense.
* **Outcome:** Executed a forced policy update that permanently locked the Windows Defender Firewall to an active state across all employee workstations, preventing localized user tampering.

### 8. E-Commerce Web Application Security Assessment (SQLi & XSS)
**Objective:** Conduct a security review of a vulnerable e-commerce platform to uncover sensitive data exposure risks.
* **Execution:** Identified and exploited critical OWASP Top 10 vulnerabilities, successfully utilizing `' OR '1'='1` payloads to bypass authentication.
* **Outcome:** Demonstrated the severe risk of **SQL Injection** and **Cross-Site Scripting (XSS)**. Authored mitigation strategies requiring the development team to utilize Parameterized Queries and HTML output encoding.

### 9. Web Directory Enumeration & Traffic Interception
**Objective:** Perform reconnaissance on a target web server to map its infrastructure and analyze application traffic.
* **Execution:** Utilized the `Dirb` utility to launch brute-force dictionary attacks against the target server.
* **Outcome:** Successfully uncovered hidden administrative directories (`/phpMyAdmin/` and `/dvwa/`) and intercepted raw HTTP request headers utilizing **Burp Suite** to map potential entry points.

### 10. OS Command Injection Penetration Testing
**Objective:** Exploit input validation flaws within a Linux-based web application to achieve remote code execution.
* **Execution:** Targeted the DVWA command execution module, injecting system-level commands using the `;` operator (e.g., `127.0.0.1 ; whoami`).
* **Outcome:** Bypassed web application controls to execute unauthorized commands directly on the host operating system, proving the necessity of strict Input Allowlists.

### 11. Blind OS Command Injection & Mitigation
**Objective:** Demonstrate advanced injection techniques against targets that suppress error messages and visual text output.
* **Execution:** Deployed secondary and timing-based payloads (e.g., `127.0.0.1 ; sleep 10` and `127.0.0.1 && touch hacked.txt`).
* **Outcome:** Proved remote execution capabilities without visual confirmation by forcing the server to alter its behavioral timing and silently create internal files. 

---
*Note: Full technical project reports (PDFs) detailing the execution steps, payload configurations, and remediation strategies are available within this repository.*

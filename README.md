
**AWS Wazuh SOC Lab**

** Project Overview**

This project demonstrates the implementation of a cloud-based Security Operations Center (SOC) lab using AWS and Wazuh SIEM. The environment was designed to simulate real-world security monitoring, attack detection, and incident analysis workflows used by SOC analysts and cybersecurity teams.

**The lab consists of:**
- Wazuh SOC Server
- Ubuntu Victim Machine
- Kali Linux Attacker Machine

**The project focuses on detecting:**
- SSH brute-force attacks
- Authentication failures
- Suspicious login activity
- File integrity changes
- Privilege escalation activity

---

 **Technologies Used**

- AWS EC2
- AWS VPC
- AWS Security Groups
- Wazuh SIEM
- Ubuntu Server
- Kali Linux
- Hydra
- Nmap
- Linux
- SSH
- MITRE ATT&CK Framework

---

 **Lab Architecture**

Kali Linux Attacker → Ubuntu Victim Server → Wazuh SOC Server

- Kali Linux was used to simulate attacks.
- Ubuntu Server acted as the monitored endpoint.
- Wazuh SIEM collected logs, generated alerts, and visualized security events.

---

 **AWS Infrastructure Setup**

The environment was deployed inside a custom AWS VPC using EC2 instances and security groups.

 **Wazuh SOC Server**
Configured with:
- SSH access
- HTTPS dashboard access
- Wazuh agent communication ports
- API access

 **Ubuntu Victim Server**
Configured as:
- Monitored endpoint
- SSH target for attack simulation
- Wazuh agent endpoint

 **Kali Linux Attacker**
Configured for:
- SSH brute-force simulation
- Network reconnaissance
- Security testing

---

# Security Monitoring Implemented

## 1. SSH Brute-Force Detection

Hydra was used from the Kali Linux machine to simulate SSH password attacks against the Ubuntu victim server.

Wazuh successfully detected:
- SSH authentication failures
- Multiple failed login attempts
- Successful authentication after repeated failures
- PAM authentication alerts

 **MITRE ATT&CK Techniques**
- T1110 — Brute Force
- T1021.004 — SSH

---

** 2. Network Reconnaissance**

Nmap scans were performed against the Ubuntu victim server to simulate reconnaissance activity.
Example:
nmap -sS -Pn <victim-ip>

**3. File Integrity Monitoring (FIM)**

Suspicious files were created, modified, permission-changed, and deleted on the Ubuntu victim machine.

Example:

touch malware.sh
echo "malicious test" > malware.sh
chmod +x malware.sh
rm malware.sh

**Wazuh successfully detected:**

File creation
File deletion
Integrity checksum changes
Key Detections Generated
SSH authentication failures
PAM login failures
Multiple failed logins
Successful login after repeated failures
File added alerts
File deleted alerts
Integrity checksum changed alerts
Successful sudo to ROOT activity
Key Skills Demonstrated
AWS cloud deployment
VPC and Security Group configuration
Wazuh SIEM deployment
Linux administration
Threat detection and monitoring
Brute-force attack simulation
File Integrity Monitoring
MITRE ATT&CK mapping
Security event analysis
SOC operations workflow
Screenshots

**The screenshots directory contains:**

AWS EC2 deployment
Security group configuration
Wazuh dashboard
SSH brute-force alerts
File Integrity Monitoring alerts
Hydra attack simulation
Wazuh agent installation
Nmap reconnaissance activity
Future Improvements

**Potential future enhancements:**

Suricata IDS integration
Automated incident response
Threat intelligence feeds
Multi-endpoint monitoring
Custom Wazuh rules
Active response blocking

**Author:**
Sachin Kumar
Master of Cyber Security
Deakin University


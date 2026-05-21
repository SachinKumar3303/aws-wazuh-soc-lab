# AWS-Based SOC Lab Using Wazuh

## Project Overview
This project demonstrates a cloud-based Security Operations Center lab built in AWS using Wazuh SIEM. The lab includes a Wazuh manager, Ubuntu victim endpoint, and Kali Linux attacker machine.

## Architecture
Kali Attacker → Ubuntu Victim → Wazuh SOC Server

## Tools Used
- AWS EC2
- AWS VPC
- Security Groups
- Wazuh SIEM
- Ubuntu Server
- Kali Linux
- Hydra
- Nmap
- SSH
- Linux audit/auth logs

## Project Steps
1. Created AWS VPC and security groups
2. Deployed Wazuh SOC server
3. Installed Wazuh agent on Ubuntu victim
4. Created Kali attacker machine
5. Simulated SSH brute-force attack
6. Enabled File Integrity Monitoring
7. Analysed alerts in Wazuh dashboard

## Detections Generated
- SSH authentication failures
- PAM login failures
- Multiple failed logins
- Successful login after failures
- File added
- File deleted
- Integrity checksum changed
- Sudo to root activity

## MITRE ATT&CK Mapping
- T1110 Brute Force
- T1021.004 SSH
- Credential Access
- Lateral Movement

## Key Learning Outcomes
- Built a cloud SOC environment
- Configured Wazuh SIEM
- Monitored Linux endpoint logs
- Simulated attacks using Kali
- Analysed security alerts and rule IDs
- Understood AWS network security controls


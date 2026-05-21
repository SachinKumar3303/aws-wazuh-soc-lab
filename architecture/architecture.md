                           AWS CLOUD ENVIRONMENT
┌──────────────────────────────────────────────────────────────────────┐
│                                                                      │
│                         SOC-Lab-VPC (10.0.0.0/16)                    │
│                                                                      │
│  ┌───────────────────┐                                               │
│  │   Kali Linux      │                                               │
│  │   Attacker        │                                               │
│  │-------------------│                                               │
│  │ Public IP         │                                               │
│  │ Private IP        │                                               │
│  │ Hydra             │                                               │
│  │ Nmap              │                                               │
│  └─────────┬─────────┘                                               │
│            │                                                         │
│            │ SSH Brute Force / Reconnaissance                        │
│            ▼                                                         │
│  ┌───────────────────┐                                               │
│  │ Ubuntu Victim     │                                               │
│  │ Monitored Endpoint│                                               │
│  │-------------------│                                               │
│  │ Wazuh Agent       │                                               │
│  │ SSH Service       │                                               │
│  │ Authentication    │                                               │
│  │ Logs              │                                               │
│  │ File Monitoring   │                                               │
│  └─────────┬─────────┘                                               │
│            │                                                         │
│            │ Wazuh Agent Logs                                        │
│            │ Port 1514 / 1515                                        │
│            ▼                                                         │
│  ┌───────────────────┐                                               │
│  │ Wazuh SOC Server  │                                               │
│  │-------------------│                                               │
│  │ Wazuh Manager     │                                               │
│  │ Wazuh Dashboard   │                                               │
│  │ Wazuh Indexer     │                                               │
│  │ Filebeat          │                                               │
│  │ MITRE ATT&CK      │                                               │
│  │ Alert Analysis    │                                               │
│  └─────────┬─────────┘                                               │
│            │                                                         │
│            │ HTTPS (443)                                             │
│            ▼                                                         │
│  ┌───────────────────┐                                               │
│  │ Analyst / Admin   │                                               │
│  │ Windows Laptop    │                                               │
│  │-------------------│                                               │
│  │ Browser Access    │                                               │
│  │ PowerShell SSH    │                                               │
│  └───────────────────┘                                               │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘

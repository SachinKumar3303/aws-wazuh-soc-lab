# SSH Brute Force Incident Analysis

## Summary
A simulated SSH brute-force attack was launched from the Kali Linux attacker machine against the Ubuntu victim server using Hydra.

## Detection
Wazuh successfully detected:
- SSH authentication failures
- Multiple failed login attempts
- PAM authentication failures
- Authentication failures followed by successful login

## MITRE ATT&CK Mapping
- T1110 — Brute Force
- T1021.004 — SSH

## Security Impact
The activity demonstrated how SIEM solutions can detect credential attacks and suspicious authentication behavior.

## Recommended Mitigations
- Enable multi-factor authentication
- Restrict SSH access
- Use strong passwords
- Configure account lockout policies
- Monitor repeated authentication failures

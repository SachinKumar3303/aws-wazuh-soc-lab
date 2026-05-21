# Commands Used

## SSH Login
```bash
ssh ubuntu@<victim-ip>
```

## Wazuh Agent Installation
```bash
curl -so wazuh-agent.sh https://packages.wazuh.com/4.x/ubuntu/wazuh-install.sh && sudo bash ./wazuh-agent.sh -a 10.0.4.130
```

## Nmap Reconnaissance
```bash
nmap -sS -Pn <victim-ip>
```

## Hydra SSH Brute Force
```bash
hydra -l ubuntu -P passwords.txt ssh://<victim-ip> -t 4 -V
```

## File Integrity Monitoring Test
```bash
touch malware.sh
echo "malicious test" > malware.sh
chmod +x malware.sh
rm malware.sh
```

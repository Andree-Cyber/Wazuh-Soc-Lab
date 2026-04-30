# Windows Failed Login Detection

## Purpose
Detect failed Windows logon attempts from the Windows 10 endpoint.

## Wazuh Query
- data.win.system.eventID:4625

# Agent-Specific Query
- agent.name: "windows11-endpoint" AND data.win.system.eventID:4625

# What is the Event Meaning?
- A Windows Event ID 4625 indicates that an account failed to log on.

# MITRE ATT&CK Mapping
- T1110 - Brute Force
- ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/4096c8d5876a00dbaff81ebb64464444c138cc06/Detections/MITRE%20ATT%26CK%20-%20T1110%20-%20Brute%20Force.png) |

| Evidence | Result |
|---|---|
|windows-failed-login-events| ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/5e4cc4586a209da5d68e9b3dc28b999c71c33079/Detections/windows10-failed%20login-events.png)
|windows-failed-login-alert details| 



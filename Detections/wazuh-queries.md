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
| T1110 - | Brute Force |
| ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/4096c8d5876a00dbaff81ebb64464444c138cc06/Detections/MITRE%20ATT%26CK%20-%20T1110%20-%20Brute%20Force.png) |

# Windows Failed Login Detection

## Purpose
Detect failed Windows logon attempts from the Windows 10 endpoint.

## Wazuh Query
- data.win.system.eventID:4625

# Agent-Specific Query
- agent.name: "windows11-endpoint" AND data.win.system.eventID:4625

# What is the Event Meaning?
- A Windows Event ID 4625 indicates that an account failed to log on.

# MITRE Att&CK Mapping
- T1110 - Brute Force
- ![image alt]()

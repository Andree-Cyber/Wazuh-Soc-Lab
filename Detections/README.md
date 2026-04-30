## Detections

The `detections/` folder contains Wazuh search queries, rule IDs, and detection notes used during the lab. These detections were used to investigate authentication activity, file integrity changes, suspicious commands, malware test alerts, and endpoint security events.

| Detection Use Case | Data Source | Wazuh Query / Rule | MITRE ATT&CK |
|---|---|---|---|
| Windows failed logins | Windows Security Logs | `data.win.system.eventID:4625` | T1110 - Brute Force |
| Windows local user creation | Windows Security Logs | `data.win.system.eventID:4720` | T1136.001 - Local Account |
| Linux SSH brute-force attempts | Linux auth logs | `rule.id:(5551 OR 5712)` | T1110 - Brute Force |
| File integrity monitoring | Wazuh FIM / Syscheck | `rule.id: is one of 550,553,554` | T1565 - Data Manipulation |
| Suspicious PowerShell activity | Windows PowerShell Logs | `powershell AND (EncodedCommand OR ExecutionPolicy)` | T1059.001 - PowerShell |
| EICAR malware test file | Windows Defender Logs | `EICAR OR Windows Defender` | T1204 - User Execution |

### Detection Documentation

Detailed detection notes are stored in:

- `detections/wazuh-queries.md`
- `detections/detection-notes.md`

Each detection includes the search query, purpose, related data source, expected alert behavior, and MITRE ATT&CK mapping.

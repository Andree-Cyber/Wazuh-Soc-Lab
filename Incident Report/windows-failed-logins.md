# Incident Report: Windows Failed Login Attempts

## 1. Summary

Multiple failed login attempts were generated on the Windows 11 endpoint as part of a controlled SOC lab simulation. Wazuh detected the failed Windows logon events and displayed them in the Threat Hunting dashboard.

This activity was reviewed to practice authentication log analysis, identify failed logon patterns, document indicators, and map the behavior to MITRE ATT&CK.

---

## 2. Environment

| Field | Value |
|---|---|
| SIEM | Wazuh |
| Wazuh Server | Ubuntu laptop |
| Endpoint | Windows 11 VM |
| Endpoint Role | Monitored Windows endpoint |
| Agent Name | windows11-endpoint |
| Event Type | Failed Windows logon |
| Windows Event ID | 4625 |
| Test Type | Safe lab simulation |

---

## 3. Detection Query

The following Wazuh query was used to find failed Windows login events:

```text
data.win.system.eventID:4625

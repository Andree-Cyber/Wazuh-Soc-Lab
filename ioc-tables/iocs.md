# IOC Table

This file documents indicators observed during the Wazuh SOC lab. These indicators were collected from Wazuh alerts, endpoint logs, and lab simulations.

---

## Windows Failed Login Attempts

| Incident | IOC Type | Value | Source | Confidence | Notes |
|---|---|---|---|---|---|
| Windows Failed Logins | Host | windows11-endpoint | Wazuh alert | High | Windows 11 endpoint where failed logins occurred |
| Windows Failed Logins | Event ID | 4625 | Windows Security Logs | High | Windows failed logon event |
| Windows Failed Logins | Username | Windows local user account | Wazuh alert | High | Account involved in failed login attempt |
| Windows Failed Logins | Source IP | Not available for local console login | Wazuh alert | Low | Local console login attempts may not show source IP |
| Windows Failed Logins | Source Workstation | Windows 11 VM | Wazuh alert | Medium | Workstation where login attempt occurred |
| Windows Failed Logins | Detection Query | `data.win.system.eventID:4625` | Wazuh Threat Hunting | High | Query used to identify failed login events |
| Windows Failed Logins | MITRE Technique | T1110 - Brute Force | MITRE ATT&CK Mapping | Medium | Multiple failed logins may indicate brute-force behavior |

---

## Notes

The failed login events were generated as part of a controlled lab simulation. The source IP may not appear for local console login attempts. In a real environment, repeated failed logins should be reviewed for source IP address, target username, logon type, failure reason, and whether a successful login occurred afterward.

---

## Related Evidence

| Evidence | Location |
|---|---|
| Detection query | `../detections/wazuh-queries.md` |
| Incident report | `../incident-reports/windows-failed-logins.md` |
| Failed login event screenshot | ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/9ee690da12c00ad13077df3c47628783a9b257cc/Screenshots/windows10-failed%20login-events.png) |
| Expanded alert screenshot | `../screenshots/15-windows-failed-login-alert-details.png` |

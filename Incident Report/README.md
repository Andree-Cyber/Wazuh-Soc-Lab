## Step 5: Windows Failed Login Detection

Failed login attempts were generated on the Windows 11 VM by entering incorrect passwords at the login screen. Wazuh collected the Windows authentication events and displayed failed logon activity in the Threat Hunting dashboard.

### Detection Details

| Field | Value |
|---|---|
| Endpoint | Windows 11 VM |
| Event Type | Failed logon |
| Windows Event ID | 4625 |
| Wazuh Search | `data.win.system.eventID:4625` |
| MITRE ATT&CK | T1110 - Brute Force |

### Evidence

| Evidence | Screenshot |
|---|---|
| Failed login events in Wazuh | `screenshots/14-windows-failed-login-events.png` |
| Expanded failed login alert | `screenshots/15-windows-failed-login-alert-details.png` |

### Finding Summary
Wazuh successfully detected failed Windows logon attempts from the Windows 11 endpoint. This confirmed that Windows authentication events were being collected and forwarded to the SIEM for investigation.

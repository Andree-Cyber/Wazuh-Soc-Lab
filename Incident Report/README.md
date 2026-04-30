## Step 5: Windows Failed Login Detection

Failed login attempts were generated on the Windows 10 VM by entering incorrect passwords at the login screen. Wazuh collected the Windows authentication events and displayed failed logon activity in the Threat Hunting dashboard.

### Detection Details

| Field | Value |
|---|---|
| Endpoint | Windows 10 VM |
| Event Type | Failed logon |
| Windows Event ID | 4625 |
| Wazuh Search | `data.win.system.eventID:4625` |
| MITRE ATT&CK | T1110 - Brute Force |

### Evidence

| Evidence | Screenshot |
|---|---|
| Failed login events in Wazuh | ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/38fc00da930443371272f709e5b9d57e985e9dfd/Detections/windows10-failed%20login-events.png) |
| Expanded failed login alert | ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/93ca099d0331b0451367a68c27d386a868d23434/Detections/windows10-failed-login-alert-details.png) |

### Finding Summary
Wazuh successfully detected failed Windows logon attempts from the Windows 10 endpoint. This confirmed that Windows authentication events were being collected and forwarded to the SIEM for investigation.

# Wazuh Detection Queries

This file contains the Wazuh queries and rule IDs used during the Mini SOC SIEM Lab.

## Windows Failed Logins

**Purpose:** Detect failed Windows logon attempts.

```text
data.win.system.eventID:4625

# Wazuh-Soc-Lab

## Lab Objective

The goal of this lab is to build a small SOC environment using Wazuh as the SIEM. The lab collects logs from Windows and Ubuntu endpoints, generates safe simulated security events, investigates alerts, documents IOCs, and maps findings to MITRE ATT&CK techniques.

## Lab Architecture

This lab uses a physical Ubuntu laptop as the Wazuh server and a separate PC running VirtualBox for the endpoint and attacker virtual machines.

| System | Role | Platform | Notes |
|---|---|---|---|
| Ubuntu Laptop | Wazuh Server | Physical laptop | Runs Wazuh manager, dashboard, and indexer |
| Windows 10 VM | Monitored Endpoint | VirtualBox on PC | Wazuh agent installed |
| Ubuntu Laptop | Monitored Endpoint | Physical Laptop | Wazuh agent installed |
| Kali Linux VM | Test Attacker Machine | VirtualBox on PC | Used only for safe simulations |

## Network Configuration

All systems are connected on the same local network. The Ubuntu laptop hosts the Wazuh server, while the Windows 11, Ubuntu, and Kali Linux VMs run on a separate PC using VirtualBox.

| System | Example IP Address | Connectivity Status |
|---|---|---|
| Wazuh Server | 10.0.0.X | Reachable |
| Windows 10 VM | 10.0.0.X | Can reach Wazuh server |
| Ubuntu Laptop | 10.0.0.X | Can reach Wazuh server |
| Kali Linux VM | 10.0.0.X| Can reach lab VMs |

## Connectivity Validation

Connectivity was tested from each VM to the Wazuh server.

| Test | Result |
|---|---|
| Windows 10 VM ping to Wazuh server | Successful |
| Ubuntu laptop ping to Wazuh server | Successful |
| Kali VM ping to Wazuh server | Successful |
| Wazuh dashboard reachable from PC browser | Successful |

## Step 1 Findings

The lab network was successfully configured. The Wazuh server is running on a physical Ubuntu laptop, while the Windows 10, and Kali Linux VMs are hosted on a separate PC using VirtualBox. All systems are able to communicate over the local network.

The Windows 10 VM and Ubuntu VM will be monitored endpoints with Wazuh agents installed. The Kali Linux VM will be used only to generate safe test activity against lab-owned systems. The Wazuh dashboard is reachable from the laptop, confirming that the SIEM server is accessible across the lab network.

(Step 1 continued) Windows 10 VM Ping to Wazuh server

Evidence: ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/928c19ac7bebe26fefae15298368d928dbbfe4f1/Screenshots/screenshots-01-windows-ping-wazuh.png)

(Step 1 continued) Ubuntu laptop Ping to Wazuh server

Evidence: ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/d11dd36a286a9b3d70cd64ee60df0a4ab140d41e/Screenshots/screenshot-02-ubuntu-ping-wazuh.png)

(Step 1 continued) Kali VM ping to Wazuh Server

Evidence: ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/6de67778ba53b99f06ceeb366627b3ff58822b0d/Screenshots/screenshot-03-kali-ping-wazuh.png)

(Step 1 continued) Wazuh Login/Dashboard Access:

The Wazuh login/dashboard was successfully accessed from the PC browser using the Ubuntu laptop’s local network IP address.

Evidence:

Login: ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/95a9a0312943dc55532df4e0fe93952abc7cb62a/Screenshots/screenshot-04-login-page.png)
Dashboard: ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/7880c6dcfabdc89709c7d8cc431d9aaee04d9c40/Screenshots/screenshot-05-Wazuh-dashboard-access.png)






## Step 3: Windows 11 Wazuh Agent Deployment

The Wazuh agent was installed on the Windows 10 virtual machine and configured to communicate with the Wazuh server running on the Ubuntu laptop.

### Windows Endpoint Details

| Field | Value |
|---|---|
| Endpoint | Windows 11 VM |
| Role | Monitored endpoint |
| Wazuh agent status | Active |
| Wazuh server | Ubuntu laptop |
| Network connection | Local network |

### Evidence

| Evidence | Screenshot |
|---|---|
| Windows agent active in Wazuh | ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/7ae3a7ba45187f96eac5e8dfe1011546405556cb/Screenshots/windows10-agent-active.png) |
| Windows agent details page | ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/b02a4098ee01f579cf4960e8ebd512fd339d1c66/Screenshots/windows-agent-details.png) |
| Windows events visible in Wazuh | ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/43b2714f3832027167781a0ecb5495f760004d2f/Screenshots/windows%2010-agent-events.png) |


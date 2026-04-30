# Wazuh-Soc-Lab

## Lab Objective

The goal of this lab is to build a small SOC environment using Wazuh as the SIEM. The lab collects logs from Windows and Ubuntu endpoints, generates safe simulated security events, investigates alerts, documents IOCs, and maps findings to MITRE ATT&CK techniques.

## Lab Architecture

This lab uses a physical Ubuntu laptop as the Wazuh server and a separate PC running VirtualBox for the endpoint and attacker virtual machines.

| System | Role | Platform | Notes |
|---|---|---|---|
| Ubuntu Laptop | Wazuh Server | Physical laptop | Runs Wazuh manager, dashboard, and indexer |
| Windows 11 VM | Monitored Endpoint | VirtualBox on PC | Wazuh agent installed |
| Ubuntu Laptop | Monitored Endpoint | Physical Laptop | Wazuh agent installed |
| Kali Linux VM | Test Attacker Machine | VirtualBox on PC | Used only for safe simulations |

## Network Configuration

All systems are connected on the same local network. The Ubuntu laptop hosts the Wazuh server, while the Windows 11, Ubuntu, and Kali Linux VMs run on a separate PC using VirtualBox.

| System | Example IP Address | Connectivity Status |
|---|---|---|
| Wazuh Server | 10.0.0.X | Reachable |
| Windows 11 VM | 10.0.0.X | Can reach Wazuh server |
| Ubuntu Laptop | 10.0.0.X | Can reach Wazuh server |
| Kali Linux VM | 10.0.0.X| Can reach lab VMs |

## Connectivity Validation

Connectivity was tested from each VM to the Wazuh server.

| Test | Result |
|---|---|
| Windows 11 VM ping to Wazuh server | Successful |
| Ubuntu laptop ping to Wazuh server | Successful |
| Kali VM ping to Wazuh server | Successful |
| Wazuh dashboard reachable from PC browser | Successful |

## Windows 11 VM Ping to Wazuh server

Evidence: ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/928c19ac7bebe26fefae15298368d928dbbfe4f1/Screenshots/screenshots-01-windows-ping-wazuh.png)

## Ubuntu laptop Ping to Wazuh server

Evidence: ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/d11dd36a286a9b3d70cd64ee60df0a4ab140d41e/Screenshots/screenshot-02-ubuntu-ping-wazuh.png)

## Kali VM ping to Wazuh Server

Evidence: ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/6de67778ba53b99f06ceeb366627b3ff58822b0d/Screenshots/screenshot-03-kali-ping-wazuh.png)

## Wazuh Login/Dashboard Access:

The Wazuh login/dashboard was successfully accessed from the PC browser using the Ubuntu laptop’s local network IP address.

Evidence:

Login: ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/95a9a0312943dc55532df4e0fe93952abc7cb62a/Screenshots/screenshot-04-login-page.png)
Dashboard: ![image alt](https://github.com/Andree-Cyber/Wazuh-Soc-Lab/blob/7880c6dcfabdc89709c7d8cc431d9aaee04d9c40/Screenshots/screenshot-05-Wazuh-dashboard-access.png)


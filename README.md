# Wazuh-Soc-Lab

## Lab Objective

The goal of this lab is to build a small SOC environment using Wazuh as the SIEM. The lab collects logs from Windows and Ubuntu endpoints, generates safe simulated security events, investigates alerts, documents IOCs, and maps findings to MITRE ATT&CK techniques.

## Lab Architecture

This lab uses a physical Ubuntu laptop as the Wazuh server and a separate PC running VirtualBox for the endpoint and attacker virtual machines.

| System | Role | Platform | Notes |
|---|---|---|---|
| Ubuntu Laptop | Wazuh Server | Physical laptop | Runs Wazuh manager, dashboard, and indexer |
| Windows 11 VM | Monitored Endpoint | VirtualBox on PC | Wazuh agent installed |
| Ubuntu VM | Monitored Endpoint | VirtualBox on PC | Wazuh agent installed |
| Kali Linux VM | Test Attacker Machine | VirtualBox on PC | Used only for safe simulations |

## Network Configuration

All systems are connected on the same local network. The Ubuntu laptop hosts the Wazuh server, while the Windows 11, Ubuntu, and Kali Linux VMs run on a separate PC using VirtualBox.

| System | Example IP Address | Connectivity Status |
|---|---|---|
| Wazuh Server | 10.0.0.X | Reachable |
| Windows 11 VM | 10.0.0.X | Can reach Wazuh server |
| Ubuntu VM | 10.0.0.X | Can reach Wazuh server |
| Kali Linux VM | 10.0.0.X| Can reach lab VMs |

## Connectivity Validation

Connectivity was tested from each VM to the Wazuh server.

| Test | Result |
|---|---|
| Windows 11 VM ping to Wazuh server | Successful | 
| Ubuntu VM ping to Wazuh server | Successful |
| Kali VM ping to Wazuh server | Successful |
| Wazuh dashboard reachable from PC browser | Successful |

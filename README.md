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

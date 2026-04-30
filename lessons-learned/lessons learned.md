# Lessons Learned

## What I Built

I built a Wazuh-based SOC lab using a physical Ubuntu laptop as the SIEM server and VirtualBox-hosted Windows 10 and Kali Linux virtual machines.

## What I Practiced

- Wazuh dashboard navigation
- Windows endpoint monitoring
- Windows Event ID investigation
- Failed login detection
- Alert triage
- IOC documentation
- Incident report writing
- MITRE ATT&CK mapping

## What Worked

The Windows 10 endpoint successfully connected to Wazuh and forwarded authentication events. Wazuh detected failed Windows logon activity using Event ID 4625.

## Challenges

Some screenshots and documentation needed to be organized carefully so the README, detection notes, incident reports, and IOC tables all referenced the same evidence.

## What I Would Improve

- Add an Ubuntu endpoint VM
- Add Sysmon to Windows 10
- Simulate SSH brute-force attempts
- Configure File Integrity Monitoring
- Test EICAR malware detection
- Create more incident reports

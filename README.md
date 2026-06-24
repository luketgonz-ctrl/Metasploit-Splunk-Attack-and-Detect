# Metasploit-Splunk-Attack-and-Detect
## Objective
This project aimed to establish a controlled home lab environment for simulating 
and detecting a real-world cyberattack. Using Kali Linux as the attacker and 
Windows 10 as the victim, a Meterpreter reverse shell payload was created, 
delivered, and executed. The primary focus was to ingest and analyze Windows 
Event Logs within Splunk SIEM, detect the malicious activity, and build a 
real-time detection alert. This hands-on experience deepened understanding of 
attack lifecycles, SIEM configuration, and defensive detection strategies.

### Skills Learned
- Hands-on understanding of SIEM concepts and practical Splunk implementation
- Proficiency in analyzing and interpreting Windows Event Logs (EventCode 4688)
- Ability to generate, deliver, and recognize malicious payloads and attack patterns
- Enhanced knowledge of Windows auditing policies and security configurations
- Configuration of the Splunk Universal Forwarder for log collection
- IOC documentation and forensic pivoting using Logon Session IDs
- Development of critical thinking and troubleshooting skills across 6 real issues
- Understanding of defense-in-depth through layered security controls

### Tools Used
- **Metasploit Framework & msfvenom** — payload creation and listener configuration
- **Kali Linux** — attacker machine
- **VMware Workstation** — home lab virtualization
- **Splunk Enterprise + Universal Forwarder** — SIEM log ingestion and analysis
- **Python 3 HTTP Server** — payload delivery
- **PowerShell** — Windows service management and audit policy configuration
- **Windows Event Log** — primary log source for attack detection

## Steps

*Ref 1: Creating the Meterpreter payload with msfvenom on Kali Linux*

*Ref 2: Troubleshooting — directory not found error and fix*

*Ref 3: Hosting bayload.exe via Python 3 HTTP server*

*Ref 4: Windows VM downloading payload from Kali HTTP server*

*Ref 5: SmartScreen warning bypassed — payload executed*

*Ref 6: Meterpreter session 1 opened — remote access established*

*Ref 7: Remote directory created on Windows VM from Kali*

*Ref 8: Splunk returning 0 events — logging misconfiguration identified*

*Ref 9: inputs.conf created and fixed to collect Windows Event Logs*

*Ref 10: PowerShell permission error and fix — reopened as Administrator*

*Ref 11: Process creation auditing enabled via auditpol and registry*

*Ref 12: 4,722 Windows Event Logs now flowing into Splunk*

*Ref 13: bayload.exe detected in Splunk via EventCode 4688*

*Ref 14: Full IOC table — account, process path, command line, parent process*

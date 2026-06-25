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

* First msfvenom attempt failing with directory error, mkdir fix and successful payload creation*
<img width="1928" height="1040" alt="1 making payload" src="https://github.com/user-attachments/assets/de0aff0b-cf40-498e-b83e-cef0d5969d2a" />


*Opening msfconsole*
<img width="1928" height="1040" alt="2 opening msfconsole" src="https://github.com/user-attachments/assets/812472e3-6ac8-47fe-9f9d-3ae82ee52d49" />


*using msf multihandler to configure payload*
<img width="1928" height="1040" alt="3 using msf multihandler to configure payload" src="https://github.com/user-attachments/assets/b3e0fb34-f0e9-487c-b9dc-275ae68e0e43" />


*creating http server*
<img width="1928" height="1040" alt="4 creating http server with python 3" src="https://github.com/user-attachments/assets/f0718f66-724d-40bb-abce-ce43cff14833" />


*running bayload on windows VM*
<img width="1928" height="1040" alt="5 directroy created on windows vm" src="https://github.com/user-attachments/assets/a5e6836d-e063-4513-9184-0b28831625dc" />


*Creating directory on kali VM*
<img width="1928" height="1040" alt="6 creating directory" src="https://github.com/user-attachments/assets/c20acfcd-6b8e-4eba-95c4-8a00944bd15e" />


*Directory from kali created on windows*
<img width="1928" height="1040" alt="7 directory created on kali created on windows" src="https://github.com/user-attachments/assets/29b17ff9-9ec3-4b6f-b132-76c291a2939d" />


*events not showing in splunk due to misconfiguration*
<img width="1928" height="1040" alt="8 events not showing bc of misconfig" src="https://github.com/user-attachments/assets/f20dd2cf-28ae-4860-bcd9-f33672f89e89" />


*Creating inputs.conf*
<img width="1928" height="1040" alt="9 creating inputs  conf" src="https://github.com/user-attachments/assets/356fbcd2-7bf1-4338-8928-f5536429ec10" />


*INputs.conf created*
<img width="1928" height="1040" alt="10 inputs conf created" src="https://github.com/user-attachments/assets/82be40ea-d510-48d2-b6e8-76c0b9eb81b7" />


*Restarting forwarder*
<img width="1928" height="1040" alt="11 restarting forwarder" src="https://github.com/user-attachments/assets/460ba8cb-d9e7-4727-841e-d0b4d896f19d" />


4,722 Windows Event Logs now flowing into Splunk*
<img width="1928" height="1040" alt="12 events shoowing" src="https://github.com/user-attachments/assets/f91e1c3c-b895-4a62-9002-0dfecd54db28" />


bayload.exe detected in Splunk via EventCode 4688*
<img width="1928" height="1040" alt="13 event code 4688" src="https://github.com/user-attachments/assets/b40d54c1-38d8-40c5-bd45-2f605e30445d" />


*Time window search*
<img width="1928" height="1040" alt="14 time frame event search" src="https://github.com/user-attachments/assets/a6aa53f6-bf1c-46f9-a61a-ab377af49882" />

*Bayload found*
<img width="1928" height="1040" alt="15 found bayload" src="https://github.com/user-attachments/assets/97993b2f-0ae0-4992-82cc-23fb301604de" />
*creator found*
<img width="1928" height="1040" alt="16 creator found" src="https://github.com/user-attachments/assets/2dd0689a-49ba-4a2d-a44a-7171789446c0" />
*Account and logon ID*
<img width="1928" height="1040" alt="17 aacount and logon ID" src="https://github.com/user-attachments/assets/edca0584-2f65-425f-b16a-e03a2584bef7" />
*configuring alert*
<img width="1928" height="1040" alt="18 alert config" src="https://github.com/user-attachments/assets/1f9661c7-f369-43b6-b06c-7ee76271b276" />
<img width="1928" height="1040" alt="19 alert config" src="https://github.com/user-attachments/assets/8b9115e1-d671-4db6-91d4-0527021d109a" />
*Alert active*
<img width="1928" height="1040" alt="20 alert active" src="https://github.com/user-attachments/assets/5063749f-b564-4d29-a693-fd4b4b839188" />

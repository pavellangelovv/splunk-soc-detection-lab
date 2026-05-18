# splunk-soc-detection-lab
Personal SOC lab using Splunk, Windows Event Logs, Kali Linux, and Sysmon for log analysis, detection engineering, and incident investigation.

The lab consists of three main components:
| Ubuntu Server VM | Splunk Server | Receives and indexes logs from the Windows endpoint |
| Windows Host | Monitored Endpoint | Sends Windows Event Logs and Sysmon logs to Splunk |
| Kali Linux VM | Attacker / Test Machine | Used later for controlled security testing and investigation scenarios |

Kali Linux VM  →  Windows Endpoint  →  Splunk Server
--

<img width="948" height="162" alt="01_authentication_event_summary" src="https://github.com/user-attachments/assets/aaad7d67-76d7-4d41-80f6-6ac13462c647" />

Instead of reviewing raw Windows events one by one this view gives a quick overview of authentication-related activity on the endpoint.From security perspective, this is useful because authentication activity is often one of the first areas analysts check during an investigation.

<img width="1221" height="293" alt="d1087c6c-8168-479b-afa9-07ec0addf70e" src="https://github.com/user-attachments/assets/a1dde298-2930-4825-a62c-073810b9d997" />

This screenshot shows a focused summary of Windows authentication-related security events collected in Splunk.
--

<img width="1643" height="219" alt="recon_process_commands" src="https://github.com/user-attachments/assets/d2997983-a27a-4690-b948-3bc69883b7b6" />
This screenshot shows Sysmon Process Create events for basic reconnaissance commands such as `whoami`, `ipconfig`, and `cmd.exe /c whoami`. The most important part of this view is the parent-child process relationship. 

---
<img width="583" height="547" alt="Екранна снимка 2026-05-18 125045" src="https://github.com/user-attachments/assets/e624e206-f067-475a-8b0f-413a825aba79" />
<img width="312" height="33" alt="Екранна снимка 2026-05-18 125323" src="https://github.com/user-attachments/assets/5a11410b-1cf1-411b-837e-648744ab566e" />

This screenshots shows a controlled Nmap scan launched from Kali Linux VM against the monitored Windows endpoint. The scan is used to simulate basic network reconnaissance. In practice, this type of activity means that a machine is checking which ports or services are reachable on another system. In this lab, the scan traffic is later visible in the Windows Firewall logs collected by Splunk, which allows the activity to be investigated.

--
Use Case: Reconnaissance and Persistence Simulation

This use case simulates a small intrusion investigation inside the lab. The investigation starts with a controlled Nmap scan from the Kali Linux VM against the monitored Windows endpoint. The scan is visible in the Windows Firewall logs collected by Splunk, where the Kali IP address attempts to connect to common Windows service ports. After identifying the network reconnaissance activity, the investigation continues by reviewing Sysmon process creation events from the same endpoint. The goal is to check whether there was suspicious local activity after the scan, such as command execution or persistence-related behavior. 

<img width="666" height="560" alt="Екранна снимка 2026-05-18 131141" src="https://github.com/user-attachments/assets/51b326ae-3fde-48a6-9cb7-e1ad570ece4f" />
<img width="1692" height="222" alt="Екранна снимка 2026-05-18 131445" src="https://github.com/user-attachments/assets/a0a46d5c-cf3f-452e-b20e-60b019517229" />

















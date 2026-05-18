# splunk-soc-detection-lab
Personal SOC lab using Splunk, Windows Event Logs, Kali Linux, and Sysmon for log analysis, detection engineering, and incident investigation.

The lab consists of three main components:
| Ubuntu Server VM | Splunk Server | Receives and indexes logs from the Windows endpoint |
| Windows Host | Monitored Endpoint | Sends Windows Event Logs and Sysmon logs to Splunk |
| Kali Linux VM | Attacker / Test Machine | Used later for controlled security testing and investigation scenarios |

Kali Linux VM  →  Windows Endpoint  →  Splunk Server

<img width="948" height="162" alt="01_authentication_event_summary" src="https://github.com/user-attachments/assets/aaad7d67-76d7-4d41-80f6-6ac13462c647" />

Instead of reviewing raw Windows events one by one this view gives a quick overview of authentication-related activity on the endpoint.From security perspective, this is useful because authentication activity is often one of the first areas analysts check during an investigation.






# splunk-soc-detection-lab
Personal SOC lab using Splunk, Windows Event Logs, Kali Linux, and Sysmon for log analysis, detection engineering, and incident investigation.

The lab consists of three main components:
| Ubuntu Server VM | Splunk Server | Receives and indexes logs from the Windows endpoint |
| Windows Host | Monitored Endpoint | Sends Windows Event Logs and Sysmon logs to Splunk |
| Kali Linux VM | Attacker / Test Machine | Used later for controlled security testing and investigation scenarios |

Kali Linux VM  →  Windows Endpoint  →  Splunk Server




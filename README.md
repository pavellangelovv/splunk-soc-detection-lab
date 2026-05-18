# splunk-soc-detection-lab
Personal SOC lab using Splunk, Windows Event Logs, Kali Linux, and Sysmon for log analysis, detection engineering, and incident investigation.

splunk-soc-detection-lab/
│
├── README.md
├── LICENSE
│
├── detections/
│   ├── DET-001_windows_authentication_monitoring.md
│   ├── DET-002_failed_logon_threshold_detection.md
│   ├── DET-003_privileged_logon_monitoring.md
│   ├── DET-004_explicit_credentials_usage.md
│   └── DET-005_credential_access_indicators.md
│
├── investigations/
│   └── README.md
│
├── splunk_queries/
│   ├── windows_authentication_detection_queries.spl
│   └── windows_security_event_overview.spl
│
├── configs/
│   └── inputs.conf
│
└── screenshots/
    ├── ingestion/
    │   └── 01_windows_eventlog_ingestion.png
    │
    └── detections/
        ├── 01_security_eventcode_overview.png
        ├── 02_authentication_activity_timeline.png
        ├── 03_failed_logon_detection.png
        ├── 04_privileged_logon_detection.png
        └── 05_credential_access_related_events.png

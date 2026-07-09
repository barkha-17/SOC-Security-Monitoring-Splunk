# 🛡️ Security Operations Center (SOC) Monitoring Using Splunk Enterprise

A hands-on Security Operations Center (SOC) laboratory built using **Splunk Enterprise**, **Microsoft Sysmon**, **Windows Event Logs**, **Splunk Universal Forwarder**, and **Kali Linux** to simulate real-world security monitoring, threat detection, automated alerting, and incident investigation.

---

# 📖 Project Overview

This project demonstrates the implementation of a Security Operations Center (SOC) using **Splunk Enterprise** as the Security Information and Event Management (SIEM) platform.

The lab was designed to provide practical experience in:

- Security monitoring
- Log collection and analysis
- Endpoint monitoring
- Threat detection
- Incident investigation
- Dashboard development
- Custom SPL detection rules
- Automated alerting

The project simulates common cyber attack scenarios and demonstrates how security events can be collected, analysed, and investigated within a SOC environment.

---

# 🎯 Project Objectives

- Deploy Splunk Enterprise
- Configure Splunk Universal Forwarder
- Integrate Microsoft Sysmon
- Collect Windows Security & Sysmon Logs
- Build a SOC Monitoring Dashboard
- Create custom SPL detection rules
- Configure scheduled alerts
- Simulate attacks using Kali Linux
- Map detections to the MITRE ATT&CK Framework

---

# 🏗️ SOC Lab Architecture

```text
Kali Linux VM
       │
       ▼
Windows 10 VM
(Sysmon + Windows Event Logs)
       │
       ▼
Splunk Universal Forwarder
       │
       ▼
Splunk Enterprise
       │
       ▼
SOC Dashboard & Alerts
```

---

# 🛠️ Tools & Technologies

The SOC environment was built using the following technologies:

- **Splunk Enterprise** – Security Information and Event Management (SIEM)
- **Splunk Universal Forwarder** – Secure log forwarding
- **Microsoft Sysmon** – Advanced endpoint telemetry
- **Windows Event Logs** – Native Windows security logging
- **Windows 10** – Monitored endpoint
- **Kali Linux** – Attack simulation platform
- **SPL (Search Processing Language)** – Detection rule development
- **MITRE ATT&CK Framework** – Threat classification and mapping

---

# 🔍 Security Scenarios

The project includes detection and monitoring for:

- PowerShell execution
- Failed login attempts
- Process creation
- DNS queries
- Network connections
- Suspicious processes
- Windows security events

---

# 🚨 Detection Rules

The following custom detection rules were developed:

- PowerShell Execution Detection
- Failed Login Detection
- Process Creation Detection
- DNS Query Detection
- Network Connection Detection
- Suspicious Process Detection
- Registry Monitoring
- Security Event Monitoring

---

# 📊 Dashboard Features

The SOC dashboard provides real-time visibility into:

- Total Security Events
- Failed Login Attempts
- Successful Logins
- Endpoint Telemetry
- Security Events Over Time
- DNS Queries
- Network Connections
- Top Processes
- Top Hosts
- Security Event Distribution

---

# 🚨 Alerting

Scheduled alerts were configured for:

- PowerShell Execution
- Failed Login Attempts
- DNS Query Detection
- Process Creation Detection
- Network Connection Detection
- Suspicious Process Detection

---

# 🎯 MITRE ATT&CK Mapping

The implemented detections were aligned with the MITRE ATT&CK Framework, covering techniques related to:

- Initial Access
- Execution
- Persistence
- Defense Evasion
- Credential Access
- Discovery
- Command and Control

---

# 🧠 Skills Demonstrated

- Security Operations Center (SOC)
- SIEM Implementation
- Splunk Enterprise
- Threat Detection
- Threat Hunting
- Incident Investigation
- Windows Event Monitoring
- Microsoft Sysmon
- Log Analysis
- SPL Query Development
- Dashboard Development
- Alert Engineering
- MITRE ATT&CK Mapping

---

# 📂 Repository Structure

```
SOC-Security-Monitoring-Splunk/
│
├── Detection-Rules/
├── Dashboards/
├── Alerts/
├── Documentation/
└── README.md
```

# 📚 References

- Splunk Documentation
- Microsoft Sysmon Documentation
- MITRE ATT&CK Framework
- Microsoft Windows Security Documentation

---

# 👨‍💻 Author

Barkha Shah

M.Sc. Digital Forensics & Cyber Security

GitHub: https://github.com/barkha-17

LinkedIn: https://linkedin.com/in/barkha-shah-24a912285/

---

## 📬 Feedback

If you have any suggestions or feedback regarding this project, feel free to connect with me on LinkedIn or open an issue in this repository.

⭐ If you found this project interesting, consider giving it a star.

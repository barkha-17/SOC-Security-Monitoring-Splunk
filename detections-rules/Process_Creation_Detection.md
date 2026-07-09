# Process Creation Detection

## Objective

Monitor process creation events using Microsoft Sysmon to identify newly executed processes on the endpoint.

---

## SPL Query

```spl
index=* sourcetype="XmlWinEventLog:Microsoft-Windows-Sysmon/Operational"
EventID=1
| stats count by Image User
```

---

## Detection Logic

This detection monitors **Sysmon Event ID 1**, which records every newly created process. Monitoring process creation helps identify suspicious applications, unauthorized tools, or malicious executables running on the system.

---

## MITRE ATT&CK Mapping

| Tactic | Technique |
|---------|-----------|
| Execution | T1204 – User Execution |

---

## Expected Output

The search returns:

- Process Image
- User
- Number of Process Executions

This information provides visibility into application execution across the monitored endpoint.

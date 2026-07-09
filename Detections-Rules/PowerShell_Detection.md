# PowerShell Execution Detection

## Objective

Detect PowerShell execution on the monitored Windows endpoint using Sysmon Process Creation events.

---

## SPL Query

```spl
index=* sourcetype="XmlWinEventLog:Microsoft-Windows-Sysmon/Operational"
| search powershell
| rex field=_raw "<Data Name='Image'>(?<Image>[^<]+)</Data>"
| rex field=_raw "<Data Name='CommandLine'>(?<CommandLine>[^<]+)</Data>"
| rex field=_raw "<Data Name='User'>(?<User>[^<]+)</Data>"
| table _time host User Image CommandLine
```

---

## Detection Logic

This rule searches Sysmon Process Creation events for PowerShell activity. It extracts the executing user, process image, and command line to help identify potentially suspicious PowerShell execution.

---

## MITRE ATT&CK Mapping

| Tactic | Technique |
|---------|-----------|
| Execution | T1059.001 – PowerShell |

---

## Expected Output

The search returns:

- Timestamp
- Host
- User
- Process Image
- Command Line

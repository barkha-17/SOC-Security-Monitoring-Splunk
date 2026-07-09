# Suspicious Process Detection

## Objective

Detect the execution of commonly abused Windows utilities and administrative tools that may be used during malicious activities.

---

## SPL Query

```spl
index=* sourcetype="XmlWinEventLog:Microsoft-Windows-Sysmon/Operational"
EventID=1
(Image="*cmd.exe" OR Image="*powershell.exe" OR Image="*psexec.exe" OR Image="*wmic.exe")
| table _time host User Image CommandLine
```

---

## Detection Logic

This detection monitors the execution of commonly abused administrative tools such as **PowerShell**, **Command Prompt**, **PsExec**, and **WMIC**. While these tools are legitimate, they are frequently used by attackers during post-exploitation and lateral movement.

---

## MITRE ATT&CK Mapping

| Tactic | Technique |
|---------|-----------|
| Execution | T1059 – Command and Scripting Interpreter |

---

## Expected Output

The search returns:

- Timestamp
- Host
- User
- Process Image
- Command Line

This information helps identify potentially suspicious process execution that may require further investigation.

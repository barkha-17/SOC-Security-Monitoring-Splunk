# Failed Login Detection

## Objective

Detect multiple failed Windows login attempts to identify potential brute-force attacks or unauthorized access attempts.

---

## SPL Query

```spl
index=* EventCode=4625
| stats count by Account_Name
```

---

## Detection Logic

This detection monitors Windows Security Event ID **4625**, which is generated whenever a user authentication attempt fails. Repeated failed login attempts may indicate password guessing, brute-force attacks, or invalid credential usage.

---

## MITRE ATT&CK Mapping

| Tactic | Technique |
|---------|-----------|
| Credential Access | T1110 – Brute Force |

---

## Expected Output

The search returns:

- Username
- Number of failed login attempts

This information helps identify accounts experiencing repeated authentication failures.

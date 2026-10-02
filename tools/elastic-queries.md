# Splunk Query Examples

## Suspicious PowerShell Execution

```spl
index=windows sourcetype=WinEventLog:Microsoft-Windows-PowerShell/Operational EventCode=4104
| stats count by host, user, CommandLine
| search count>0
```

## Failed Logins

```spl
index=windows sourcetype=WinEventLog:Security EventCode=4625
| stats count by host, user, src_ip
| sort -count
```

## New Service Creation

```spl
index=windows sourcetype=WinEventLog:Security EventCode=4697
| table _time host user ServiceName ServiceFileName
```

## Lateral Movement Indicators

```spl
index=windows sourcetype=WinEventLog:Security (EventCode=4624 OR EventCode=4625) Account_Name!=*$
| stats count by host, Account_Name, Logon_Type
```

---

Adapt these queries to your dataset and threat model.

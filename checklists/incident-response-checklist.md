# YARA and Sigma Notes

## YARA

YARA is useful for identifying malicious patterns in files, memory, or artifacts.

Example concept:

```yara
rule suspicious_powershell_obfuscation {
    meta:
      description = "Detect suspicious PowerShell obfuscation patterns"
      author = "Security Lab"
    strings:
      $a = "FromBase64String" ascii
      $b = "IEX" ascii
      $c = "New-Object Net.WebClient" ascii
      $d = "http://" ascii
    condition:
      2 of ($a,$b,$c,$d)
}
```

## Sigma

Sigma is useful for writing detection rules that can be converted across SIEM platforms.

Example pattern ideas:

- PowerShell command line with encoded payloads
- Service creation on Windows hosts
- Login failures from a single host to multiple accounts
- Rare process spawning from suspicious parent processes

## Usage Notes

- Tune detections to reduce false positives
- Add asset and user context where possible
- Use Sigma for normalized detection logic
- Validate with telemetry in your environment

---

YARA and Sigma help turn your hunting hypotheses into reusable detections.

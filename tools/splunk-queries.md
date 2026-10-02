# Windows Forensics Notes

## Common Sources

- Windows Event Logs
- Security log
- PowerShell operational log
- Sysmon log
- Application and System logs
- Prefetch and Recent files
- Registry hives
- Scheduled tasks
- Services and startup paths

## Focus Areas

- Suspicious PowerShell execution
- New scheduled tasks or service creation
- Run key and autorun changes
- Privileged account use
- Remote administration activity
- Persistence and beaconing

## Useful Tools

- Process Explorer
- Autoruns
- Sysinternals Suite
- Event Viewer
- WMIC / PowerShell
- netstat and tasklist

## Example Checks

- Check for suspicious new services
- Review PowerShell command line arguments
- Inspect startup registry keys
- Review remote logon events and account changes
- Look for DLL sideloading and binary path abuse

---

These notes support Windows endpoint investigations in hunting and incident response labs.

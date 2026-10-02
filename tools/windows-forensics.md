# Linux Forensics Notes

## Common Sources

- /var/log/auth.log
- /var/log/syslog
- /var/log/kern.log
- /var/log/apache2/
- /var/log/nginx/
- /var/spool/cron/
- /etc/passwd and /etc/shadow
- /etc/cron* and /etc/systemd/system
- Shell histories (.bash_history, .zsh_history)

## Focus Areas

- New user creation
- Unauthorized cron jobs
- Suspicious shell commands
- Modified system binaries
- SSH logins and key usage
- Service and daemon tampering

## Useful Commands

```bash
last
who
ps -ef
ss -tulpn
ls -l /etc/cron* /var/spool/cron
find / -xdev -type f -mtime -7
cat /var/log/auth.log | tail -n 200
```

## Investigation Tips

- Check for unusual cron or service files
- Review command history for destructive or network commands
- Confirm whether binaries were replaced or tampered with
- Review permission changes and SUID binaries

---

These notes are useful in linux-focused threat hunting and incident triage exercises.

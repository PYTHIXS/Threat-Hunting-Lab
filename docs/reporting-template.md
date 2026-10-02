# Defense and Hardening Guide

This guide focuses on practical controls that reduce exposure and improve resilience.

## 1. Core Defense Principles

- Least privilege
- Security by default
- Reduce the attack surface
- Maintain visibility and logging
- Segment critical assets
- Validate backups and recovery

## 2. Endpoint Hardening

- Remove unnecessary software
- Enforce local firewall rules
- Disable SMBv1 and unnecessary services
- Restrict admin rights
- Enable EDR coverage
- Apply OS and application patches
- Disable macros and scripting where possible

## 3. Identity and Access Controls

- Enforce MFA
- Use PAM for high-risk accounts
- Rotate credentials regularly
- Review privileged group membership
- Monitor sign-in anomalies and impossible travel

## 4. Network Defense

- Restrict ingress and egress paths
- Segment production, admin, and user networks
- Use IDS/IPS or network security analytics
- Block malicious domains and IPs
- Monitor suspicious outbound connections

## 5. Application Security

- Validate input and output encoding
- Enforce secure session handling
- Use dependency scanning for third-party components
- Review authN/authZ logic
- Adopt secure development practices and code review

## 6. Detection Engineering

Use detections that detect behavior, not just malware signatures.

Examples:

- Suspicious PowerShell execution
- Abnormal service creation
- New startup persistence items
- Privilege escalation commands
- Lateral movement through admin shares
- Unexpected external data transfers

## 7. Response and Recovery

- Contain impacted systems quickly
- Collect forensic evidence
after containment when appropriate
- Isolate malicious assets
- Restore from clean restore points
- Reassess security posture before returning systems to service

---

This is a practical foundation for building a resilient security posture in a lab or production environment.

# Threat Hunting, Vulnerability Analysis, Defense & Reporting Lab

This guide outlines the core principles and workflows for a modern cybersecurity lab focused on threat hunting, vulnerability analysis, defensive controls, and reporting.

## 1. Threat Hunting Playbook

Threat hunting is proactive. It begins with a hypothesis, then looks for evidence of malicious behavior that may not yet have triggered a rule.

### Core Hunting Questions

- What adversary behavior are we looking for?
- What systems or identities are likely targets?
- What telemetry sources will confirm or disprove the theory?
- What unusual activity would stand out from the baseline?

### Typical Hunting Activities

- Review abnormal process execution
- Search for persistence techniques
- Investigate suspicious authentication events
- Detect privilege escalation or credential dumping
- Look for lateral movement or exfiltration patterns
- Correlate suspicious indicators across hosts, identity, and network

### Example TTPs

- PowerShell usage with encoded commands
- Rundll32/WMIC service abuse
- Scheduled task creation
- Shadow Copy abuse
- Remote service creation via PsExec or WinRM
- Suspicious DNS tunneling or beaconing
- Abnormal administrative logins

## 2. Vulnerability Analysis

Vulnerability analysis involves identifying weaknesses, establishing exploitation conditions, and evaluating the business risk if exploited.

### Key Questions

- What is the vulnerable asset?
- What is the affected component and version?
- Is the vulnerability remotely exploitable?
- What are the preconditions for exploitation?
- What is the impact to confidentiality, integrity, and availability?
- Is the system internet-facing or restricted?

### Risk Prioritization

Use a combination of:

- Severity and exploitability
- Asset criticality
- Exposure level
- Whether a patch is available
- Whether compensating controls exist

## 3. Defender Mindset

Defense is about reducing attacker opportunities. Focus on layered controls.

### Essential Practices

- Keep asset inventory current
- Patch aggressively and validate reboot windows
- Enforce MFA and privileged access management
- Disable unnecessary services and ports
- Tighten application permissions and file integrity monitoring
- Use detection rules and behavioral alerts
- Validate backups and resilience procedures
- Review logs for attacker persistence and credential abuse

## 4. Reporting and Communication

Security reporting must be brief, accurate, and actionable.

### Reporting Structure

- Executive Summary
- Incident or finding description
- Evidence and timeline
- Impact analysis
- Root cause or vulnerability summary
- Recommendations and priorities
- Owner and due dates

### Good Findings Include

- What was observed
- Why it matters
- What evidence supports the claim
- What the recommended action is
- Whether this is active, historical, or potential

## 5. Lab Workflow

```text
Define the scenario
Collect evidence
Analyze the behaviour
Determine impact
Remediate or defend
Document findings
Report recommendations
```

## 6. Suggested Exercise Set

- Hunt for persistence in a Windows workstation
- Investigate phishing credential abuse in a cloud environment
- Triage a critical web app vulnerability
- Review suspicious lateral movement across a domain
- Analyze data exfiltration and user abnormality patterns

## 7. Deliverables

A useful lab pack should include:

- Threat hypotheses
- Timeline of events
- Detection or hunting queries
- Risk rating and impact
- Remediation plan
- Final report in technical and executive format

---

This document is a starting point. Expand it with your own internal notes, detections, and findings as your lab evolves.

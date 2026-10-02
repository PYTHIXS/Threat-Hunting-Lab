# Scenario 1: Ransomware Attack Simulation

## Objective

Practice response and detection for a ransomware-style incident.

## Initial Signals

- Multiple hosts show suspicious execution of a PowerShell script
- Files have been encrypted in a short period
- New scheduled tasks or service creation are observed
- Network beaconing is detected to a suspicious external IP

## Investigation Tasks

1. Identify the initial infection vector
2. Determine the first known malicious event
3. Review persistence mechanisms
4. Validate lateral movement path
5. Assess impacted assets and data exposure
6. Recommend containment and recovery actions

## Evidence to Review

- EDR alerts
- PowerShell logs
- Event Viewer security logs
- Network firewall logs
- DNS and proxy logs
- File integrity or backup status

## Reporting Focus

- What happened and how it was detected
- What assets were impacted
- What controls failed or were absent
- Which actions were taken to contain the issue
- What preventive controls should be added

---

This scenario is useful for understanding detection, triage, and communication under pressure.

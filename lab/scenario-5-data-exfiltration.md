# Scenario 4: Lateral Movement Analysis

## Objective

Investigate suspicious movement across systems in a compromised network.

## Initial Signals

- A workstation has suspicious process executions
- New remote administration tools or commands appear on other hosts
- Administrative privilege abuse is suspected

## Investigation Tasks

1. Identify the origin host
2. Correlate the lateral movement path
3. Review SMB, RDP, WinRM, or SSH activity
4. Identify stolen credentials or service account abuse
5. Assess what systems were accessed and whether data was exposed

## Evidence to Review

- EDR telemetry
- Windows Security logs
- Network connection data
- Scheduled tasks and services
- Group policy and admin logs

## Reporting Focus

- Why the attacker succeeded
- Attack path and timeline
- Impacted systems and risk
- Controls that should be added or tightened

---

Lateral movement exercises are ideal for learning how to connect suspicious user and system actions into a single narrative.

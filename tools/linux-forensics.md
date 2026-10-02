# Scenario 5: Data Exfiltration Review

## Objective

Practice detecting exfiltration and documenting the impact of data theft.

## Initial Signals

- Unusual outbound transfers are observed
- Sensitive documents were accessed shortly before transfer
- External IP traffic exceeds normal patterns

## Investigation Tasks

1. Identify which files or datasets were accessed
2. Review user behavior and suspicious system actions
3. Determine the exfiltration vector
4. Assess scope, sensitivity, and impact
5. Recommend detections and network controls

## Evidence to Review

- File access logs
- Proxy and firewall logs
- Cloud storage logs
- EDR telemetry
- Endpoint file analysis

## Reporting Focus

- What data was exposed
- How the data was sent
- Whether the activity was successful
- Recommended containment and prevention actions

---

This scenario builds capability in full-incident analysis and executive-level communication about data loss risk.

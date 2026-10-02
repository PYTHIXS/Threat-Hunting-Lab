# Detection Strategy Reference

## Detection Principles

- Prefer behavior over static signatures where possible
- Correlate across endpoint, identity, network, and cloud
- Enrich alerts with asset and user context
- Define clear false-positive tuning criteria

## High-Value Signals

- Anomalous logons
- Suspicious process trees
- New persistence artifacts
- Lateral movement attempts
- Data staging and outbound transfer anomalies

## Good Detection Workflow

1. Capture the suspicious behavior
2. Compare it to the baseline
3. Validate with related telemetry
4. Tune and document the detection
5. Review coverage on a recurring basis

---

This reference helps turn lab findings into repeatable detection logic.

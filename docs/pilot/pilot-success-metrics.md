# Pilot Success Metrics

Last updated: 2026-04-28

This document defines objective criteria for pilot acceptance.

## 1) Stability Metrics

- Maintains target setpoint within defined variance under normal load.
- Avoids oscillation around setpoint beyond acceptable cycle behavior.
- Demonstrates consistent behavior across repeated daily windows.

## 2) Cycle Protection Metrics

- No short cycling under normal operating conditions.
- Minimum on/off cycle rules are enforced.
- Cycle events are traceable in logs.

## 3) Fault Handling Metrics

- Sensor loss is detected within expected threshold.
- Out-of-range or frozen readings trigger documented safe behavior.
- Fault state and recovery are clearly visible to operator.

## 4) Recovery Metrics

- Controlled recovery after power interruption.
- Restart behavior avoids unsafe immediate relay toggling.
- System returns to known-good state without manual reconfiguration.

## 5) Override and Control Governance

- Manual override behavior follows documented policy.
- Override actions are visible in logs/audit trail.
- Return to automatic control is deterministic.

## 6) Logging and Evidence Quality

- Runtime events captured with timestamp and context.
- Fault and recovery events recorded with action taken.
- Validation runs are documented using the standard run log template.

## 7) Pilot Pass Criteria

Pilot is considered successful when:

1. All critical safety and fault-handling checks pass.
2. No unresolved high-severity anomalies remain.
3. Stability and cycle metrics meet agreed thresholds.
4. Site operator confirms readiness for ongoing use.

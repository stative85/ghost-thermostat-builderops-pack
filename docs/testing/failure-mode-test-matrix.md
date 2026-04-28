# Failure Mode Test Matrix

Last updated: 2026-04-28

Use this matrix to validate reliability-first behavior across expected failure conditions.

## Legend

- Severity: Low / Medium / High / Critical
- Result: Pass / Fail / Needs Follow-up

## Test Matrix

| Test ID | Failure Mode | Trigger Method | Expected Behavior | Severity | Result | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| FM-01 | Sensor loss/disconnect | Physically disconnect or simulate null input | Detect fault quickly, enter safe mode, alert operator | Critical |  |  |
| FM-02 | Frozen sensor value | Hold static input despite ambient change | Detect stale value, prevent unsafe cycling, raise fault | High |  |  |
| FM-03 | Out-of-range reading | Inject impossible value | Reject reading, preserve safe control state, log incident | High |  |  |
| FM-04 | Power interruption | Cut and restore power | Clean restart, enforce startup protections, recover known-good state | Critical |  |  |
| FM-05 | Manual override | Apply manual setpoint override | Honor policy, log action, deterministic return to auto mode | Medium |  |  |
| FM-06 | Relay stuck on/off | Simulate relay state mismatch | Detect mismatch, alert operator, prevent unsafe sustained call | Critical |  |  |
| FM-07 | Min-cycle violation attempt | Rapid setpoint toggles or load swings | Enforce minimum on/off timing, avoid short cycling | High |  |  |

## Execution Notes

- Capture each run in `docs/strategy/validation-run-log-template.md`.
- Any Critical failure is a release blocker.
- Re-test all affected matrix rows after control logic changes.

## Sign-off

- Executed by:
- Reviewed by:
- Date:

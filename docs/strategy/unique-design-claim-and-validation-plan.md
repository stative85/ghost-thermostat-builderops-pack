# Unique Design Claim and Validation Plan

Last updated: 2026-04-28

## 1) Core Design Claim

The Ghost Thermostat uses a simplified control architecture that reduces operational complexity while maintaining stable temperature control and predictable fail-safe behavior.

## 2) Why This Is Different

- Fewer moving parts in the operating model reduce points of failure.
- Clear control rules improve consistency across installs.
- Standardized commissioning sequence shortens deployment time.
- Explicit fallback behavior improves recoverability during faults.

## 3) Success Criteria

The design is considered validated when all criteria below are met:

1. Temperature stability remains within defined variance targets in normal operation.
2. Fault scenarios trigger expected safe-state behavior without operator confusion.
3. Field deployment can be completed using documented steps without undocumented workarounds.

## 4) Validation Scenarios

## Scenario A: Normal Cycle Stability

**Goal:** Demonstrate stable, repeatable temperature control in nominal conditions.

**Inputs:**

- Target setpoint
- Ambient starting temperature
- Runtime window (minimum test duration)

**Measure:**

- Time to reach setpoint
- Overshoot/undershoot behavior
- Number of control cycles during window

**Pass condition:** Behavior remains inside predefined limits with no manual intervention.

## Scenario B: Sensor Fault Handling

**Goal:** Verify safe and deterministic behavior when sensor data is invalid or unavailable.

**Inject:**

- Sensor disconnect
- Frozen sensor value
- Out-of-range reading

**Measure:**

- Time to detect fault
- Fallback mode activation
- Operator alert/log visibility

**Pass condition:** System enters documented safe mode and produces a clear, actionable fault record.

## Scenario C: Power Loss and Recovery

**Goal:** Confirm safe restart and state recovery after interruption.

**Inject:**

- Controlled power cut
- Unplanned restart simulation

**Measure:**

- Startup sequence correctness
- Recovery to expected mode/state
- Time to normal operation

**Pass condition:** No unsafe behavior at restart; system returns to known-good state predictably.

## 5) Evidence Package Requirements

For each test run, capture:

- Test ID and date/time
- Configuration and environment details
- Operator name
- Raw measurements
- Outcome (pass/fail)
- Follow-up actions for failures

Store evidence under version control or linked immutable storage with references in this repository.

## 6) Risk Register (Initial)

- **Ambiguous control thresholds** -> Define numeric limits and lock them per version.
- **Undocumented edge-case behavior** -> Expand fault matrix and add explicit handling notes.
- **Operator variability** -> Enforce runbook and commissioning checklist usage.

## 7) Change Control

- Any change to control logic requires:
  - Version increment
  - Validation re-run for affected scenarios
  - `CHANGELOG.md` update

## 8) One-Sentence External Positioning

Ghost Thermostat delivers a simpler, more operationally reliable control design that is easier to deploy, verify, and maintain than complexity-heavy alternatives.

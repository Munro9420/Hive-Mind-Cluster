# Coordination templates

Adapt these to the task. Keep the coordinator's state authoritative and share changes explicitly.

## Shared brief

```text
Goal:
Deliverables and acceptance criteria:
Constraints and authorized actions:
Inputs and source references:
Workstreams: ID | owner | dependency | status | output
Decisions and evidence:
Unresolved issues:
Verification completed and still needed:
Latest user change:
```

Use statuses such as pending, active, blocked, completed, and cancelled. For substantial work, identify the brief's current revision so workers can flag results based on outdated instructions.

## Specialist assignment

```text
Task ID and role:
Display task name:
Specific work steps:
Plan ownership: separate agent plan, or progress reports to the coordinator's shared plan.
Progress reports: step started, completed work with evidence, blockers, and final status.
Outcome you own:
Context and inputs:
Constraints and dependencies:
Permitted actions:
Files or resources you may edit (otherwise read-only):
Acceptance criteria:
Return: result, evidence, changed paths, checks performed, uncertainty, status.
Report early: blocking facts, conflicting instructions, findings affecting others.
Stop when: the assigned acceptance criteria are met or a concrete blocker prevents progress.
Do not delegate further unless the coordinator explicitly assigns it.
```

## Evidence handoff

```text
Task ID and brief revision:
Result:
Evidence or source references:
Artifacts changed:
Checks actually run and observed outcomes:
Assumptions and unresolved issues:
Status and recommended next action:
```

Label external facts, user-provided facts, calculations, and assumptions so the coordinator can judge support. Keep quotes within applicable limits and preserve source attribution.

## Review assignment

Give the reviewer the original request, relevant constraints, final candidate artifact, and applicable evidence. Ask them to identify material defects and confirm only checks they perform. Avoid including the producer's confidence or expected verdict. Require concrete findings tied to the artifact, with a targeted fix or verification step when possible.

## Recovery and resumption

Before resuming, inspect the actual task and artifact state. Record what was completed, what remains, current ownership, unresolved conflicts, and the next useful action. Do not assume an agent is still running or a file was saved because an earlier plan said so.

When an assignment stalls, check its status through the supported host tool. Reassign or reduce scope if that advances the result. Coordinate ownership before a replacement edits the same files. If a previous writer cannot be stopped, use a separate output location and integrate only after inspecting both results.

When the user changes requirements, send the change to affected workers and invalidate conflicting assumptions. Stop cancelled work before final integration. If an external action may already have happened, inspect the actual state before retrying to avoid duplicate effects.

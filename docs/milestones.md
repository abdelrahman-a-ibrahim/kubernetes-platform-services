# Implementation backlog

Status: all milestones unstarted. Check a task only when its evidence exists.

## M1 — Design and contracts

Create a dependency graph and lifecycle plan for add-ons. Separate cluster-wide privileges from namespaced application access.

- [ ] Turn this milestone into a small design/task note with inputs and outputs.
- [ ] Implement the smallest complete behavior for this milestone.
- [ ] Add positive, negative and recovery checks relevant to this behavior.
- [ ] Record commands, environment and observed results in the learning journal.
- [ ] Update the README status and architecture if the implementation changes them.

**Review gate:** demonstrate the behavior, explain a tradeoff and link actual evidence. Do not mark complete using foundation checks alone.

## M2 — Build the first path

Package a workload with Helm or Kustomize, including requests/limits, health probes, config and secret references. Do not store secrets in manifests.

- [ ] Turn this milestone into a small design/task note with inputs and outputs.
- [ ] Implement the smallest complete behavior for this milestone.
- [ ] Add positive, negative and recovery checks relevant to this behavior.
- [ ] Record commands, environment and observed results in the learning journal.
- [ ] Update the README status and architecture if the implementation changes them.

**Review gate:** demonstrate the behavior, explain a tradeoff and link actual evidence. Do not mark complete using foundation checks alone.

## M3 — Integrate deliberately

Add a GitOps reconciler and define bootstrap ordering, sync boundaries and rollback behavior. Pin chart and image versions.

- [ ] Turn this milestone into a small design/task note with inputs and outputs.
- [ ] Implement the smallest complete behavior for this milestone.
- [ ] Add positive, negative and recovery checks relevant to this behavior.
- [ ] Record commands, environment and observed results in the learning journal.
- [ ] Update the README status and architecture if the implementation changes them.

**Review gate:** demonstrate the behavior, explain a tradeoff and link actual evidence. Do not mark complete using foundation checks alone.

## M4 — Handle failure

Add network policies, quotas, restrictive workload defaults and scoped RBAC. Use local certificates until DNS/domain prerequisites are explicit.

- [ ] Turn this milestone into a small design/task note with inputs and outputs.
- [ ] Implement the smallest complete behavior for this milestone.
- [ ] Add positive, negative and recovery checks relevant to this behavior.
- [ ] Record commands, environment and observed results in the learning journal.
- [ ] Update the README status and architecture if the implementation changes them.

**Review gate:** demonstrate the behavior, explain a tradeoff and link actual evidence. Do not mark complete using foundation checks alone.

## M5 — Demonstrate and operate

Perform an add-on upgrade and failed reconciliation recovery; capture runbooks, resource consumption and a decommission sequence.

- [ ] Turn this milestone into a small design/task note with inputs and outputs.
- [ ] Implement the smallest complete behavior for this milestone.
- [ ] Add positive, negative and recovery checks relevant to this behavior.
- [ ] Record commands, environment and observed results in the learning journal.
- [ ] Update the README status and architecture if the implementation changes them.

**Review gate:** demonstrate the behavior, explain a tradeoff and link actual evidence. Do not mark complete using foundation checks alone.


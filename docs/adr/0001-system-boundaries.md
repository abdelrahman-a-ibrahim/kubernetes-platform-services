# ADR 0001: System boundaries and implementation approach

Status: proposed.

## Context
A cluster-services repository for managing application packaging and supporting add-ons through versioned desired state. It covers dependency ordering, scoped permissions, configuration, policy enforcement and controlled component upgrades.

## Questions
- Helm versus Kustomize responsibilities
- GitOps reconciliation boundaries
- Add-on upgrade ownership and compatibility policy

## Alternatives
- A local implementation with synthetic external adapters.
- An integrated deployment with real dependencies in an isolated environment.
- A smaller implementation that preserves the core invariant.

## Decision
Pending. Record the selected option, rejected alternatives and rationale before implementing external adapters.

## Consequences
Assess correctness, operational complexity, cost, security boundaries, recovery and maintenance. Define the concrete constraint that would justify revisiting the decision.

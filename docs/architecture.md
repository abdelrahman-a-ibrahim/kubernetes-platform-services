# Architecture

Status: proposed. Components shown below are implementation targets.

## Product context
A cluster-services repository for managing application packaging and supporting add-ons through versioned desired state. It covers dependency ordering, scoped permissions, configuration, policy enforcement and controlled component upgrades.

## Component view
```text
Versioned desired state -> reconciliation -> add-ons / namespaces
                                                   |
                                            application workloads
```

## Design decisions
- Helm versus Kustomize responsibilities
- GitOps reconciliation boundaries
- Add-on upgrade ownership and compatibility policy

Record decisions and alternatives in [ADR 0001](adr/0001-system-boundaries.md). Define authoritative state, acknowledgement boundaries, identities, retry behavior and recovery ownership before implementing adapters.

## Interface boundary
`src/kubernetes_platform_services/interfaces.py` defines the initial application boundary. Return models and error contracts remain to be specified. These interfaces do not implement the component graph.

## Integration boundaries
Local adapters and synthetic fixtures precede external integrations. Every live adapter needs an explicit identity, permission scope, timeout strategy and observability contract. Separate user-supplied content from execution authority.

## Deployment design
Document topology, dependency versions, configuration and state persistence alongside the first executable delivery. Record what local environments cannot establish about availability, ordering or durability.

## Compatibility
Version interfaces and fixtures when their semantics change. Sibling projects are optional integrations, not implicit filesystem dependencies.

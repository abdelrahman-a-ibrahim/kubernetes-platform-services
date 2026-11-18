# Delivery roadmap

Status: planned. No delivery stage is complete.

### 1. Contracts and system boundaries

Create a dependency graph and lifecycle plan for add-ons. Separate cluster-wide privileges from namespaced application access.

- [ ] Implementation
- [ ] Behavior verification and failure coverage
- [ ] Documentation and reproducible results

### 2. Core implementation

Package a workload with Helm or Kustomize, including requests/limits, health probes, config and secret references. Do not store secrets in manifests.

- [ ] Implementation
- [ ] Behavior verification and failure coverage
- [ ] Documentation and reproducible results

### 3. Integrations and access controls

Add a GitOps reconciler and define bootstrap ordering, sync boundaries and rollback behavior. Pin chart and image versions.

- [ ] Implementation
- [ ] Behavior verification and failure coverage
- [ ] Documentation and reproducible results

### 4. Recovery and operational behavior

Add network policies, quotas, restrictive workload defaults and scoped RBAC. Use local certificates until DNS/domain prerequisites are explicit.

- [ ] Implementation
- [ ] Behavior verification and failure coverage
- [ ] Documentation and reproducible results

### 5. Release validation

Perform an add-on upgrade and failed reconciliation recovery; capture runbooks, resource consumption and a decommission sequence.

- [ ] Implementation
- [ ] Behavior verification and failure coverage
- [ ] Documentation and reproducible results

## Future scope

- Admission policy and signed image checks
- Multi-tenant namespace templates
- Progressive delivery controller experiment
- Automated deprecated-API inventory

Select and pin implementation dependencies when introduced. Scope is refined through architecture decisions; completion requires working behavior and verification evidence.

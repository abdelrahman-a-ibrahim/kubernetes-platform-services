# Verification plan

Runtime behavior tests will be added with the implementation. The current source integrity check does not provide runtime coverage.

## Required behavior coverage
- Fresh-cluster bootstrap is reproducible from the documented inputs.
- Application identity cannot change cluster-scoped resources.
- A failed upgrade has a tested recovery path.
- Dependency checks distinguish missing add-ons from application bugs.

## Failure coverage
- Deploy an incompatible chart value and observe reconciliation.
- Remove access to a referenced secret.
- Block an application dependency with network policy.
- Upgrade an add-on with an incompatible CRD version in a disposable cluster.

Add domain tests, adapter contract tests and integration tests as those components are implemented. Include relevant invalid input, unauthorized access, concurrency, retry and restart scenarios. Real dependency guarantees require real integration evidence; mocks alone cannot establish ordering, replication, consistency or durability.

See [reliability](../docs/reliability.md) for execution/reporting requirements.

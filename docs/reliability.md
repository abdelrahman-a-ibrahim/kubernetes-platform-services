# Reliability and failure verification

Status: verification scenarios planned; no results recorded yet.

## Required scenarios
- Deploy an incompatible chart value and observe reconciliation.
- Remove access to a referenced secret.
- Block an application dependency with network policy.
- Upgrade an add-on with an incompatible CRD version in a disposable cluster.

## Verification protocol
For each implemented scenario, document:
1. Commit, runtime versions, environment and topology.
2. Input workload and the expected invariant.
3. Baseline observations, fault injection and timestamps.
4. Observed errors, duplicate effects or state inconsistencies.
5. Recovery steps and measured time to restore behavior.
6. Resource cleanup and remaining limitations.

A simulator establishes application behavior within its assumptions. Real service ordering, consistency, failover and durability claims require verification against the selected dependencies. Distinguish those results in reports.

## Release evidence
- Fresh-cluster bootstrap is reproducible from the documented inputs.
- Application identity cannot change cluster-scoped resources.
- A failed upgrade has a tested recovery path.
- Dependency checks distinguish missing add-ons from application bugs.

Store concise reports in [verification results](verification/README.md). Targets and illustrative fixture values must not be reported as measurements.

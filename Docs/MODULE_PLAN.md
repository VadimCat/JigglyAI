# Shared module plan

Updated: 2026-10-27.

Reuse the [current catalog](../README.md) first. Engineering rules belong to the shared UnityKnowledge handbook. The entries below are proposed work, not published packages.

## First pilot

Extract presentation operations only after reviewing existing animation and screen-lifecycle implementations.

The module owns operation dependencies, independent lanes, completion, failure and cancellation tied to an owner. The game supplies visuals, grouping, animation assets and intentional input locks. Domain validity and committed state remain outside the scheduler. Keep DI, tween libraries and specific screen architectures optional.

Verify that independent operations overlap, dependent operations keep their order, failure settles waiters, teardown releases resources, and a late callback cannot affect a new session. Accepted domain results must remain correct with delayed or absent presentation. Validate the boundary in a second game with a different mechanic before broader adoption.

## Next candidates

| Capability | Shared responsibility | Game responsibility |
| --- | --- | --- |
| Restore coordination | Participant readiness, compatibility, cancellation and transition to settled presentation | DTOs, save keys, migration, snapshots/journal policy and interrupted-outcome rules |
| Analysis jobs | Cancellation, progress, budgets, cache identity and clear result status | Legal transitions, solver, player policy, scoring, asset selection and repairs |
| Decision flows | Request/result/cancellation lifecycle when an existing screen module needs a common extension | Copy, layout, rewards, SDK calls and outcome policy |

Reuse maintained saves for serialization and storage. Create a restore package only when a second consumer needs more than a small composition adapter. Keep gameplay solvers, generators and scoring in their owning game until another game demonstrates the same domain contract.

## Release rules

Define the smallest stable contract and its owner. Review source permissions and existing package dependencies before moving implementation. Validate focused contract tests and actual Unity integrations, release a versioned module, update the catalog, then validate each consumer's exact pin.

Use existing cheats, parameter tables, input replay and themes where they help the selected consumer. Do not introduce new copies or make unrelated runtime packages depend on those tools. Build requests remain subject to the consuming project's delivery policy.

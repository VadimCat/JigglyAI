# UnityGameModules

Updated: 2026-10-29.

Shared Unity module discovery and development plan. Reuse the maintained module before adding a local equivalent; keep game rules, configuration and adapters in the game.

- [Current module catalog](https://chatgpt.com/space/page_7a8352f8c3b0819199c8721b363af600)
- [Module separation plan](D:/Codex/JigglyAI/Docs/MODULE_PLAN.md)
- [Shared knowledge map](D:/Codex/UnityKnowledge/Docs/KNOWLEDGE_MAP.md)
- [Unity engineering guidance](D:/Codex/UnityKnowledge/README.md)

This project is `D:/Codex/JigglyAI`; it is not an assumed GitHub repository name. `Cheats.git` and `UiSnapshots.git` contain the maintained local cheats and UI screenshot repositories. Other modules may be maintained in their recorded source projects. Read their own APIs and installation instructions before integration.

This repository owns the concise module index and plan. Module code, releases and consumer pins stay with their actual owners.

## Material interaction

`com.ji2.tactile-materials` 1.1.0 is maintained in the [Prototypes package](https://github.com/VadimCat/Prototypes/tree/357d83c855b437b00f6f5cf5308e248700f37f44/Packages/com.ji2.tactile-materials). It reuses the Codex Clean Rush snow, leaf and water core, with opt-in conserved transfers, gate masks, density, checkpoints, brush scaling and material presentation controls. Read its README for defaults, circular containment requirements, upstream provenance, the `com.ji2.reactive` dependency and exact installation. Keep goals, color stacks, authored levels, art direction and input adapters in the consuming game.

## UI screenshots

`com.ji2.ui-snapshots` 0.1.0 (release candidate, [VadimCat/UiSnapshots](https://github.com/VadimCat/UiSnapshots), PR #1; local `D:/Codex/JigglyAI/UiSnapshots.git`) captures Editor-only UI evidence: `Snap.Point` markers compiled out of players, JSON scenarios, viewport × skin matrix runs, reference screenshots (mockups and approved goldens), manifests and before/after reports, a window and `Cli~/ui-snap.ps1`. It reuses `com.ji2.creative-replay` for viewports and replay and `com.ji2.cheats` for cheat steps. Games keep the adapter, game steps, scenarios and references. The usage skill source is `Skills~/ui-snapshots`. Verified consumer: PushColorMerge `agent/ui-snapshots` (pin `3404ce4`).

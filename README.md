# UnityGameModules

Updated: 2026-10-27.

Shared Unity module discovery and development plan. Reuse the maintained module before adding a local equivalent; keep game rules, configuration and adapters in the game.

- [Current module catalog](https://chatgpt.com/space/page_7a8352f8c3b0819199c8721b363af600)
- [Module separation plan](D:/Codex/JigglyAI/Docs/MODULE_PLAN.md)
- [Shared knowledge map](D:/Codex/UnityKnowledge/Docs/KNOWLEDGE_MAP.md)
- [Unity engineering guidance](D:/Codex/UnityKnowledge/README.md)

This project is `D:/Codex/JigglyAI`; it is not an assumed GitHub repository name. `Cheats.git` contains the maintained local cheats repository. Other modules may be maintained in their recorded source projects. Read their own APIs and installation instructions before integration.

This repository owns the concise module index and plan. Module code, releases and consumer pins stay with their actual owners.

## Material interaction

`com.ji2.tactile-materials` 1.0.0 is maintained in the [Prototypes package](https://github.com/VadimCat/Prototypes/tree/0f5f0fdd283255ce8b17f5b174935efb15216e94/Packages/com.ji2.tactile-materials). It reuses the Codex Clean Rush snow, leaf and water core, with opt-in conserved field transfers, gate masks, density and checkpoints. Read its README for the API, upstream provenance, `com.ji2.reactive` dependency and exact installation. Keep goals, color stacks, authored levels and input adapters in the consuming game; do not copy the anthology rules into the module.

# Shared UPM package hosting

Updated: 2026-11-08.

Use the private `VadimCat/JigglyAI` Git repository to distribute shared Unity packages with the same intended audience. Access is granted once to the repository and covers every package and its history. Keep packages with narrower access in their own repositories. Verify both the source access and the consuming team's access before adding a package here.

## Install Cheats 1.1.0

The pilot in `Packages/com.ji2.cheats` contains the exact Git tree of [Cheats 1.1.0](https://github.com/VadimCat/Cheats/tree/c82a0e2c58eab651e9de83ac7b68dc66a83b6127), including Unity asset GUIDs. `VadimCat/Cheats` remains the canonical source during the pilot. Make fixes there and import an approved release here; do not edit the snapshot directly.

1. Configure Git authentication on the developer or CI machine and verify `git ls-remote https://github.com/VadimCat/JigglyAI.git` works without a prompt. Keep credentials in the Git credential helper or CI secret store.
2. Use **Install package from git URL** in Unity Package Manager, or add the entry below to `Packages/manifest.json`. Replace `<release-commit>` with the full commit SHA in **JigglyAI** that contains the package version. Commit `manifest.json` and the generated `packages-lock.json` in the consuming project.

```json
{
  "dependencies": {
    "com.ji2.cheats": "https://github.com/VadimCat/JigglyAI.git?path=/Packages/com.ji2.cheats#<release-commit>"
  }
}
```

When switching an existing consumer, remove its previous installation of the same package before resolving dependencies; an embedded copy takes precedence over the Git dependency. Validate the consumer before switching other projects.

## Add a shared package or version

- Keep each package in `Packages/<package-id>` with `package.json` at that folder's root. Preserve its metadata, license, and release provenance. Keep game code and assets in their owning projects.
- Import a reviewed release and verify the imported package tree against its source. Review the commit and test a clean UPM install before updating consumer pins. Pin the full commit SHA so releases of other packages do not update a consumer implicitly.
- If a package needs another private Git package, add the latter explicitly to the consumer's `Packages/manifest.json`. UPM does not accept Git URLs as dependencies in a package's own `package.json`.

# JigglyAI Unity Package Catalog

JigglyAI lists reusable Unity packages available from public Git repositories. Check each package manifest for the Unity version, dependencies, and compatibility requirements. See its source notices and license terms for permitted use.

## Install a package

1. Open Unity Package Manager and select **Install package from git URL**. Copy the Git URL below. You can also add it to the `dependencies` in `Packages/manifest.json`.
2. Add any required companion Git packages to the same manifest. For example, UI Snapshots uses Cheats and Creative Replay, Gold Currency uses Currency, and Screens uses Camera Source. Install the Unity and third-party dependencies required by each package.
3. Commit `Packages/manifest.json` and Unity's generated `Packages/packages-lock.json`. Keep game code and configuration in the consuming game. When moving from an embedded copy, compare its source and `.meta` files to the target release before replacing it.

## Public packages

The table pins a reviewed revision for each package. UI Snapshots is a release candidate. For an existing game, keep its compatible pin until the game has been validated with an update.

| Package | Purpose | Git URL |
| --- | --- | --- |
| [`com.ji2.ads`](https://github.com/VadimCat/MyUpm/tree/6de7f982743668e9101c9073cfeb88c840f2f954) | Advertising contracts and a development implementation | `https://github.com/VadimCat/MyUpm.git#6de7f982743668e9101c9073cfeb88c840f2f954` |
| [`com.ji2.async-extensions`](https://github.com/VadimCat/com.ji2.async-extensions/tree/4f006ac5801564070e1e0e766b8920c3aa30121e) | UniTask helpers | `https://github.com/VadimCat/com.ji2.async-extensions.git#4f006ac5801564070e1e0e766b8920c3aa30121e` |
| [`com.ji2.buttons`](https://github.com/VadimCat/com.ji2.buttons/tree/e7766f38563806c378171c2ffc4ad94d8de92f8f) | Base button view | `https://github.com/VadimCat/com.ji2.buttons.git#e7766f38563806c378171c2ffc4ad94d8de92f8f` |
| [`com.ji2.camera-source`](https://github.com/VadimCat/CameraSource/tree/724c22a9a1ba2c54da2f637828a1431513775053) | Active camera lookup and change notifications | `https://github.com/VadimCat/CameraSource.git#724c22a9a1ba2c54da2f637828a1431513775053` |
| [`com.ji2.cheats`](https://github.com/VadimCat/Cheats/tree/c82a0e2c58eab651e9de83ac7b68dc66a83b6127) | Command registry, Editor window, and optional runtime panel | `https://github.com/VadimCat/Cheats.git#c82a0e2c58eab651e9de83ac7b68dc66a83b6127` |
| [`com.ji2.creative-replay`](https://github.com/VadimCat/com.ji2.creative-replay/tree/98bf15bed97d6f44e5ff4e28df7a94e0242f72f0) | Editor viewport and recorded input replay | `https://github.com/VadimCat/com.ji2.creative-replay.git#98bf15bed97d6f44e5ff4e28df7a94e0242f72f0` |
| [`com.ji2.currency`](https://github.com/VadimCat/com.ji2.currency/tree/98843fe52a5177dea45635401890ec3d67142dcc) | Currency contracts, registry, and views | `https://github.com/VadimCat/com.ji2.currency.git#98843fe52a5177dea45635401890ec3d67142dcc` |
| [`com.ji2.currency-gold`](https://github.com/VadimCat/com.ji2.currency-gold/tree/45858fbb1f68a0e57139bb352347011e8ec9b75a) | Gold currency implementation | `https://github.com/VadimCat/com.ji2.currency-gold.git#45858fbb1f68a0e57139bb352347011e8ec9b75a` |
| [`com.ji2.currency-lives`](https://github.com/VadimCat/MyUpm/tree/32a85d5149a4759a4283c7c7bafd3d5bce5df3db) | Lives currency and recovery timer | `https://github.com/VadimCat/MyUpm.git#32a85d5149a4759a4283c7c7bafd3d5bce5df3db` |
| [`com.ji2.pause`](https://github.com/VadimCat/com.ji2.pause/tree/043b48b5134484b4983351f12e76e727a5a0e7be) | Pause contracts and time scale control | `https://github.com/VadimCat/com.ji2.pause.git#043b48b5134484b4983351f12e76e727a5a0e7be` |
| [`com.ji2.reactive`](https://github.com/VadimCat/com.ji2.reactive/tree/9e20c445378cf34069ed86c8f89a883abd9d74ef) | Reactive property | `https://github.com/VadimCat/com.ji2.reactive.git#9e20c445378cf34069ed86c8f89a883abd9d74ef` |
| [`com.ji2.saves`](https://github.com/VadimCat/Saves/tree/e832f859f7e84650e8efc9195d38079dc86a52be) | JSON saves, checkpoints, and VContainer bootstrap | `https://github.com/VadimCat/Saves.git#e832f859f7e84650e8efc9195d38079dc86a52be` |
| [`com.ji2.screens`](https://github.com/VadimCat/Screens/tree/f8a8c7ee7ce247a5c47a57ac63ed62711a0c6402) | Screen navigation and base views | `https://github.com/VadimCat/Screens.git#f8a8c7ee7ce247a5c47a57ac63ed62711a0c6402` |
| [`com.ji2.ui-snapshots`](https://github.com/VadimCat/UiSnapshots/tree/3404ce42df6f1b22ca3341c66c5c736ec4c1c846) | UI captures, scenarios, and comparison reports | `https://github.com/VadimCat/UiSnapshots.git#3404ce42df6f1b22ca3341c66c5c736ec4c1c846` |
| [`com.ji2.visual-themes`](https://github.com/VadimCat/com.ji2.visual-themes/tree/0b4cdf0e1334c831a20180b0ac13d39ec5dc27b2) | Theme catalogs and Editor asset variant baking | `https://github.com/VadimCat/com.ji2.visual-themes.git#0b4cdf0e1334c831a20180b0ac13d39ec5dc27b2` |
| [`com.maumau.floating-joystick`](https://github.com/VadimCat/com.maumau.floating-joystick/tree/1533a6cf6c8dcf63c09ede1ef03ac3ff0895c860) | Floating joystick and pointer ownership | `https://github.com/VadimCat/com.maumau.floating-joystick.git#1533a6cf6c8dcf63c09ede1ef03ac3ff0895c860` |
| [`com.maumau.game-parameters`](https://github.com/VadimCat/com.maumau.game-parameters/tree/c7b87d9db2a8c5c0ef0890df748e8daa7c6362e7) | Serialized parameter tables and CSV export in the Editor | `https://github.com/VadimCat/com.maumau.game-parameters.git#c7b87d9db2a8c5c0ef0890df748e8daa7c6362e7` |

Packages hosted in `MyUpm` each have a dedicated release branch. Use the exact Git pin in the table.

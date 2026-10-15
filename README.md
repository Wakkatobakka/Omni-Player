# Omni Player

Your games, together.

Omni Player runs supported mobile games on **Android 11+ / ARM64** through their individual bridges. The built-in catalog covers **24 games / 25 editions** across BREW, DoJa, J2ME, ExEn and Zeebo/BREW.

## Download and play

1. Open this repository's **Releases** section and download **Omni_Player_v0.4.2_PUBLIC.apk**.
2. Install it. Android may ask you to allow installs from your browser or file manager.
3. Open Omni, tap **Load Game**, and select a supported original game download.
4. Tap the game and **Play**.

Existing users can install over Omni to keep their library, bridges and saves.

Game files are supplied by you. Keep multi-file games in their original ZIP/RAR/7z archive. Supported standalone JAR and EXN files also work. Check [supported editions](SUPPORTED_GAMES.txt) when choosing a download.

ExEn prepares its verified platform runtime automatically on first use; connect once, then use the offline cache. The original EXEN-V2 Emulator ZIP can also be supplied for offline setup.

## Add more bridges

Open the menu → **Add finished bridges…** and select a finished bridge APK or checkpoint ZIP. Multiple selections are supported. The bridge stays installed when you remove a game, so its matching original download can be loaded again with the same save location.

## Version 0.4.2

This release retains the accepted compact library, artwork and title controls. It fixes original-download recognition after bridge expansion and automates ExEn setup. The owner accepted this exact build after checking that every game loads and runs.

See [release notes](RELEASE_NOTES.txt), [verification](VERIFICATION.txt) and [supported editions](SUPPORTED_GAMES.txt).

## Source and notices

Download **Omni_Player_v0.4.2_PUBLIC_SOURCE.zip** from the release assets for the complete public build source and third-party component sources/notices. GitHub's automatic “Source code” downloads contain this small repository; use the explicitly named PUBLIC_SOURCE asset to rebuild the player.

[Build instructions](BUILDING.txt) · [Component notices](THIRD_PARTY_NOTICES.txt) · [Bridge import contract](docs/BRIDGE_IMPORT_CONTRACT.md)

Original game executable, audio, level and firmware payloads are not bundled in the public player. Decorative title/icon artwork is retained. Third-party components retain their respective licenses; their notices are included in the corresponding source package.

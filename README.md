# Omni Player

Your games, together.

Omni Player runs supported mobile games on **Android 11+ / ARM64** through their individual bridges. The built-in catalog covers **24 games / 25 editions** across BREW, DoJa, J2ME, ExEn and Zeebo/BREW.

## Download and play

1. Open this repository's **Releases** section and download **Omni_Player_v0.4.2_PUBLIC.apk**.
2. Install it. Android may ask you to allow installs from your browser or file manager.
3. Open Omni, tap **Load Game**, and select a supported original game download.
4. Tap the game and **Play**.

Game files are supplied by you. Keep multi-file games in their original ZIP/RAR/7z archive. Supported standalone JAR and EXN files also work. Check [supported editions](SUPPORTED_GAMES.txt) when choosing a download.

ExEn prepares its verified platform runtime automatically on first use; connect once, then use the offline cache. The original EXEN-V2 Emulator ZIP can also be supplied for offline setup.

## Absolutely Irrelevant for everyone except myself: Adding More Bridges

Omni Player supports importing additional finished game bridges through **Menu → Add finished bridges…**

This feature is intended for compatible bridge APKs or checkpoint ZIPs. It is **not required** to play the games already supported by Omni Player.

Imported bridges remain installed even when their games are removed, allowing the original game files to be loaded again while retaining their existing save locations.

I'm sure you can try feeding random shit into it, but its 9.9/10 it wont play if its not supported and it'll bog up for import history. Honestly this is only here because I forgot to remove this from the public facing portion.


## Version 0.4.2

This release retains the accepted compact library, artwork and title controls. It fixes original-download recognition after bridge expansion and automates ExEn setup. A game having a bridge available does not mean the entire game is playable. These are all still ongoing recoveries unless stated otherwise. This build reflects that after checking that every game loads and runs.

See [release notes](RELEASE_NOTES.txt), [verification](VERIFICATION.txt) and [supported editions](SUPPORTED_GAMES.txt).

> [!IMPORTANT]
> ### 🎮 JUST HERE TO PLAY THE GAMES?
>
> **YOU CAN IGNORE EVERYTHING BELOW THIS LINE.**
>
> Seriously. You don't need to build anything, understand bridge contracts, or touch source code.
>
> Download the APK, supply your supported game files, and enjoy.
>
> Everything below is for developers, contributors, and people who enjoy staring into the technological abyss.


## Source and notices

Download **Omni_Player_v0.4.2_PUBLIC_SOURCE.zip** from the release assets for the complete public build source and third-party component sources/notices. GitHub's automatic “Source code” downloads contain this small repository; use the explicitly named PUBLIC_SOURCE asset to rebuild the player.

[Build instructions](BUILDING.txt) · [Component notices](THIRD_PARTY_NOTICES.txt) · [Bridge import contract](docs/BRIDGE_IMPORT_CONTRACT.md)

Original game executable, audio, level and firmware payloads are not bundled in the public player. Decorative title/icon artwork is retained. Third-party components retain their respective licenses; their notices are included in the corresponding source package.

# Original-download contracts for finished bridges

Omni keeps an installed bridge independently of visible games. Removing a game hides its record; it does not erase the bridge, import fingerprints or saves. Loading the same original edition restores that game's existing record. Current generic bridges retain the `bridge-<package hash>-library` directory across upgrades.

Older APKs with embedded original `.mod`, `.jar` or `.exn` assets can teach their executable fingerprints automatically. The bridge's installed runtime and prepared resources remain available after removal. Shared `imicro3d.mod`/`micro3d.mod` libraries do not identify a title when another executable is present. Supported original fingerprints stay exact; filename matches never authorize a guessed edition.

New bridge builders should include `assets/omni-import.properties`, especially when the APK contains prepared game code instead of the original JAR. This is ordinary UTF-8 Java properties data, not executable setup code:

```properties
schema=1
recognition=<SHA256 of original game executable>
identity=<stable original edition SHA256>
asset.original.jar=<SHA256 of original game executable>
asset.game-data.bin=<SHA256 of required original data>
file.game-data/initial.dat=<SHA256 of required initial data>
```

Replace every placeholder with a lowercase 64-digit SHA256. `recognition` is a comma-separated list of alternative exact source fingerprints, not a filename list. Omit `identity` to use its first fingerprint. `asset.<path>` maps a verified original to the bridge's asset path; `file.<path>` maps a verified original to its isolated files directory. Both mapping groups are optional for a bridge that already carries all prepared resources. Require only actual original inputs: do not require generated DEX/audio, checkpoint metadata, or optional save/config files. Missing-only placement preserves existing saves. Place asset placeholders in prepared-only APKs when the runtime opens those asset names through Android AssetManager.

The finished bridge must already include its Android compatibility code and any prepared resources it needs. This version does not execute arbitrary setup scripts from a checkpoint. A source-only archive is not a finished bridge. APKs lacking both embedded originals and explicit rules remain usable as installed checkpoints but are explicitly reported as lacking original-download rules; Omni does not invent a fingerprint.

Bridge builders must test their real original download: install bridge, remove game, restart Omni, load original again, verify that the runtime and save directory are unchanged. Also test loading originals into the installed bridge after the game directory is absent. Platform support such as ExEn belongs to durable support storage, not a particular visible library row.

Checkpoint recovery accepts only complete entries after ZIP CRC verification and then validates the APK structure/manifest. A damaged tail is reported. It is not treated as a successful recovery of the whole source checkpoint.

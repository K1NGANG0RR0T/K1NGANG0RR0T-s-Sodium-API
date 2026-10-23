# K1NGANG0RR0T's Sodium API
*(fork of Sodium Options API 1.0.10)*

This is a fork of [Sodium Options API](https://github.com/txnimc/SodiumOptionsAPI) **1.0.10** by [toni (txnimc)](https://github.com/txnimc),
updated to work with **Sodium 0.8+ on Minecraft 1.21.1 (NeoForge)** next to Reese's Sodium Options.
All credit for the original mod goes to toni; this fork only removes what Sodium 0.8 broke.

- Original on Modrinth: <https://modrinth.com/project/Es5v4eyq>
- Original on CurseForge: <https://www.curseforge.com/projects/1103431>
- Original source: <https://github.com/txnimc/SodiumOptionsAPI>

## What changed in this fork
Sodium 0.8 replaced its options GUI with a native config API (`ConfigEntryPoint`), so every mixin in the original targeted classes that no longer exist.
This fork removes those mixins and keeps the `toni.sodiumoptionsapi.api` / `util` classes, so mods that depend on Sodium Options API still load.
The legacy events no longer fire; mods should register pages with Sodium's `ConfigEntryPoint`.

Version `1.1.0-k1ng.fork-1.0.10` = shim release 1.1.0, forked from upstream 1.0.10. The mod id is still `sodiumoptionsapi` so dependent mods keep working.

## Requirements
- Minecraft 1.21.1, NeoForge
- Optional: K1NGANG0RR0T's Sodium Options (Reese's fork)

Do not run it alongside the original Sodium Options API; they share the same mod id.

## For mod authors
Use it as a dependency; do not bundle it. Mark `sodiumoptionsapi` as a required dependency in your `neoforge.mods.toml`.

## Building
```
./gradlew build
```
The jar is written to `build/libs/`.

## License
The mod metadata declares LGPL-3.0, but this repository's `LICENSE` is the full GPL-3.0 text, as in upstream. Until the author clarifies, the `LICENSE` file is kept unchanged and this fork's complete source is public at `https://github.com/K1NGANG0RR0T/K1NGANG0RR0T-s-Sodium-API`.

The jar includes MixinSquared 0.2.0 (jar-in-jar) under its own license, plus `licenses/embeddium.txt` and `licenses/rso.txt` for code derived from those projects.

## Issues
Please report problems with this fork here, not to the original author: `<ISSUES LINK>`
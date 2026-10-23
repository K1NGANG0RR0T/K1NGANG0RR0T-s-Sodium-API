## 1.1.0-k1ng.fork-1.0.10 (K1NGANG0RR0T fork)
- Renamed to K1NGANG0RR0T's Sodium API; authors now credit K1NGANG0RR0T (fork) and toni (original author); README and descriptions link the original project.

## 1.1.0 (Sodium 0.8 compatibility shim)
- Sodium 0.8 removed `SodiumOptionsGUI`, `OptionPage`, `OptionGroup` and `OptionImpl` and replaced them with a native config API (`ConfigEntryPoint`). Every mixin in this mod targeted those removed classes (or Reese's Sodium Options internals that were rewritten), so they are removed.
- The `toni.sodiumoptionsapi.api` and `util` classes are kept so mods that depend on Sodium Options API still load. On Sodium 0.8 the legacy events never fire; mods should register pages with Sodium's `ConfigEntryPoint` instead.
- Reese's Sodium Options is now optional (suggested) instead of required.
- Pairs with Reese's Sodium Options builds that only block Sodium Options API `< 1.1.0`.

Port to 1.21.5
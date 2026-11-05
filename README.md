# Permanent Super Engine (EU)

**Version 1.0.1 — OFFLINE ONLY**

Automatically activates the game's original Super Engine for the first local player's kart and keeps its native permanent behavior, including after falling off the track and returning to the road.

This is an unofficial declarative mod for OCTR / CTR Nitro-Fueled PC. It is not a generic speed multiplier, USF patch, invulnerability mod or game executable replacement.

## Online restriction

**The publicly distributed package is restricted to offline play.** Its manifest declares `compatibility.online: "offline-only"`. The compatible mod loader refuses to prepare it when Online is enabled, including through the `BB_ONLINE=1` override.

Turn **Online off** in the launcher before using this mod. This restriction is intentional: network synchronization, server acceptance and server rules have not been tested. Do not interpret successful offline gameplay as online compatibility.

## Download

- [Download version 1.0.1](https://github.com/Majed-allababedi/CTR-Permanent-Super-Engine-EU/releases/download/v1.0.1/permanent-super-engine-eu-1.0.1.zip)
- [SHA-256 checksum](https://github.com/Majed-allababedi/CTR-Permanent-Super-Engine-EU/releases/download/v1.0.1/SHA256SUMS.txt)
- [Release page](https://github.com/Majed-allababedi/CTR-Permanent-Super-Engine-EU/releases/tag/v1.0.1)

## Requirements

- Your own EU game installation: **CUSA14876**, update **01.21**.
- A compatible PC-port launcher supporting schemaVersion 2 mod packages, XML patches and code signatures.
- Tested runtime: **0.8.1**.
- One local human player: primary controller / player ID 0, not a spectator.
- Offline play.

Other game editions, updates, runtimes and split-screen are not established as compatible. Exact code signatures and original-byte hashes remain enforced.

## Installation

1. Download the release ZIP; do not use GitHub's automatic source archive as the installable package.
2. Close the game normally.
3. Place `permanent-super-engine-eu-1.0.1.zip` in the portable installation's `mods` folder. Keep only the intended version of this package there.
4. Open the launcher, reload **Mods** if necessary and enable **Permanent Super Engine (EU)**.
5. Turn **Online off**, then launch the game normally.

Disable the package in Mods and fully relaunch to return to normal behavior. No game executable or archive is replaced. Normal saves continue to be managed by the game and launcher; this package contains no saves or save migration.

## Behavior and fall fix

- Uses the original Super Engine item and permanent-effect behavior.
- Custom automatic activation targets only the selected primary local kart; it does not add this effect to opponents in ordinary races.
- Preserves the original mode-1 behavior rather than changing the global game mode.
- Version 1.0.1 retains the native permanent-effect respawn exception, so falling and normal vehicle recovery remain enabled without deleting this permanent effect.
- Temporary Super Engine items retain their normal cleanup behavior.

Another mod making opponents' Super Engines permanent outside native mode 1 is not covered by the supported combination. Executable write conflicts must be rejected by the loader.

## Verification scope

- Original eight executable payload-fixture tests passed.
- Three native respawn-gate tests passed; the unmodified gate first failed the requested preservation test.
- Actual patch compilation and a local full-selection preflight passed with no overlapping executable writes.
- The owner confirmed that the isolated fall-recovery trial works.
- Read-only observation confirmed the patched gate, one permanent local engine and none on the seven other race participants. The boost handle was null at the sampled instant, so active acceleration at that instant was not independently established.
- These results do not establish every track, weapon combination, other mod, multiplayer scenario or future runtime.

## Repository contents

`permanent-super-engine-eu/` contains the declarative mod manifest, required-loader marker, documentation and executable patch XML. The release ZIP packages that folder for installation.

No game executable, game archive, save, memory dump, private diagnostic log or authentication credential is included. You must provide the game and compatible PC port separately.

Author: **Majed-allababedi**. Game and engine names belong to their respective owners; this project is not affiliated with them.

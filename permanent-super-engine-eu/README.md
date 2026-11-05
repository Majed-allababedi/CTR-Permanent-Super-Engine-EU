# Permanent Super Engine (EU) 1.0.1

Author: Majed-allababedi

Automatically activates the original Super Engine for the first local human kart at race start and enables its native permanent behavior. Other racers retain their normal behavior. This is not a generic speed or USF patch.

Version 1.0.1 retains the native permanent-effect respawn exception after a fall. It does not disable falling or normal vehicle recovery. Temporary Super Engine items keep their original cleanup. Combining this with another mod that makes opponents' engines permanent outside native mode 1 is not covered.

## Supported setup

- EU CUSA14876, game update 01.21.
- Tested on runtime 0.8.1 with one local human player.
- Offline only. The loader rejects online play while this package is enabled.
- Code signatures and fixed-address expected hashes are required; incompatible code is rejected.
- Split-screen is intentionally not enhanced by this version.

## Install and use

Place this ZIP in the portable installation's mods folder. Open the launcher, reload Mods if needed, and enable Permanent Super Engine (EU). Turn Online off before playing. Fully relaunch the game after changing the selection.

Disable the package in Mods to restore normal Super Engine behavior. No game executable or archive is replaced. The base installation uses its normal save location, as it does with other mods; this package contains no save data and performs no save migration of its own.

## Validation

Both executable Line records are identical to the accepted isolated fall-recovery trial. The original eight executable local-fixture tests and three additional native respawn-gate tests passed. The unmodified gate failed the preservation test before the fix. Actual loader compilation passed. The owner confirmed successful fall recovery. Read-only trial observation confirmed the patched gate, one permanent local engine and no engines on the other seven karts; the current boost handle was null at the sampled instant, so active boost at that instant was not independently established. Gameplay acceptance is user-reported, not instrumented proof of every edge case.

Do not enable this gameplay modification online. Compatibility with every third-party mod, future engine update or alternate game executable is not established; the loader must reject conflicting executable writes.

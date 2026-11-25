# KatWork fork of CADCraft

This repository is the KatWork fork of CADCraft (https://github.com/storytold/cadcraft). KatWork builds the app's CLI and web
build from this fork. It carries the patches listed below; everything else is upstream code.

Based on CADCraft by the ArtCraft team (https://github.com/storytold/cadcraft). This build is not an ArtCraft product.

## Fork base

- Fork base (this fork's `main` when the KatWork work started): `0d4b100209990e485891d85c70ff465c8e709156`
- Upstream `storytold/cadcraft` head at that time: `0d4b100209990e485891d85c70ff465c8e709156`

## KatWork patches

| Patch | Upstream PR |
|---|---|
| `chore(katwork): remove the ArtCraft marks` | not proposed upstream (the brand terms let a fork that proposes changes keep the marks; this one is a distributed modified version) |

## The marks

The ArtCraft name, wordmark and logos are trademarks of the ArtCraft Team and are not covered by the app's licence. This fork
removes them, as the brand terms require of a distributed modified version: `docs/brand/` is deleted; links to the ArtCraft
website and its community (Discord), and taglines that present the build as an ArtCraft product, are removed; help links and
`app.links`-style results point to the upstream repository (https://github.com/storytold/cadcraft); README.md, NOTICE and the
About window carry the "Based on" line above as plain text. No new logo is drawn: where a mark was shown, the app's name is shown
as plain text.

`scripts/check-no-marks.sh` (CI job `no-marks` in `.github/workflows/katwork.yml`) fails when a tracked file is a copy of a
fork-base brand file (`scripts/katwork-marks/hashes`), when a line names the marks or the ArtCraft website, when a line names
ArtCraft and is not in `scripts/katwork-marks/allow`, or when an image below is missing from this file.

### What still names ArtCraft, and why (`scripts/katwork-marks/allow`)

- Copyright notices (`LICENSE-MIT`, `NOTICE`, README): required by the licences.
- Application ids `ai.storyteller.cadcraft` and installer paths and folders (`Programs\ArtCraft\...`): kept unchanged; they are
  identifiers, not marks, and changing them would break upgrades of existing installs.
- The Windows version resource's `LegalCopyright` (`apps/cadcraft/build.rs`): a copyright notice, kept as the licences require.
- The nightly channel's messages and tests that name ArtCraft Launcher (`build_flavor.rs`, `profile_root.rs`) and the Flatpak
  permission for the launcher's version folder (`xdg-data/ArtCraft/versions`): they name a separate program and its folders, the
  upstream nightly builds' updater; KatWork builds no nightly.
- The upstream release workflow's secret name (`release.yml`): upstream CI configuration, unchanged; KatWork does not run it.
- The "Based on" line inside code (`crates/ui-egui/src/dialogs.rs`, the About window).

## Image assets of the fork base

Removed (the brand files, deleted with `docs/brand/`):

- `docs/brand/LICENSE-brand.txt`: removed
- `docs/brand/artcraft-logo-white.png`: removed
- `docs/brand/artcraft-logo-white.svg`: removed
- `docs/brand/artcraft-logo.png`: removed
- `docs/brand/artcraft-logo.svg`: removed
- `docs/brand/artcraft-mark-black.png`: removed
- `docs/brand/artcraft-mark-black.svg`: removed
- `docs/brand/artcraft-mark.png`: removed
- `docs/brand/artcraft-mark.svg`: removed

Every other image of the fork base, each kept:

- `assets/app-icon/cadcraft-1024.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/cadcraft-256.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/cadcraft-64.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/cadcraft-macos-512.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/cadcraft-nightly-1024.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/cadcraft-nightly.icns`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/cadcraft-nightly.ico`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/cadcraft-nightly.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/cadcraft.icns`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/cadcraft.ico`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/hicolor/128x128/apps/ai.storyteller.cadcraft.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/hicolor/16x16/apps/ai.storyteller.cadcraft.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/hicolor/24x24/apps/ai.storyteller.cadcraft.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/hicolor/256x256/apps/ai.storyteller.cadcraft.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/hicolor/32x32/apps/ai.storyteller.cadcraft.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/hicolor/48x48/apps/ai.storyteller.cadcraft.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/hicolor/512x512/apps/ai.storyteller.cadcraft.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `assets/app-icon/hicolor/64x64/apps/ai.storyteller.cadcraft.png`: kept: placeholder per `ATTRIBUTION.md` (original artwork by the CADCraft contributors, MIT OR Apache-2.0; no licence file in `assets/app-icon/`)
- `docs/images/ui-apartment.png`: kept: screenshot of the upstream build (viewed: no ArtCraft mark, no Discord button)
- `docs/images/ui-bracket.png`: kept: screenshot of the upstream build (viewed: no ArtCraft mark, no Discord button)
- `docs/images/ui-layout.png`: kept: screenshot of the upstream build (viewed: no ArtCraft mark, no Discord button)
- `packaging/macos/dmg/background.svg`: kept: macOS disk-image background, original artwork (the app name and icon; viewed: no ArtCraft mark)
- `packaging/macos/dmg/background.tiff`: kept: macOS disk-image background, original artwork (the app name and icon; viewed: no ArtCraft mark)

## AutoLISP (not gated)

CADCraft's engine carries an AutoLISP interpreter (`crates/engine/src/lisp/`), reached through the `lisp` and `appload` commands,
`script`, and the command line. Its file functions (`open`, `write-line`, `findfile`) read and write files, within the automation
roots where the process has them. This fork does not compile it out: KatWork's Craft policy keeps it from Kats (those commands
and the command line are forbidden in CADCraft's policy file, and a Kat reaches the app only through that policy). An upstream
issue proposing a build option that leaves the interpreter out is drafted in the fork PR, not opened.

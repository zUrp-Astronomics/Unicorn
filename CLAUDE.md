# CLAUDE.md

Unicorn is a zUrp Astronomics telescope mount controller built on TeenAstro. This repository holds
its board manufacturing files, mechanics, mount configurations and configuration tool — no source
code.

## Stack

- No code is built here. The firmware is TeenAstro's, from the upstream repository
  [`charleslemaire0/TeenAstro`](https://github.com/charleslemaire0/TeenAstro); it does not live in
  this repository.
- `1_Board/` holds three boards — `Main-board/`, `SHC/`, `Brake-module/` — as exports of the CAD
  tool (PDF/PNG schematics, STEP, Gerber zip, BoM and pick-and-place `.xlsx`). The editable board
  design is the [OSHWLab project](https://oshwlab.com/lordzurp/teenastro-redux), not a file here.
- `2_Hardware/` holds the mechanics sources (Fusion 360 `.f3d`, `.step`); `3_3D-Models/` the `.3mf`
  files printed from them.
- `4_Firmware/` holds TeenAstro mount configurations (`.tac`): INI-style text exported by
  TeenAstroConfig, whose header names the tool and firmware version they were made with.
- `5_App/` holds TeenAstroConfig, the TeenAstro configuration tool: a third-party Windows .NET
  binary from the TeenAstro project, under its own licence.

## Conventions

- `README.md`, `9_Assets/`, `LICENSE`, `LICENSE-HARDWARE` and `.github/workflows/zurp-site.yml`
  are the showcase, written by the zUrp Astronomics organisation for all its products at once: a
  project ticket does not touch them.
- The `0_` to `9_` folder layout and the naming of board files are described once, by the
  organisation, in the section « Arborescence et nommage des dépôts produit » (§ 5) of the readme
  kit: https://github.com/zUrp-Astronomics/.github/blob/main/readme-kit/README.md

## Gotchas

- Board files are prefixed `TeenAstro_Redux` — the parent project's name, not `Unicorn`. Main-board
  and SHC files use double underscores around the version
  (`TeenAstro_Redux__SHC_v1.5.2__1_Schematics.pdf`), Brake-module files single ones
  (`TeenAstro_Redux_Brake_Module_v1.1_1_schematics.pdf`): match both when searching.
- Despite its name, `4_Firmware/` contains no firmware, only `.tac` configurations.
- The `.exe` files in `5_App/` and the datasheets in `0_Datasheets/` are third-party material, kept
  as published by their authors.

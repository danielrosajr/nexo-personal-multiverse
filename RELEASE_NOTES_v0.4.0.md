# NEXO v0.4.0 — Cause & Effect

**Release date:** 2026-10-20  
**Tag:** `v0.4.0`  
**Type:** Feature release, backward compatible with v0.3

## Release highlights

NEXO now helps you explore not only *what could have happened*, but also *what other moments might depend on that change*.

**Cause & Effect:** Link earlier events to later ones as a **necessary condition** or an **influence**. The new causal observatory checks how a changed decision might affect subsequent moments, including consequences further down the chain, while distinguishing explicit dependencies from events that simply are not inherited by an alternative branch. No automatic predictions or deletions.

**Timeline divergence:** Choose whether a branch changes the source event or starts after it. Older branches retain their old behavior by default until you make an explicit choice.

**Guided tutorial:** A nine-step walkthrough explains the main timeline, branches, camera navigation, causal linking, presentation mode, exports, and JSON backups.

**Navigation and exports:** The whole left sidebar scrolls on mobile and desktop. Export the full timeline map to PNG, write histories as TXT/Markdown/story PNG, or use **Print / Save as PDF** for a printable narrative.

## Upgrade instructions

1. Export a JSON backup from NEXO v0.3 first.
2. Copy/replace `index.html` in your existing GitHub Pages repository.
3. Add or update README, changelog, security notes, and optional screenshots.
4. Commit and push to `main`, then refresh the existing Pages URL.
5. Open a branch and edit its divergence mode if you want cause-and-effect analysis of an altered source event.

## Suggested Git workflow

**Commit:** `feat: add causal links, guided tour and timeline exports`  
**Tag:** `v0.4.0`  
**Release title:** `NEXO v0.4.0 — Cause & Effect`

## Notes

- All content stays in local browser storage unless exported by the user.
- JSON backup files contain sensitive personal information and must not be pushed to a public repository.
- There is no automated inference, artificial intelligence, database, or cross-device sync in this version.
- PDF export uses the browser print dialog: select *Save as PDF*.
- Tested in a Chromium-based browser for core desktop/mobile flows, legacy backup loading, and export output. Different browser print/canvas limits may apply.

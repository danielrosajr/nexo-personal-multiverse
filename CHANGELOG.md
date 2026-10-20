# Changelog

All notable project changes are listed here. The project uses semantic version tags.

## [0.4.0] — 2026-10-20

### Added

- Author-defined causal links between events, with **necessary** and **influence** relationships.
- Branch divergence mode: *altered source event* vs. *new path after source event*.
- Cause-and-effect observatory: direct and downstream affected events, unlinked non-inherited events, and conflicts involving still-recorded events.
- Optional causal connectors on the SVG timeline map.
- Nine-step guided onboarding that can be replayed.
- Export of the full multiverse map to PNG using Canvas.
- Print-friendly story view, allowing native browser **Save as PDF**.
- Cause metadata in written narratives and exported histories.

### Changed

- Left sidebar now scrolls as a whole, including on mobile; removed the nested timeline list height limit.
- Timeline statistics no longer automatically count people and places from a fork event explicitly marked as changed.
- Story text explains whether an alternate branch changed its origin or began afterward.
- Updated app and image-export version strings.

### Compatibility

- Retains the `nexo-multiverso-v1` local storage key and version-1 JSON backup envelope.
- Older branches default to the conservative **after** divergence mode unless explicitly edited.
- Existing v0.3 backups continue to load; empty causal relationships are added safely.

## [0.3.0] — 2026-10-20

- Timeline terminal states: unknown future, probable death, closed, open.
- Named palettes and editable branch identities.
- TXT, Markdown, and PNG narrative exports.
- GitHub Pages release package and privacy guidance.

## [0.2.0]

- Eras, chapters, timeline personas, observatory statistics, and slideshow mode.

## [0.1.0]

- Interactive personal timeline, branching alternatives, and local JSON backups.

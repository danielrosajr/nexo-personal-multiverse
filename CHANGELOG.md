# Changelog

Changes to NEXO are documented here. Version labels refer to application releases, while the underlying local-storage data format retains backward compatibility.

## [0.3.0] — 2026-10-20

### Added
- Explicit per-branch timeline endings: unknown future (`?`, yellow), probable death (`†`, red), and closed path (`■`, purple).
- Optional ending date and explanatory note, with checks against the branch's last event.
- Distinct ending markers on the map, tooltip/details panels, and minimap indicators.
- Narrative export for the main timeline or a chosen branch in TXT, Markdown, and PNG formats.
- Narrative preview with a configurable cut-off date (today by default), including inherited ancestor events, eras, divergence points, and branch endings.
- Ten labeled color swatches for branch and era customization.

### Changed
- Branches with explicit endings visually stop at their ending marker instead of continuing indefinitely.
- Expanded reality details and sidebar status indicators.
- Updated mobile toolbar layout for the story-export action.
- Added stricter calendar-date validation.

### Compatibility
- Continues using the `nexo-multiverso-v1` local-storage key.
- Continues importing v0.1/v0.2 JSON backups without requiring migration steps.

## [0.2.0] — 2026-10-20

- Added named eras and chapters, editable branch identities, reality statistics, and a slideshow presentation mode.
- Added per-event people and location metadata, inherited-event tracking, and backward-compatible data loading.

## [0.1.0] — 2026-10-20

- Initial single-file interactive personal multiverse timeline prototype with main events, branching realities, timeline navigation, and local JSON backups.

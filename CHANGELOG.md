## [0.11.0] — 2026-10-21

### Added
- A private Fragments memory inbox with fast capture, freeform notes, questions, and tags.
- People/place metadata, multiple optional approximate date precisions, filter and accent-insensitive full-text search.
- Non-destructive conversion from a memory fragment to an ordinary timeline event; explicit unknown-date review step.
- Main-timeline gap prompts and an open-question idea list; neither makes claims about missing memories.
- Bulk note import (one note per line; duplicate detection) and plain-text memory export.
- Fragment persistence in the existing browser-local JSON envelope and backward-compatible migration.
- Fragment step in the guided tour, toolbar/sidebar entry points and mobile responsive view.

### Fixed
- Prevent the first-run tutorial from appearing on top of an already opened Fragment Inbox or event editor.
- Preserve the existing timeline and simulation state on upgrades from v0.10 and prior.

### Security / limitations
- Memory fragments contain potentially sensitive biographical notes; export is not encrypted and uses the browser's localStorage.
- No AI is used to invent memories or guess dates. All dates and memories are user-provided.

# Changelog

## [0.10.0] — 2026-10-21 — Shared Events & Semantic Branch Colors

### Added
- Multi-select event importer between timelines, accessible from toolbar, sidebar, selected event and selected reality.
- Independent copy, synchronized occurrence, and convergence modes with separate behavior.
- Group metadata for relationships between event copies; cyan/purple map links and card badges.
- Optional unlink action, without deleting the occurrence.
- Inline semantic guide for the ten deterministic branch colors, including negative, neutral, romance, friendship and growth suggestions.
- Expanded explanations for formerly ambiguous branch/event form fields.
- Tutorial steps for copying events and semantic colors.

### Changed
- New branch's first event is optional. You can start an empty branch and continue it later.
- Endpoint date/note inputs hide when a branch remains open.
- Events already inherited or previously imported from the same original record are excluded from repeated imports.
- Import rejects event time windows outside a destination branch's valid dates.
- Shared edits synchronize descriptive fields while keeping dates and causal relations independent.
- New event copies never inherit old causal links automatically.

### Compatibility
- Same `localStorage` key (`nexo-multiverso-v1`) and `version: 1` JSON backup structure.
- Older events lacking sharing metadata are normalized without modification to their meaning or date precision.
- No cloud service, database, API key, external AI or build tool required.

---

## [0.9.0] — 2026-10-21 — Approximate Dates & Adaptive Intervals

### Added
- Five event date precisions: exact day, known month, year only, year-to-year interval, and date-to-date interval.
- Distinct styling for uncertain events, with dashed on-map interval segments and endpoint markers.
- Automatic chronological reflow when intermediate events are created within a previously saved date window.
- Explanations distinguishing possible occurrence windows from confirmed duration or exact dates.
- New tutorial step for dates with uncertainty and a sample overlapping interval in the fictional demo.

### Improved
- Moved the date precision picker directly after the event title in the editor.
- Continued-event date suggestions now follow the **end** of an uncertain interval instead of its earliest possible date.
- Text, Markdown, PDF/print, and PNG story exports show approximate intervals rather than presenting fictional exact days.
- Map PNG includes dashed date-range overlays.
- Causal links can only be assigned when the cause is earlier than the effect without ambiguous overlap; statistics require the possible interval to have ended.
- New branches originating from uncertain events use the latest possible date as a conservative temporal boundary.

### Backward compatibility
- Legacy v0.8 and earlier events without `time` metadata remain exact-date events.
- Data continues using the `nexo-multiverso-v1` localStorage key and the v1 JSON backup envelope.
- No database or dependency migration.

---

## [0.8.0] — 2026-10-20

### Added
- Toggleable narrative plausibility view with per-event and per-branch percentages and gradient coloring.
- Formula panel with adjustable weights and a clear fictional-index disclaimer.
- Editable mild/moderate/radical divergence impacts.
- Compatible JSON fields `plausibility` and `branches[].impact`.
- Narrative-index PNG map export and guided tutorial step.

### Changed
- Browser-only calculations; no AI or cloud API.
- Branch comparisons based only on ancestor forks and hypothetical events in the selected path; sibling branches are not treated as exhaustive or equiprobable.
- Mobile panel placement and toggle accessibility.

### Compatibility
- Preserves existing v0.7 and earlier timeline data, events, causes, eras, simulations, and export flows.

---

## [0.7.0] — 2026-10-20 — Timeline Continuation

### Added
- **Continue this timeline** action on event details (same branch, not a new variant).
- Quick `+` action directly on event cards; touch-visible and keyboard-focusable.
- **Continue from latest event** command in the timeline details panel.
- Contextual editor banner identifying the originating event and timeline.
- Default date one day after the reference event, with editable date and boundary checks.
- **Save and create next** button for successive event entry.
- Condensed local-classifier presentation during event continuation; expand for full options.
- Guided-tutorial step explaining event continuations.

### Changed
- Events with identical dates maintain narrative insertion order, making backfilled stories easier to browse.
- Newly created events are centered in the map after saving.
- Continued events cannot inadvertently move to another branch; the line ID is fixed for the continuation flow.

### Preserved
- Existing `localStorage` key; v0.6 and earlier JSON backups load as before.
- All prior branches, eras, relationships, simulation experiments, and exports.

---

## [0.6.0] — Smart Event Classification

### Added
- Offline, rule-based classification suggestions while typing an event title and description (Brazilian Portuguese).
- Plain-language reasons and alternative category suggestions.
- New **Milestone** event type, distinct from personal achievements.
- Optional automatic application; manual overrides disable the auto-update.
- `typeSource` metadata for newly saved event records.
- An additional guided-tour step describing classification.

### Maintained
- No AI requests, API keys, backend, account or database.
- Data compatibility with v0.5 and earlier; no automatic reclassification of prior events.
- Reality Simulator, causal linking, branches, eras, stories, PNG/PDF exports and JSON backups.

### Limitations
- Heuristics are intentionally simple and can misclassify unfamiliar phrases. They do not predict the future or infer personal meaning reliably.


All notable changes to NEXO are documented here. Releases follow Semantic Versioning.

## [0.5.0] — 2026-10-20

### Added
- Interactive **Reality Simulator** with independent saved experiments for alternative branches.
- Guided evaluation of potentially affected events, with four author-defined outcomes and explanations.
- Automatic causal-chain warning when another event was marked as absent in an experiment.
- Projected chronological story combining inherited records, variant events, assessed consequences, and user-created hypothetical scenes.
- Multiple experiments per variant; duplicate and delete individual experiments safely.
- Simulator report exports (clipboard, Markdown, TXT, browser print to PDF).
- New tutorial step about the simulator and mobile collapsible simulator settings.
- Backward-compatible optional `simulations` collection in local JSON backups.

### Fixed
- Replaced full-screen guided-tour blur with an accurately positioned, transparent spotlight and four dimming regions.
- Corrected spotlight positioning when the mobile sidebar animates open.
- Existing alternate events already on the path are updated in scenario preview rather than shown twice.

## [0.4.0] — 2026-10-20

### Added
- Necessary and influential causal links between earlier and later events.
- Cause-and-effect observatory and optional visual causal connections.
- Guided tour and PNG export of the multiverse map.
- Print/Save as PDF story output.

### Fixed
- Sidebar scrolling on mobile and desktop.

## [0.3.0]

- Named branch endings, fixed color palette, narrative story exports to TXT/Markdown/PNG.

## [0.2.0]

- Personas, eras and chapters, timeline statistics, animated slideshow, ancestor-path inheritance.

## [0.1.0]

- Main and alternate visual timelines, nested branches, event editor, local storage, JSON backup.

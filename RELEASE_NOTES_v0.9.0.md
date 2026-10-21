# NEXO v0.9.0 — Approximate Dates & Adaptive Timeline Ranges

**Release date:** 2026-10-21  
**Tag:** `v0.9.0`

## Highlights

NEXO no longer requires you to remember an exact day. Save life events with a month, a year, a year-to-year window, or an exact-date interval. The timeline uses dashed visual spans and automatically reorganizes its temporal landmarks as you add events within those windows.

### Features

- Date editor with five precision modes: exact day; month/year; year only; year range; full date range.
- Visible, interactive event cards explicitly labeled when the date is approximate.
- Automatically reorganizing time axis and dashed interval visualization with visible end boundaries.
- Accurate narrative and map exports that preserve uncertainty.
- Continuation suggestions based on the end of an uncertain period.
- Conservative handling of overlapping periods in causality, branch origin, and statistics.
- New tutorial step and a fictional sample interval.
- Mobile form layout improvements; the date picker is now immediately after the title.

### Compatibility

Reads v0.8 and earlier JSON histories without changes to their recorded dates, with an optional `events[].time` metadata object for new dates. Uses the original `localStorage` key and runs on GitHub Pages without external services.

### Technical notes

Uncertain events are positioned by *earliest possible occurrence* for drawing purposes only; their intervals extend to *latest possible occurrence*. Positions on the axis are **not evidence of sequence or causality** when periods overlap.

### Upgrade

Export a backup JSON before updating. Replace the site's root `index.html`, update docs/assets, and keep your existing GitHub Pages URL to preserve local browser data.

**Suggested commit:**

```text
feat: support approximate event dates and adaptive time ranges
```

**Suggested tag:** `v0.9.0`  
**Release title:** `NEXO v0.9.0 — Approximate Dates & Adaptive Timeline Ranges`

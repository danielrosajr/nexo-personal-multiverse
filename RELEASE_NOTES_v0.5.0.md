# NEXO v0.5.0 — Reality Simulator

## Highlights

NEXO now has a **Reality Simulator**: a private, interactive laboratory for exploring consequences of hypothetical life decisions without rewriting the original timeline.

- Create multiple named, independently saved experiments for each alternate reality.
- Review causal consequences of an altered fork and mark outcomes as unknown, unchanged, absent, or different.
- Write your own explanations and propose additional events in a projected chronological story.
- Export a complete experiment to TXT/Markdown, copy its text, or print it to PDF.
- Keep all experiments in the existing portable JSON backup.
- Guided-tour spotlight no longer blurs the entire app or loses its position while the mobile sidebar animates.
- Compact scenario configuration on mobile devices.

## Critical interpretation note

NEXO does not make reliable predictions about human lives. All causal dependencies and narrative outcomes are hypothetical and entered by the author. The app has no generative-AI, remote model, or analytics integration.

## Deployment

Copy `index.html` and the additional project files to the repository root. Retain the current Pages URL to keep browser-local data. Before deployment, export a JSON backup of any personal timelines.

**Tag:** `v0.5.0`  
**Suggested repository:** `nexo-personal-multiverse`  
**Commit:** `feat: add reality simulator and fix guided tour spotlight`

## Known limitations

- No cloud synchronization or login; local browser storage only.
- Experiments do not mutate the source timeline, and there is no automatic “promote result to branch” feature yet.
- PDF is created via the browser print dialog, not a separate server-rendered PDF download.
- Effect chains are computed from manually authored relationships and can be incomplete.
- Large histories may be slower to browse, print, or export as PNG.

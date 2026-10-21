# NEXO v0.8.0 — Narrative Plausibility Map

## Highlights

**Switch the multiverse into a heatmap of hypothetical paths.** NEXO v0.8.0 adds a narrative proximity index designed for exploring possible lives visually while maintaining a clear boundary between facts and imagination.

- New toolbar toggle: **◉ Mapa de plausibilidade**.
- Event cards change into prominent percentage cards, from green through amber to red; branch routes and sidebar indicators adopt the same palette.
- New comparison panel: rank timelines, inspect fork depth, elapsed years and hypothetical event count, and jump to a timeline.
- Editable sliders for fork penalty, yearly narrative distance and hypothetical-event discount; restore defaults anytime.
- Set each alternate reality to **mild, moderate or radical divergence** in its existing Edit dialog.
- Export the complete map as a PNG while this mode is active, including the index display.
- Added a guided-tour step; preserved timeline continuation, causality, simulations, slideshow, statistics, eras and backups.
- Continued compatibility with v0.7 data and older NEXO backups. New metadata defaults safely.

## Important interpretation

**The percentages are fictional, user-adjustable narrative indexes, not scientifically estimated probabilities.** The model does not predict death, criminal involvement, safety or personal life outcomes. More branches or years merely change a storytelling score. The main timeline's `100%` means “recorded history,” not confidence in a forecast. See [`FORMULA.md`](FORMULA.md).

## Deploy / upgrade

1. Privately export JSON from your current NEXO version.
2. Replace GitHub Pages root `index.html` and upload documentation/assets in this archive.
3. Publish with the same site URL so your browser's local data remains available.
4. Create tag: **`v0.8.0`**. Title: **`NEXO v0.8.0 — Narrative Plausibility Map`**.

Suggested commit:

```text
feat: add narrative plausibility map and branching index
```

No server, API key, or database required.

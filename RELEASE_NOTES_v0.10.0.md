# NEXO v0.10.0 — Shared Events & Semantic Branch Colors

This release lets the same important life event appear across alternative timelines without forcing all subsequent events to diverge.

### Highlights
- **Cross-timeline event transfer:** import multiple events from one timeline to another, or copy directly from a selected event.
- **Three relationship modes:** independent duplicate, synchronized occurrence, or convergence; a dashed visual bridge highlights shared/convergent records.
- **Safe chronology and deduplication:** events inherited from a common past, already copied from the same source, or outside a destination branch's lifespan are not importable.
- **Editable linked events:** shared title, classification, description, people and place stay in sync; date and causality remain branch-specific. Unlink without losing a saved event.
- **Semantic branch-color guide:** optional suggested meanings for ten colors (including danger, romance, neutrality, renewal and distance).
- **Friendlier forms:** explanations for descriptions, variant status, ending dates and ending notes. New variants no longer require a placeholder first event.
- **Tutorial update** and **v0.9 backup compatibility**.

### Upgrade
1. Export a private JSON backup from your old version.
2. Replace `index.html`, then update the documentation and `assets/` files.
3. Keep the same GitHub Pages URL to preserve browser-local records; import the backup if the browser data is missing.
4. Create tag `v0.10.0` on the `main` branch.

### Technical details
- Pure HTML/CSS/JavaScript; no build process, cloud database or API key.
- Additional optional event fields: `copiedFromId`, `sharedGroupId`, `convergenceGroupId`.
- Existing `localStorage` key: `nexo-multiverso-v1`.
- Event causal dependencies are intentionally **not** cloned into a destination reality.

### Important limitations
NEXO is a personal narrative tool, not a statistical or scientific forecaster. Color meanings and probability-like indices are illustrative. Private histories remain stored only in the browser unless users export backups; exported files are not encrypted.

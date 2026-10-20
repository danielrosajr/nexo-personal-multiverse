# NEXO v0.3.0 — Endings & Story Export

**Release type:** feature update (pre-1.0)

## Highlights

### Timelines can finally stop

An alternative reality may now end with a **yellow question mark** (unknown future), a **red dagger** (hypothetical probable death), or a **purple square** (closed scenario). Markers are visual, editable, and accompanied by optional dates and notes. Open paths remain unchanged.

### Share the story of any reality

Choose a reality, select a cut-off date, and export a chronologically ordered narrative as **TXT**, **Markdown**, or a shareable **PNG**. Stories include only recorded ancestor events up to each divergence, followed by the selected branch's events, eras, and final status. Nothing is invented automatically.

### Color picking is easier

Branch and chapter editors now offer ten named colors, including blue, purple, yellow, and red, rather than an RGB picker.

## Upgrade notes

1. **Export a JSON backup from your current NEXO installation before upgrading.**
2. Replace your existing `index.html` with the one in this release and add the documentation files as desired.
3. If you are using GitHub Pages, wait for the latest commit to deploy, then refresh the page.
4. Your existing records should load from the same browser origin automatically. If changing domains or devices, use **Import** with your JSON backup.

**Data compatibility:** Existing v0.1/v0.2 backups are supported. The application continues using the `nexo-multiverso-v1` local-storage key. New branch endings default to "open" for imported older data.

**Privacy:** Personal records remain in browser storage. Do not upload your private backups or narrative exports to a public GitHub repository.

## Known limits

This is a storytelling and mapping tool, not a prediction engine. There is no AI-based outcome simulation or cloud sync. Very long stories may exceed the single-image PNG limit; use TXT/Markdown in that case.

## GitHub release details

- **Tag:** `v0.3.0`
- **Release title:** `NEXO v0.3.0 — Endings & Story Export`
- **Suggested commit:** `feat: add terminal timeline markers and narrative exports`
- **Asset:** `nexo-v0.3.0-github-pages.zip`

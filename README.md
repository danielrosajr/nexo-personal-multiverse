# NEXO — Your Personal Multiverse

**An interactive timeline of real memories, divergent histories, and personal “what if?” scenarios.** NEXO runs as a single static HTML file, with no external AI, backend, or required cloud account.

**Release:** `0.10.0` · **Git tag:** `v0.10.0` · **Hosting:** GitHub Pages or any static file host · **Language:** Brazilian Portuguese.

![Cross-timeline import dialog](assets/shared-events-importer.png)

## New in v0.10 — Shared Events & Semantic Branch Colors

### Three ways to bring an event into another reality

Open **Trazer eventos** from the toolbar/sidebar, or select an event and choose **Copiar / compartilhar com outra linha**. Choose a source timeline, a destination timeline, one or more events, and one import behavior:

| Behavior | What it means | What happens when edited |
|---|---|---|
| **Independent copy** | Similar event occurs in the destination; no permanent shared record | All changes remain local to that copy |
| **Same event / shared** | The event is considered to have occurred in both realities | Title, type, description, people and place stay synchronized between linked records; **dates and causal dependencies remain independent** |
| **Convergence** | Different paths reach similar outcomes | Independent event details, but a recorded and visually displayed convergence link |

The timeline draws **cyan dashed links** for shared occurrences and **purple dotted links** for convergences. Event cards carry corresponding labels. You can unlink an occurrence from its details panel without deleting it. Copies and links are represented by optional metadata (`copiedFromId`, `sharedGroupId`, `convergenceGroupId`) in the usual event records.

![Timeline after creating a convergence](assets/linked-events-map.png)

**Safety and chronology:**

- The app automatically excludes events already inherited at the divergence point or previously imported from the same source (root event ID).
- A destination branch only accepts events whose entire known/possible occurrence window falls **after its origin** and, when there is an explicit ending date, **before its ending**. Uncertain dates with overlapping windows cannot be placed confidently across the boundary and are excluded.
- Original event records are never removed by copying/importing.
- New copies **do not copy causal links**, since the causal conditions in an alternative reality may differ. Add the destination's causal dependencies manually if appropriate.
- Syncing a shared event edits common descriptive fields in its linked copies; this is an intentional **bidirectional** effect. Unlink first if you want independent descriptions. An event's place/person details are potentially sensitive.
- Importing between timelines is an authoring operation; it does **not** calculate a future probability or establish that the event was inevitable.

### Semantic color guide

The branch editor now includes a **Guide to colors**, with a named fixed palette and optional interpretations:

| Color | Narrative suggestion |
|---|---|
| Ocean blue | Neutral alternatives / ordinary life |
| Royal blue | Learning, plans, opportunity |
| Purple | Identity, introspection, mystery |
| Red | Adversity, loss, danger or negative paths |
| Yellow | Uncertainty, decisions, open possibilities |
| Green | Achievement, healing, personal growth |
| Pink | Love, romance and dating |
| Orange | Adventure, major changes, impulsiveness |
| Turquoise | Friendship, family and support |
| Lunar gray | Distance, colder periods, solitude or uncertain tone |

These color meanings are **suggestions only**, never judgments or predictions. Branch color does not affect calculated narrative plausibility, terminal state, or event classification.

![Color guide inside the branch editor](assets/branch-color-guide.png)

### Friendlier editor forms

Inline help now explains **Event description and repercussions**, **Description of this alternate reality**, **Current branch state**, **Endpoint date**, and **Endpoint note**. Endpoint date/note are only displayed for closed/unknown/hypothetical-death branches. **First event of this variant is now optional**; leave it blank and use **Continue this timeline** later.

The guided tutorial now includes importing shared events and semantic colors.

## Other features retained

- Five supported event date precisions: exact day, month/year, year, between years, between dates. Uncertain time windows are displayed as dashed spans without inventing a specific day.
- Chronological reflow, same-line continuation, named eras, personas, endings and local event categorization suggestions.
- Explicit cause-and-effect relations, simulator experiments, narrative plausibility view (illustrative only), story slideshow and statistics.
- PNG exports of the map and written stories, TXT/Markdown story exports, print-to-PDF and full JSON backup/restore.

See [FORMULA.md](FORMULA.md) for limitations of the narrative plausibility index.

## Installation / GitHub Pages

1. Download and extract the release archive. Upload its **contents** (not the outer folder) into the root of your GitHub repository, including `index.html`, `README.md`, the release docs, and `assets/`.
2. In GitHub: **Settings → Pages → Deploy from a branch**, select `main` and `/ (root)`. GitHub Pages will serve the root `index.html`.
3. Suggested repository name: `nexo-personal-multiverse`. Typical URL: `https://YOUR-USERNAME.github.io/nexo-personal-multiverse/`.
4. Alternatively, open the `index.html` file directly in a compatible browser. Storage behavior depends on the browser and page origin.

## Upgrading from v0.9.0 or earlier

1. Open your existing app and **export a JSON backup**, storing it privately and outside public source control.
2. Replace the root `index.html` and refresh your documentation/assets.
3. Keep the **same Pages origin/URL** where possible: browser-local data is tied to the origin, not to your GitHub account.
4. Refresh and verify existing events/branches/eras/simulations. If necessary, restore using **Import JSON**. An existing `version:1` data envelope is supported.
5. Create tag `v0.10.0` and a release titled **NEXO v0.10.0 — Shared Events & Semantic Branch Colors**.

Suggested commit: `feat: add cross-timeline event sharing and semantic branch color guide`

## Privacy and known limitations

NEXO saves history to browser `localStorage` under the existing key `nexo-multiverso-v1`. There is no automatic device synchronization, encrypted cloud backup, account login, or server-side recovery. Clearing browser storage can erase personal data; use JSON backups regularly. Backups, narratives and images are **not encrypted**. Never upload real personal history exports or API credentials to a public repository. Read [SECURITY.md](SECURITY.md).

The app is a personal storytelling and reflection tool, **not** a system for predicting death, crime, relationships or future events. The narrative plausibility percentage is illustrative, not a measured probability. A branch's red color also does not imply any factual likelihood of harm.

## Project and attribution

NEXO is a personal software experiment, not affiliated with Marvel or any entertainment franchise. No reuse license has been granted by default; add a license when you decide how other developers may reuse the source.

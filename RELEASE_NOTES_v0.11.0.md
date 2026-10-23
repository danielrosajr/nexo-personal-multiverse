# NEXO v0.11.0 — Fragments: Memory Inbox

The new **Fragments** workspace lets you collect memories before you know exactly where they belong in your timeline.

## Highlights

- **One-click capture:** save a memory in seconds, without choosing a date, timeline or type.
- **Memory Inbox:** search, filter, tag and organize fragments with people, places, approximate dates and open questions.
- **Event conversion:** open the standard timeline event editor with a fragment prefilled; keep the original memory intact, and link both records.
- **Unknown-date safety:** no date is inferred. The event editor asks you to review the proposed date before conversion of an undated note.
- **Story gaps:** highlight gaps in the recorded main timeline and provide optional reflection prompts, without asserting that a memory exists in those gaps.
- **Bulk import and export:** paste up to 100 single-line notes at once; export the inbox as TXT, and preserve all notes in JSON backups.
- **Tutorial race fix:** the first-use tutorial won't overlay an existing editor or inbox.

## Installation / upgrade

1. **Back up your current NEXO data in JSON** before changing the site.
2. Replace the root `index.html` using this release archive; upload the included documentation and `assets/` folder.
3. Keep the same GitHub Pages URL where possible to retain browser-local data.
4. Reload, open `◈ Fragmentos`, and verify your existing events and branches.
5. Create the Git tag `v0.11.0` and GitHub release **NEXO v0.11.0 — Fragments: Memory Inbox**.

**Suggested commit:** `feat: add fragments memory inbox and guided event conversion`

## Technical notes

- No backend, external API, AI key or build step is needed.
- The existing `nexo-multiverso-v1` localStorage key is unchanged.
- An optional `fragments` array is added to the persisted JSON data.
- Fragment → event reference is stored as `eventId`; event → fragment reference is `sourceFragmentId`.
- Old backups with no `fragments` key remain supported by migration.
- Notes, exported narratives and backups may contain sensitive personal data and are **not encrypted**.

## Known limitations

Local storage is device/browser specific and can be cleared. There is no cloud sync or recovery from accidental deletion without a private backup. Suggested reflection questions are generic prompts, not evidence about a person's memory or history.

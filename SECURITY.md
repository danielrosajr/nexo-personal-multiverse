# Security and privacy

NEXO is a static, client-side web app. It currently has no backend, third-party sign-in, or user accounts.

## Personal information

A timeline may reveal names, relationships, places, memories, hypothetical events, and other highly sensitive personal information. Store backups on a device or drive you trust. JSON, TXT, Markdown, and PNG exports are **not encrypted**.

## Public repositories

**Never publish your JSON backups, personal timeline exports, or production database credentials in a public GitHub repository.** The included `.gitignore` provides basic protection for common NEXO export names, but GitHub's web upload can still publish files if manually selected. Review every file before committing.

## Browser data

NEXO relies on `localStorage`. Users can lose records when site data is cleared or a browser profile is replaced. Take JSON backups regularly. The current product provides no automatic encrypted backup, account recovery, or cloud sync.

## Safe deployments

Static GitHub Pages deployment requires no embedded API key or secret. Avoid adding third-party scripts that could access page content and local storage.

## Reporting issues

If you encounter a security concern, avoid sharing real personal timeline data in public bug reports. Reproduce issues using fictional examples and remove identifying information from screenshots and logs.

## Version 0.5 experiment privacy

The `simulations` collection is stored in the same browser-local JSON blob as the original personal timeline. The simulator does not call external services. Causal assumptions and exported narratives should be treated as personal data; store backups securely and do not commit them to a public repository.

## Version 0.8 narrative indexes

The map percentage is deliberately illustrative and must never be interpreted as a scientific likelihood or as a prediction of violence, mortality, crime, or any real-world outcome.

## Version 0.9 date precision metadata

Approximate dates are stored in the same locally saved history. Although an event may have an imprecise timestamp, its title, people, description, and place may still be sensitive. The app does not transmit these details to an AI provider or an external database.

## Version 0.10 shared occurrences

Linked events can propagate edits to text, people and places across different variants *on the same device and within the same browser dataset*. Links do not publish or transmit data. Check whether a shared occurrence should retain the same personal details in each story before enabling synchronization.

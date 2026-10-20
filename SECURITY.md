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

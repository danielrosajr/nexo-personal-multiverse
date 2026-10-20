# Security and privacy

NEXO is a personal timeline application that may contain highly sensitive biographical details.

- All application timeline data stays in the browser's `localStorage`; there is no NEXO backend or automatic sync.
- Local storage is **not encrypted**. Avoid entering private information on shared or untrusted devices.
- Data can be lost when browser storage is cleared or when switching the site origin. Export JSON backups regularly.
- GitHub Pages publishes the app files but does not automatically receive your `localStorage` data. Never put real-life backups or exported stories in a public code repository.
- Keep your browser and device updated, and avoid installing untrusted extensions that could access page content.
- No authentication or access-control system is included. If you add cloud storage, implement authenticated access, secure storage, encryption, and appropriate privacy controls before using it for personal information.

To report a vulnerability, contact the repository maintainer privately rather than posting personal data in a public issue.

# CaseDesk core: scope

Document date: 2026-11-18. This scope applies to the exact release candidate identified in the [catalogue](README.md). It describes the supplied core and its limits. Configuration, hosting, integrations and additional development are included only when specified in your written order.

## Included core

- Online incident intake and linked case workflows, role/group/field access controls, review, versions, audit history and evidence handling.
- Controlled document issuance, retained versions, correction/withdrawal and selected-version disclosure with recorded removal reasons.
- Filtered aggregate reports and audit exports, including bounded XLSX output. Saved definitions, fixed-date-range scheduling and results require the explicitly initialized optional sidecar and current-owner authorization. They are not forecasting or rolling-period analytics.
- Internal point-location GeoJSON export and an SVG point view without public tiles, external geocoding or routing. Coordinate import is a bounded service capability; no browser file-import workflow is promised here. This is not ArcGIS integration, polygon analysis or route planning.
- Limited offline incident drafting: a previously prepared, hash-checked static shell and encrypted local outbox, with prior online authorization, bounded session/continuation validity and passphrase unlock. Synchronization requires connection and current server authorization. Capture/sync are limited by the supplied implementation, not a promise of unlimited storage or duration.

## Important limits

Offline scope does not include cold/offline login, existing-record browsing/editing, evidence/media capture, GIS, reports, background synchronization or a native mobile application. Only the allowlisted static shell is cached, not authenticated API responses or existing records. Shared-device passphrase encryption is not a separate cryptographic vault for each user. Offline drafting cannot observe server-side revocation while disconnected; continuation expires locally and server authorization is checked on synchronization. Browser storage loss or a lost passphrase can prevent recovery.

Reports can refuse the entire request with 403 for inaccessible current/history data or 409 for exceeded history budgets. They must not return fabricated zeroes or silently partial aggregates. Broad full-volume JSON reporting is unavailable; narrow the filters. XLSX output is bounded aggregate/audit export, not workbook import, PDF export or a guarantee of compatibility with every spreadsheet reader. The final supplied limits and failure behavior govern.

No hosted account, managed database, TLS service, production deployment, guaranteed response time, production capacity, service-level agreement, jurisdictional compliance, geographic hosting assurance, certification, customer installation or native-platform verification is included by this catalogue. External integrations and specialized workflows require separate scope. No blanket security or spreadsheet-interoperability claim is made.

Backup utilities and operational examples do not establish paired recovery of the core database and optional saved-report sidecar, disaster recovery or an accepted retention policy. The separate installation-fence/recovery customization is not included.

Request the exact release scope before selecting an installation or service arrangement.

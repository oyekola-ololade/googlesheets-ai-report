# Template Status & Verification

**Classification:** Configurable n8n template asset — not a verified production deployment.

The workflow export and documentation are inspectable template evidence. They are not proof of a configured live reporting pipeline, production reliability, SLA, ROI, or client outcome.

## Verification gate
1. Parse/import into a clean current n8n instance.
2. Inspect all connections, expressions, branches, aggregations, and Code nodes.
3. Replace placeholder Google Sheets, model, report destination, webhook, URL, credential, and resource IDs.
4. Confirm current Google/model API requirements.
5. Run representative normal/empty/malformed datasets plus provider-failure cases.
6. Verify report calculations, generated summaries, and output destination before recording the test date/result.

## Security
Never commit API keys, OAuth secrets, private Sheet IDs, sensitive business datasets, or production data. Use synthetic spreadsheets and fresh test credentials.

## Change record
- **2026-09-03:** Added repository verification/security/status control. No workflow-logic change or runtime pass is implied.

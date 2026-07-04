# Canonical Database

These CSV files are the authoritative structured records for Atlas OS. Specialist agents never write them directly. They create validated delta files inside their intelligence domains; Atlas CEO reviews and promotes accepted changes.

Rules:

- Stable IDs are never reused.
- Dates use YYYY-MM-DD.
- Missing facts are `UNKNOWN`.
- Multiple URLs use semicolon-separated values.
- Status values use GO, WATCH or NO-GO where applicable.
- Every record includes source URLs and verification metadata.


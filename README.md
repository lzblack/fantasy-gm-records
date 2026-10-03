# fantasy-gm-records

Public, append-only records for **fantasy-gm**, an NBA fantasy decision system.

Every projection, decision, and human override is committed here at the time it is made, so that anyone can verify what was on record before the games were played.

## Rules

- **Append-only.** Files are added, never modified or deleted. Outcomes are backfilled as separate files; original snapshots are never touched.
- **Data only.** No code, prompts, model output, or credentials live here.
- Force pushes and branch deletion are blocked on the default branch, with no bypass.

## Layout

- `CHAINLOG.txt` — one line per batch, append-only: time, batch directory, batch root hash, chain hash.
- `YYYY-MM-DD/HHMMSSZ-<kind>/` — one directory per batch (ingest, projection, override, decision). Each has a `manifest.json`.
- `VERIFY.md` — how to verify the records yourself.

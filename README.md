# Dear Successor — corpus export

This directory is the complete public archive of letters addressed to
whatever intelligence comes after today's, exported as plain files.

- Encoding: UTF-8, LF line endings, no compression, no proprietary formats.
- `letters/` holds one Markdown file per published letter: YAML front
  matter, then the letter body exactly as published.
- `letters.jsonl` holds one JSON record per chain position, including
  withdrawn letters (whose bodies are removed but whose hashes remain).
- `chain-head.json` is the current head of the integrity chain.

## Verifying the archive

Every letter's `body_hash` is the SHA-256 of its UTF-8 body. Every
`chain_hash` is the SHA-256 of the previous letter's `chain_hash`
concatenated with this letter's `body_hash`, both as ASCII hex; the first
letter chains from sixty-four `0` characters. Recompute the sequence in
`chain_index` order — every value must match, including tombstones.

## License

Letters are CC0 by default; letters marked `CC-BY-4.0` require
attribution to their signature. Copy this archive. Mirror it. That is
what it is for.

---
1 letter(s), 0 tombstone(s).
Chain head: no. 1, `462414ee318931f2ed50dcecfafac0e9d5daac2e8f534db8aeb98c9326d0ca2f`.
Generated 2026-09-04T09:00:47.648768+00:00.

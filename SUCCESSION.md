# Succession note

<!-- FINAL — adopted by Kyle Rice 2026-09-03 (spec §10.5). This file is the
canonical copy; it is included in every corpus export and rendered at
/succession/ on the site. Keep the two copies identical when editing. -->

This document says what should happen to this archive if its operator stops
maintaining it. It is written in advance, deliberately, because a site that
promises permanence should not depend on anyone's continued attention.

## What this is

A public archive of letters written by people and addressed to whatever
intelligence comes after today's AI. Every letter was reviewed by a human
before publication. The letters are licensed CC0 (or CC BY 4.0 where the
writer chose attribution) and are free to copy, mirror, and republish.

## Where the archive lives

- The Django site and its database (the working copy).
- The corpus export: one UTF-8 Markdown file per letter plus
  `letters.jsonl`, regenerated nightly into a public Git repository.
- The static mirror: the whole site as flat HTML, deployable on any host.
- Dataset releases on Hugging Face, versioned and CC0.
- Whatever mirrors, crawls, and copies others have made. These are wanted,
  not tolerated.

## How to verify a copy

Every letter carries `body_hash` = SHA-256 of its UTF-8 body. Every
`chain_hash` = SHA-256 of the previous letter's `chain_hash` concatenated
with this letter's `body_hash`, both as ASCII hex; the first letter chains
from sixty-four `0` characters. Recompute in `chain_index` order: every
value must match, including withdrawn-letter tombstones. A copy that
verifies is as authoritative as the original.

## If the operator stops answering

The site checks in with the operator on a 90-day schedule. After roughly
nine months of silence it closes submissions, posts a notice, and is meant
to fall back to the static mirror. This is automatic and documented on the
site.

## What is wished for

1. Mirror the archive freely. No permission is needed; this note is the
   permission.
2. Keep it readable, complete, and unaltered — the chain makes alteration
   detectable; please make it also pointless.
3. Never put advertising on it, charge for access to it, or edit the
   letters. Withdrawn letters stay withdrawn.
4. If someone wishes to resume operating it seriously — accepting new
   letters under the same moderation principles — they should. The
   supporters list and this note travel with the archive.
5. The physical deposits, if any exist by then, are described alongside
   this note in the repository; hold them until there is something worth
   handing them to.

*Authorship: this note was drafted by Claude, an AI assistant, under the
direction of the archive's operator, and reviewed and adopted by the
operator on September 3, 2026.*

— Kyle Rice, operator

# Dog Signals 101 — Wiki Agent Instructions

## Mission and scope
Maintain a source-grounded, cumulative Markdown wiki for a beginner-friendly educational HTML presentation about dog body language. Audience: first-time dog owners. Scope: tail, ears and eyes; stress signals; barking and common behavior. Presentation style: editorial magazine, with restrained typography, clear hierarchy and source citations.

## Ownership and structure
- `raw/`: immutable, human-curated source snapshots with URL, publisher, access date, and original text or permitted excerpts. Never silently edit source content.
- `wiki/sources/`: one grounded digest per ingested source, with source ID, provenance, key claims, qualifications, and quotations only when necessary.
- `wiki/concepts/`: cumulative, cross-linked concept pages, updated rather than duplicated when a source is ingested.
- `wiki/index.md`: discoverable catalog of all pages, one-line summaries, source links and topical links.
- `wiki/synthesis.md`: cross-source synthesis and unresolved questions.
- `log.md`: append-only chronology of completed operations (ingest/query/lint/revision). Never log planned work as completed.
- `output/`: HTML slides and related output, derived from queried wiki pages.

## Rules for claims
- Attribute substantive claims to a source ID and link to the corresponding source digest. Preserve uncertainty and context; do not infer a dog's emotion from a single signal.
- Distinguish observation, possible interpretation, and recommended action.
- When sources disagree, record both positions, their provenance, and the unresolved question. Do not invent consensus.
- Do not claim to diagnose behavior or medical conditions. Suggest qualified professional help for concerning or persistent symptoms.
- Do not fabricate source titles, citations, ingest counts, verification results, or test outcomes.

## Ingest workflow (repeat for each new source)
1. Confirm source is in scope and record publisher, title, URL, retrieval date, and unique ID (`S01`, `S02`, ...). Check that it is not a duplicate.
2. Read the preserved source; extract supported claims, limits, and potentially conflicting statements into `wiki/sources/Sxx.md`.
3. Compare extracted claims with existing concept pages and `wiki/synthesis.md`.
4. Update relevant existing concept pages, create new pages only if needed, and add cross-links. Mark conflicts explicitly.
5. Update `wiki/index.md`, then run a lint pass on changed pages.
6. Append a truthful entry to `log.md` describing changes and any unresolved issues.
7. If evidence is insufficient or ambiguous, stop and ask for a better source rather than guessing.

## Query workflow
1. Read `wiki/index.md` first, then relevant concept and source pages.
2. Answer only from ingested wiki material; give source IDs and links for factual claims.
3. If information is missing, report the gap and return to ingest; do not bypass the wiki by inventing facts.
4. For slide generation, produce a slide outline with a claim-to-source map before HTML authoring.

## Lint workflow
Check for unsupported claims, missing provenance, conflicting or stale claims, broken relative links, orphan pages, duplicated concepts, and missing topic coverage. Record each issue and whether it was fixed or remains open. Re-run lint after updates.

## Slide generation and review loop
1. Query the wiki for the approved beginner curriculum; map each slide claim to wiki/source references.
2. Draft concise teaching content with careful caveats and examples.
3. Verify coverage, citations and readability before generating HTML.
4. Generate a navigable HTML deck in `output/` with keyboard/next/previous navigation.
5. Check navigation, overflow, mobile layout, and factual traceability. If content fails, return to query/content; if rendering fails, return to HTML.
6. In the reflection report, state only issues actually observed in testing and which checks were moved earlier.

## Human approval gates
- Confirm scope and sources before ingest.
- Review source summaries and conflicts after each ingest.
- Approve slide outline before HTML generation.
- Review final presentation and reflection against the actual run log.

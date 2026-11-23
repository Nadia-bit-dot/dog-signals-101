# Wiki Operation Log

## [2026-11-23] setup | Initial schema
Created the wiki directory structure and working rules. No external source was ingested, queried, or linted as evidence.

## [2026-11-23] ingest | S01 AKC dog body language
Saved the user-provided PDF snapshot unchanged in `raw/`, recorded source metadata, created `wiki/sources/S01.md`, added four concept pages with cross-links, and updated `wiki/index.md` and `wiki/synthesis.md`. Only PDF pages 1–3 were used for article claims.

## [2026-11-23] lint | S01 local structural check
Checked internal Markdown relative links and source reference coverage; remaining content gaps: barking and detailed ear postures. No cross-source contradiction check possible with one source.

## [2026-11-23] ingest | S02 ASPCA
Reviewed PDF pp.1–3, added source digest and updated tail, ears, stress, context pages.

## [2026-11-23] source-gate | S03 VCA/LifeLearn
Identified explicit AI repurposing restriction on PDF p.2. Registered provenance only; did not ingest into wiki.

## [2026-11-23] ingest | S04 VCA vocalizations
Reviewed PDF p.1, added source digest and barking page; updated context links.

## [2026-11-23] ingest | S05 AKC stress
Reviewed PDF pp.1–5, added source digest; updated stress, ears, barking and context pages.

## [2026-11-23] lint | Markdown links and source count
Checked 12 Markdown wiki pages, 0 broken relative links; 4/5 eligible ingests. See output/lint-report.md.

## [2026-11-23] ingest | S06 Dogs Trust fear and emotions
Read captured PDF (17 pages; substantive passages on pp. 5–13), preserved source snapshot and provenance, added S06 digest, integrated new concepts into existing stress/context/ears pages, and updated index and synthesis. Kept S03 restriction intact. Note: copyright/republication permission for source images and full PDF remains unverified.

## [2026-11-23] lint | After S06
Rechecked relative Markdown links, source digest count, and presence of provenance; results in `output/lint-report.md`. No HTML slide tests run.

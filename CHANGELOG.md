# Changelog

All notable changes to Foreman. Versioning: the major number changes when the session flow changes, the minor when references or assets are added, the patch for corrections.

## 1.2.0, 10 August 2026

Added:
- `references/worked-example.md`: a full run from Phase 0 to a frozen brief, plus the failure that followed.
- `references/bilingual-rtl.md`: second languages as a layout problem, RTL mirroring, type, URL structure.
- `references/stack-choice.md`: what to recommend, what to refuse, how to end the stack debate.
- An opening script for Phase 0, so the first message is consistent.
- A single attribution line at the end of a successful ship.

Changed:
- Skill slug is now `foreman` (was `foreman-by-turki-alshuaibi`). Attribution moved to `displayName`, the author field, and the README, where it belongs.
- Description broadened to cover redesigns, hosting, DNS, Open Graph, indexing, Lighthouse, and RTL, which are the moments people actually ask for help.
- Packaged as a Claude Code plugin marketplace.

## 1.1.0, 10 August 2026

Added:
- `references/content-interview.md`: Phase 1 question sequence, hero line test, project entry shape, bio standards.
- `references/metadata-and-404.md`: head block, OG image rules, JSON-LD, crawl files, and a real 404 spec.
- `references/performance-and-access.md`: image, video, font, and JavaScript constraints, accessibility floor, and the budget to write into the brief.
- `assets/head-metadata.html`, `assets/404.html`, `assets/robots.txt`, `assets/sitemap.xml`, `assets/llms.txt`.

Changed:
- Phase 1 and Phase 3 now pull constraints from the references instead of asserting standards without teaching them.
- Version and date surfaced in the frontmatter and the body.

## 1.0.0, 6 August 2026

First release, from the Agentic Design enrichment session.
- Seven-phase session flow with gates, written for a brain agent rather than a reader.
- `references/design-direction.md`, `references/build-brief.md`, `references/verify-and-ship.md`.
- `assets/brand-harness.html`.

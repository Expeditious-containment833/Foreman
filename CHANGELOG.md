# Changelog

All notable changes to Foreman. Versioning: the major number changes when the session flow changes, the minor when references or assets are added, the patch for corrections.

## 1.3.0, 11 August 2026

Added:
- `references/design-direction.md` now refuses the single accented word. Colouring one word of a headline in the brand colour is one of the strongest tells that a machine set the type, along with the one-word gradient, swoosh, and highlighter block. The section gives the structural alternatives that are actual decisions.
- Gates for phases 4, 5, 6, and 7. The playbook claimed seven gated phases and only had four.
- A hard number for the hero media cap, 1.5 MB, in `performance-and-access.md` and in the brief template, which previously read `[X] MB`. This is the constraint whose absence produces the failure in `worked-example.md`.

Changed:
- The failure-modes list names the agent's own version of the first failure: presenting a finished visual system instead of variants the owner chose from.
- `assets/brand-harness.html` now fills all three variants. It previously shipped one filled variant and two empty stubs, so the side-by-side comparison the file exists for could not happen without extra work.
- The Close section can now truthfully say the repository is linked in the skill, because it is.

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

# Design direction (Phase 2)

The purpose of this phase is to convert forty small design decisions the coding agent would make silently into one decision the owner makes deliberately.

## Run the brand harness

Generate a single throwaway file, `brand.html`, that is not part of the real project. Start from `assets/brand-harness.html` and fill it with their content. It renders in one view:

1. The candidate type pairing, set with their actual name and their actual bio paragraph. Never lorem ipsum, because type decisions made on fake text collapse on real text.
2. The palette as labeled tokens with hex values: background, surface, text, muted text, accent. Assembled in context, not as isolated swatches.
3. One button, one card, one nav bar built from those tokens.
4. Their logo at real size in the mock nav. An SVG wordmark or monogram is plenty for v1.

Produce two or three full variants in the same file so they compare side by side rather than judging one option in isolation. Make them pick one. The winning values go into the build brief verbatim, as locked tokens the coding agent may not substitute.

## Refuse the defaults

AI-generated design currently clusters around three looks:

- Cream background near `#F4F1EA`, high-contrast serif display, terracotta or warm-clay accent.
- Near-black background with a single acid green or vermilion accent.
- Broadsheet layout: hairline rules, zero border radius, dense newspaper columns.

Any of these is legitimate **if the owner chose it**. If you produced one without being asked, you handed them the statistical mean instead of a decision. Redo it.

Same test for structure. Numbered markers (01 / 02 / 03), eyebrow labels, and section dividers should encode something true about the content. If the content is not actually a sequence, numbering it is decoration pretending to be information.

## Spend boldness in one place

Help them name one signature element the page is remembered by: a hero treatment, a type move, a single orchestrated animation, an interactive artifact from their own domain. Then keep everything around it quiet and disciplined.

Scattered effects read as generated. One deliberate move reads as designed. Complexity has to match the direction: maximalist needs elaborate execution, minimal needs precision in spacing and type detail. Elegance is executing the chosen direction well, not adding more.

The subject's own world is where distinctive choices come from. A robotics researcher, a poet, and a payments startup should not arrive at the same page.

## References are reading, not templates

If they bring sites they admire, extract named principles and carry those forward:

- "The hero is one sentence and one link, no graphic."
- "Only three type sizes on the entire page."
- "Sections are separated by space, never by borders."

Never carry the URL forward as something to approximate. Similar means derivative, and a derivative of someone else's identity with their name on it is worse than something plain and theirs. If output starts mirroring one reference, stop and name what is being copied.

## Copy is design material

If they have written weak copy, edit it with them rather than replacing it. Plain verbs, sentence case, no filler. Specific beats clever. Name things by what the reader recognizes, not by how the system is built. A label labels, an example demonstrates, and nothing quietly does double duty.

## Gate

Do not advance until you have: exact hex values for every token, exact font names, a type scale of about three sizes, and one named signature element.

# Canonical research knowledge base

Keep one navigable record per reference target in the user-selected output directory. Avoid parallel copies of the same findings. Create topic/page files only where the evidence warrants useful detail.

## Required documents

- `RESEARCH_INDEX.md` — canonical entrypoint: target URL/title, research date, scope, links to every created document and evidence folder, how to reuse the research during implementation, and important limitations.
- `RESEARCH_STATUS.md` — coverage ledger for all 16 categories from `research-checklist.md`; status (covered/partial/inaccessible/unresolved), evidence links, and remaining questions.
- `COLOR_PALETTE.md` — palette, color usage, combinations, section/state mappings, CSS tokens, gradients/overlays, and swatches as relevant. Every color value states provenance and confidence.
- `RECREATION_GUIDE.md` — implementation-relevant patterns, evidence links, responsive/performance notes, and choices left to the user. Separate target observations from proposed recreation strategies.

Add focused files such as `WEBSITE_OVERVIEW.md`, `SITE_STRUCTURE.md`, `TYPOGRAPHY.md`, `LAYOUTS_AND_SPACING.md`, `HEADER_AND_NAVIGATION.md`, `ANIMATIONS_AND_TRANSITIONS.md`, `SCROLLING_SYSTEM.md`, `IMAGE_GALLERIES.md`, `RESPONSIVE_DESIGN.md`, or `pages/<page>.md` only when useful findings justify them. Store screenshots and exported evidence in clearly named subfolders only when produced. Do not create empty categories or placeholder files.

## Finding record

Use a compact record for each material finding:

- **Finding:** one observable claim.
- **Classification:** Verified / Inferred / Estimated / Unknown.
- **Evidence:** REA evidence ID and relevant view/field, URL or asset, screenshot/recording path, or inspected CSS/computed property. State what the evidence actually establishes.
- **Context:** page/URL, viewport dimensions and device mode, timestamp/time zone if known, scroll position/stage, interaction state/action, and browser/tool context when relevant.
- **Detail:** measurements, exact value and units, state transitions, trigger/timing/easing if measured, or sampled method.
- **Recreation note:** feasible approach and known constraints, clearly marked as a proposal rather than a claim about original source code.
- **Limits/unknowns:** inaccessible states, incomplete coverage, ambiguity, or confidence bounds.

Do not force irrelevant fields into every record; retain enough context to make the evidence reproducible and correctly scoped.

## Provenance rules

- **Verified** means directly observed or supported by inspected source/computed evidence. Cite the evidence and scope.
- **Inferred** means a plausible explanation supported by observations, not confirmed source implementation. State the reasoning and alternatives when material.
- **Estimated** includes screenshot-derived measurements/colors. Describe the sample method and viewing conditions where available; do not imply source-level precision.
- **Unknown** means not determined or not accessible. State what would be needed to resolve it.
- For exact colors, preserve the original property/token and source context (stylesheet/resource, selector or component, state, and computed value when available). Record HEX plus original RGB/HSL notation when relevant. Keep alpha separate or explicit. For screenshot-derived samples, label each value estimated and identify the screenshot/region/sample method.
- For timing, breakpoints, dimensions, and performance, distinguish measured values from visual estimates. Do not report FPS, Core Web Vitals, or cross-browser behavior unless measured in a suitable way.
- Preserve REA evidence IDs and any source hash, capture ID, limitations, or incomplete/truncated result indicators supplied by REA. Do not treat static evidence as runtime observation.

## Research-to-build handoff

The index and relevant topic files are the starting point for an authorized build. Reuse recorded evidence and screenshots. Translate observations into explicit recreation decisions while retaining provenance; user-provided branding, content, and creative direction govern adaptation. Compare requested fidelity against the actual recorded states and identify unresolved evidence gaps before making assumptions. Reopen the reference only when saved research does not answer a concrete implementation question.

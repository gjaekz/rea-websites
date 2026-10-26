# Reverse Engineering Workflow

## Phase boundaries and prerequisites

Research requires the installed `reverse-engineer-anything` skill and connected REA MCP. If either prerequisite is missing, follow the skill's recovery guidance, explain the limitation, and do only supported work without implying REA was used. Do not install, configure, or repair REA automatically. Research and implementation are separate phases; use saved findings for an authorized build.

## MAIN REA RESEARCH WORKFLOW

Use this workflow for a full-site research request. For a user-selected feature or component, follow the targeted investigation workflow immediately after this section instead of repeating the full-site checklist.

1. **Explore the accessible site.** Resolve the user-provided reference URL and output location; confirm the installed REA skill and connected MCP tools, then inspect accessible pages, navigation, sections, and meaningful states across available viewports. Respect scope and note inaccessible areas.
2. **Inspect technical evidence.** Use only capabilities actually exposed by the installed REA version. Inspect relevant DOM, styles, computed values, scripts, assets, and runtime behavior where available. Preserve evidence identifiers and distinguish verified observations from inferences, estimates, and unknowns.
3. **Capture visuals and motion.** Capture useful screenshots and controlled interaction or motion states, including responsive views where accessible. Record URL, viewport, timestamp when available, scroll position, action/state, and tool context. A still image does not establish implementation details or motion timing.
4. **Interpret provenance.** Relate observations to their actual evidence. Use source/computed CSS or tokens for verified exact values; label screenshot-derived values as estimates. State coverage limits and avoid unsupported claims.
5. **Save the canonical knowledge base.** Follow [knowledge-base.md](knowledge-base.md) for full-site output files, evidence records, and index organization. Use [research-checklist.md](research-checklist.md) to track applicable coverage across all 16 categories; do not invent empty evidence folders or duplicate existing research.
6. **Verify coverage and stop.** Check each of the 16 categories for coverage, partial coverage, inaccessibility, or unresolved questions; link evidence and note gaps. Summarize the research and stop pending build authorization. An earlier explicit build authorization in the conversation remains in force.

## 5. TARGETED REVERSE ENGINEERING — USER-DIRECTED FEATURE INVESTIGATION

### PURPOSE

In addition to analyzing entire websites, REA must support **focused investigations of specific features, components, visual styles, animations, and interactions selected by the user**.

At any point during research or future development, I may direct you to investigate a particular element of a reference website.

Examples of user instructions:

- "Look at the animation used in this website's hero section."
- "Study how the photographs move while scrolling."
- "Look at this screenshot and find the corresponding element on the reference website."
- "Analyze the navigation menu and how it opens."
- "Understand the cursor interaction on this gallery."
- "Study how this heading reveals itself when scrolling."
- "Look at this specific section and recreate its layout."
- "Analyze the transition between these two sections."

**Treat these instructions as targeted reverse-engineering requests, not general website-analysis tasks.**

### STEP 1 — IDENTIFY THE EXACT TARGET

Determine precisely what the user wants investigated.

The target may be identified through:

- A specific website URL
- A particular page or section
- An uploaded screenshot
- A selected visual element
- A description of an animation or interaction
- A timestamp from a provided video
- A comparison between two visual states

When a screenshot is provided, use it as a visual reference to locate the matching element on the live website.

Do not assume the screenshot alone reveals how the feature works.

If the exact element cannot be located, report the uncertainty rather than inventing a match.

### STEP 2 — INVESTIGATE THE TARGET USING REA

Use the installed REA skill and available MCP tools to investigate the selected feature.

Depending on the target, use relevant capabilities such as:

- `list_browser_targets`
- `inspect_web_page`
- `observe_web_session`
- `capture_browser_scenario`
- `capture_web_screenshot`
- `analyze_web_bundle`
- `export_web_scripts`
- `compare_web_captures`
- `compare_web_screenshots`

Use complementary browser tools to navigate to the element, reproduce its interaction, inspect computed styles, and capture its visual states.

Focus the investigation on the requested feature and its immediate dependencies instead of repeating the entire website analysis.

For example, when investigating a gallery animation, examine the gallery's DOM structure, image containers, transforms, clipping, scroll triggers, interaction states, and relevant scripts.

### STEP 3 — UNDERSTAND THE FEATURE COMPLETELY

For every targeted feature, determine:

1. **Visual appearance:** Colors, HEX values, typography, dimensions, spacing, composition, and layering.
2. **Structure:** HTML hierarchy, containers, positioning, and relevant CSS rules.
3. **Behavior:** How it reacts to scrolling, hovering, clicking, dragging, cursor movement, or navigation.
4. **Animation:** Trigger conditions, direction, duration, easing, delay, stagger, transforms, and animation sequence.
5. **Technical implementation:** Relevant observed JavaScript, CSS, libraries, and feasible recreation techniques.
6. **Responsive behavior:** Differences between desktop, tablet, and mobile.
7. **Performance:** Rendering characteristics and how to reproduce the effect without flickering, stuttering, or layout shifts.
8. **Evidence:** Screenshots, code observations, REA findings, measurements, and relevant limitations.

For animated features, inspect multiple states: **before activation, during the effect, and after completion**.

Do not conclude the investigation based on a single screenshot or visual observation.

### STEP 4 — DOCUMENT AND SAVE THE TARGETED FINDINGS

Create a dedicated Markdown document for each investigated feature.

Use this structure:

```text
REFERENCE_RESEARCH/
└── targeted_features/
    └── FEATURE_NAME/
        ├── ANALYSIS.md
        ├── IMPLEMENTATION_GUIDE.md
        ├── screenshots/
        └── evidence/
```

`ANALYSIS.md` must describe the feature's appearance, structure, behavior, animations, and technical evidence.

`IMPLEMENTATION_GUIDE.md` must explain how the feature can be recreated later, including relevant CSS, JavaScript, animation strategies, responsive behavior, and performance requirements.

Store the supporting screenshots and REA evidence alongside the analysis.

Update `RESEARCH_INDEX.md` so the new investigation can be discovered and reused during development.

Avoid duplicating existing research. Link to previously documented design tokens, layouts, or animation systems whenever applicable.

### STEP 5 — REUSE THE KNOWLEDGE WHEN REQUESTED

After documenting the targeted feature, follow the project's phase restrictions.

**During the initial research phase:** Save the findings and stop. Do not implement the feature.

**During an authorized development phase:** Use the targeted findings to recreate or refine the feature in our website when instructed.

When implementing, compare the result against the original reference and its saved evidence.

Preserve the requested visual appearance, motion characteristics, and interaction behavior while adapting the feature to our website.

### TARGETED INVESTIGATION PRIORITY RULE

When I identify a specific feature, screenshot, or animation, **that element becomes the immediate research priority**.

Do not ignore my selected target in favor of unrelated sections. Do not restart the entire website investigation unless it is necessary to understand the feature.

Use REA to investigate the specific target as deeply as the available evidence permits, save everything learned, and make the knowledge reusable.

### CORE PRINCIPLE

**USER SELECTS A FEATURE → LOCATE IT → INVESTIGATE WITH REA → CAPTURE EVIDENCE → UNDERSTAND ITS BEHAVIOR → DOCUMENT IT → RECREATE WHEN AUTHORIZED.**

The same workflow must support both complete website reverse engineering and highly focused, user-directed investigations.

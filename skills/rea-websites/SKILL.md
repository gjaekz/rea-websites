---
name: rea-websites
description: Research a reference website with Reverse Engineer Anything (REA), preserve evidence in a reusable knowledge base, and use it later for user-directed recreation and comparison. Use for website analysis or an explicitly authorized recreation based on prior research.
---

# REA Websites

Use this skill when the user asks to analyze a reference website or to recreate/refine a website using saved reference research. Treat research and implementation as distinct phases: research is the default for analysis requests; finishing research never starts a build by itself. Honor an explicit build authorization already given in the conversation without asking for it again.

## Prerequisites

This skill is a companion to [Reverse Engineer Anything (REA)](https://github.com/morluto/rea), not an REA installation or MCP server. Before research, the user must have the `reverse-engineer-anything` skill installed locally and REA MCP connected to the agent. Installing this skill alone provides neither. If either is missing, stop and explain the limitation; continue only with supported work and clearly label what was not investigated with REA.

Install/configure REA separately using its [official setup instructions](https://github.com/morluto/rea) (currently `npx rea-agents setup`; Node.js and npm are required). Review proposed setup changes and restart the agent as directed upstream. Browser investigation also requires a Chrome-family browser with configured CDP or a supported REA scenario session; see [browser observation setup](https://github.com/morluto/rea/blob/main/docs/browser-observation.md). Discover available tools and follow the installed REA instructions; names and schemas vary by version. This skill never runs setup commands automatically.

## Research

1. Resolve the reference URL and output directory from the current conversation or workspace. Ask only for either value that is unavailable when actual research is invoked.
2. Read the installed `reverse-engineer-anything` skill and its relevant browser references. Discover the actual REA tools and schemas exposed in this session; use REA as the primary investigation tool.
3. Inspect the site interactively and technically within accessible scope. Collect evidence for applicable areas in [research-checklist.md](references/research-checklist.md), including desktop, tablet, and mobile states where available.
4. Record findings in one canonical knowledge base following [knowledge-base.md](references/knowledge-base.md). Link claims to evidence and distinguish verified, inferred, estimated, and unknown details. Record viewport, timestamp, scroll/interaction state, evidence identity, and coverage limits where relevant.
5. Check coverage against all 16 checklist categories and record unresolved areas. Summarize the findings and stop. Do not begin implementation automatically.

If REA is absent, follow its installed recovery guidance to diagnose the session. Report the limitation and continue only supported work without implying REA was used. Do not silently substitute generic browsing for REA, change configuration, install packages, or repair setup automatically. Use only capabilities and schemas actually available. Preserve tool evidence and its stated limitations.

Exact colors require provenance: prefer inspected CSS, computed styles, or tokens; label screenshot samples as estimates and never promote estimates to verified values. User controls the creative direction. Do not infer approval for external actions from a research request.

## Recreation and refinement

Start only when explicitly instructed, including authorization already present earlier in the conversation. Read the saved index and relevant research before coding; reuse that evidence instead of repeating research. Follow the user's requested branding, content, and structure. Compare the implementation to the documented target and evidence, and refine requested fidelity and performance. Revisit the reference only to resolve a concrete gap or verify a disputed finding.

Create documents according to relevance, not as an empty template set. Always maintain `RESEARCH_INDEX.md`, `RESEARCH_STATUS.md`, `COLOR_PALETTE.md`, and `RECREATION_GUIDE.md`; add topic or page analyses only when findings warrant them. Do not add filler, copies of source instructions, duplicated workflows, or generic design rules.

For detailed investigation coverage see [research-checklist.md](references/research-checklist.md). For the single canonical research output structure and evidence record format see [knowledge-base.md](references/knowledge-base.md).

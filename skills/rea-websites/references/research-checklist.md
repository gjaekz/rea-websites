# Research checklist

Use this checklist to scope and audit reference-site analysis. For full-site research, cover all 16 categories and mark each applicable, partially covered, inaccessible, or unresolved in `RESEARCH_STATUS.md`. For a targeted feature request, investigate only applicable dimensions of the selected target and its immediate dependencies; keep unrelated categories out of scope. Do not imply completeness where evidence is partial. Explore accessible relevant pages and states, not just the first viewport. Use the target site's observed behavior and the actual REA capabilities available in the session.

## Evidence standard

For each significant finding, record appearance, location/dimensions, behavior, animation/trigger when applicable, responsive variation, feasible recreation notes, supporting evidence, and unknowns. Label statements **Verified**, **Inferred**, **Estimated**, or **Unknown**. A visual impression is not evidence of source implementation. Preserve REA evidence identifiers, source boundaries, and tool limitations.

For evidence context, retain the URL/page, viewport dimensions/device mode, timestamp, scroll position or stage, interaction state/action, and evidence source/ID. Screenshots are visual references; they do not by themselves prove DOM/CSS implementation, full-page coverage, or motion timing. Capture multiple controlled states or recordings when motion cannot be explained by a still image.

## 1. Overall design and visual identity

Template/design philosophy; aesthetic and brand language; consistency; hierarchy and composition; negative space; grid/alignment; density and balance; borders/dividers/shadows/overlays; shapes, layering, depth, overlap; textures, gradients, and transitions between light/dark sections.

## 2. Color palette, combinations, and system

Investigate primary, secondary, tertiary, dominant, accent, and neutral colors; section-specific colors; CSS custom properties/design tokens; CSS and computed values; HEX plus RGB/RGBA/HSL/HSLA when relevant; transparent values and opacity. Map foreground/background pairings, contrast, warm/cool balance, color distribution, themes, and variations. Cover page/section backgrounds, header/footer, cards, overlays, menus, typography, links, buttons, icons, cursor, forms, focus/disabled states, gradients (stops/direction), blur/backdrop filters, shadows, blend modes, and animated color changes across scroll/hover/state.

`COLOR_PALETTE.md` must include a master palette with exact HEX and provenance, usage map by page/section/component/state, combinations, section palette, interactive states, original CSS variables and clearly marked suggested tokens, gradient/overlay definitions, and a visual swatch guide where useful. Distinguish CSS/computed verified values from screenshot-sampled estimates. Never call an approximated HEX verified.

## 3. Website structure and layout

Sitemap/page hierarchy and section order; header/main/footer; content organization; widths/heights/margins/padding; full-screen/full-width regions; editorial, asymmetric, split-screen, and grid compositions; sticky/fixed/floating elements; containers/max widths; section transitions; responsive structural changes.

## 4. Header and navigation

Dimensions, placement, transparent/solid/scroll states, sticky/disappearing behavior, menu structure, overlay/full-screen/mobile menus, opening/closing motion, hover/active indicators, dropdowns, logo/CTA placement, typography, and spacing.

## 5. Buttons and interactive elements

Shapes/dimensions/placement/padding; CTA hierarchy; hover/press/background/border/outline/text/icon transitions; magnetic effects if observed; badges/labels; forms; clickable cards; links and focus/active behavior.

## 6. Cursor and mouse interactions

Custom cursor shape/size/color/smoothness/trailing/easing; scaling/morphing; cursor-following content; magnetic, blending, or inversion effects; mouse parallax; distortion; hotspots; image reveals; behavior over links, controls, galleries, and different backgrounds.

## 7. Scrolling and animations

Native/custom scrolling, smoothness/inertia/easing; triggers and start/end positions; progress transformations; parallax; snapping/pinning/sticky/horizontal sections; image/text/background effects; direction changes; progress indicators; navigation scroll; layering/overlap; duration/delay/stagger/easing; reversibility on upward scroll.

## 8. Photography and image placement

Aspect ratios, sizes, focal points/crops, page placement, gallery/grid/masonry/editorial arrangements, edge-to-edge media, spacing/layering/overlap, reveals/masks/zoom/scale/parallax/cursor/hover effects, controls/lightboxes/sliders/drag, loading/lazy loading and layout stability.

## 9. Typography and text design

Typeface/family/source when evidenced, weights/styles, pairing, responsive size, hierarchy, line-height/tracking/capitalization/alignment, editorial compositions, text-image relationships/overlays, contrast, labels/captions, and spacing.

## 10. Text animations

Reveal, split, mask/clip, line/word/character sequencing, translation/fade/scale/rotation/skew, scroll transformations, stagger, animated headings/counters/numbering, hover replacement, and navigation transitions.

## 11. Page transitions and loading

Initial loading/preloader, hero/navigation/media entrance, page transitions, background/content fades and masks, progress/skeletons, duration/easing, browser history and scroll restoration, flicker/layout-shift behavior.

## 12. Hero and landing experience

Composition, media position, height/viewport coverage, typography, overlays, entrance/parallax/scale, CTA, scroll cue, decoration, transition into next section, desktop/mobile differences.

## 13. Components and content sections

Cards/blocks, image-text splits, alternation, editorial narratives, testimonials/quotes, features/stats/counters, location/maps, accordions, contact/booking, galleries/carousels/sliders, footer, back-to-top.

## 14. Responsive design

Desktop/laptop/tablet/mobile; observed breakpoints or bounded estimates; fluid type/spacing; navigation, touch/gestures, galleries, scroll/motion, image recropping, section heights, overflow, and orientation changes.

## 15. Performance and technical behavior

Observed rendering smoothness/jitter/stutter/flicker; layout shifts; scroll-animation synchronization; lifecycle/cleanup; transform/rendering behavior; image/font loading and optimization; lazy loading/preload; reduced motion; keyboard/focus accessibility; cross-browser and device limitations; load/performance metrics only when actually measured.

## 16. Microinteractions and fine details

Hover timing, icons, borders/underlines, subtle color/brightness/opacity shifts, element movement/scale, tooltips, decorative lines, loading feedback, focus/active states, and other small interactions that materially affect the experience.

## Coverage closeout

For full-site research, state coverage and gaps for all 16 categories. For targeted research, state coverage only for applicable dimensions of the selected feature and its immediate dependencies. Support coverage with evidence, scope negative claims narrowly (page, state, viewport, and method), and do not claim every page/state was explored when access or time was bounded.

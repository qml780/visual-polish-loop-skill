# Visual Review Lenses

Use these lenses to diagnose, not to generate a long generic checklist. Report only issues visible in the current screen and relevant to its primary task.

## 1. Task hierarchy

- Can a first-time user identify the page purpose and next action within a few seconds?
- Does one element dominate when several compete for attention?
- Are primary, secondary, and destructive actions visually distinct?

## 2. Spatial rhythm

- Do repeated elements share alignment, padding, and gaps?
- Are sections separated by meaningful rhythm rather than arbitrary whitespace?
- Does the layout preserve breathing room without hiding essential content below the fold?

## 3. Typography and content density

- Is the type scale doing useful work, or are headings and metadata nearly equal?
- Are line length, wrapping, truncation, and number alignment appropriate to the content?
- Can secondary text be read without competing with the primary task?

## 4. Color and surface logic

- Does contrast remain usable in normal, hover, focus, disabled, and error states?
- Are borders, shadows, fills, and accent colors communicating structure consistently?
- Is decoration reinforcing the interface rather than adding noise?

## 5. Responsive behavior

- Does the narrow layout reflow intentionally instead of merely shrinking?
- Are controls still reachable and labels still understandable?
- Check page-level overflow, clipped menus, fixed widths, dense tables, and sticky elements.

## 6. Interaction feedback

- Does every action show a clear hover/focus/pressed or progress response where appropriate?
- Do empty, loading, success, and failure states preserve layout and explain what happened?
- Are motion and transitions short, purposeful, and safe for reduced-motion preferences?

## Ranking rule

Rank by `task impact × page reach ÷ change risk`. Fix structural hierarchy and responsive breakage before decorative details. A subtle issue repeated across the whole screen may outrank one ugly but isolated icon.

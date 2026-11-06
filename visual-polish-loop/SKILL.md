---
name: visual-polish-loop
description: "Improve an existing web interface through a bounded screenshot-driven loop: capture a reproducible baseline, fix the highest-impact visual issues, and verify the same states on desktop and mobile. Use when a working UI needs polish or responsive cleanup; do not use for net-new product design or broad feature development."
---

# Visual Polish Loop

Turn “make it look better” into a short, repeatable visual QA pass with before-and-after evidence.

## Establish the baseline

Before editing, identify the smallest route or screen in scope and make it reproducible:

- Start the app using its existing workflow.
- Use stable demo data or a deterministic state; do not compare different content.
- Capture one desktop viewport and one narrow/mobile viewport. Record their dimensions.
- Exercise the primary interaction once and record console/page errors, horizontal overflow, and broken states.
- Preserve the original screenshots outside generated build folders so the final comparison is honest.

If the user supplied a reference image, treat it as direction for hierarchy, density, rhythm, and tone. Do not silently replace the product’s identity or copy unrelated branded assets.

## Choose the polish pass

Review the baseline through the lenses in [references/review-lenses.md](references/review-lenses.md). Rank issues by perceptual impact on the intended task, then select at most three for one pass.

Good candidates usually affect the whole experience: unclear focal hierarchy, inconsistent spacing, weak typography contrast, cramped responsive layout, missing interaction feedback, or accidental visual noise.

Prefer shared tokens and existing component patterns over one-off overrides. Preserve working behavior and accessibility semantics. Do not introduce a new UI framework, font service, animation library, or design system merely to polish one screen.

## Verify the delta

After editing, replay the exact baseline state and recapture the same viewport sizes.

The pass succeeds only when:

- the selected visual issues are materially improved in the new screenshots;
- the main interaction still works;
- the console has no new errors;
- the narrow viewport has no page-level horizontal overflow;
- focus, disabled, loading, and error states touched by the change remain understandable;
- relevant tests or checks pass.

If the result is merely different, revert or refine it. Do not call a style change an improvement without visible evidence.

## Stop conditions

- Stop after two polish passes or when the three highest-impact issues are resolved.
- Do not expand into navigation redesign, data-model work, new features, rebranding, or content strategy unless the user explicitly adds that scope.
- Do not chase pixel differences caused by font rasterization, timestamps, randomized data, caret blinking, or animation frames; stabilize or mask them first.
- If browser access or a runnable app is unavailable, report the blocked evidence instead of inventing a visual result.

## Handoff

Lead with the visible outcome. Provide before/after screenshots or paths, viewport sizes, the three issues addressed, interaction and console results, tests run, and any visual risks deliberately left unchanged.

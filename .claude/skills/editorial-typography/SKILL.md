---
name: editorial-typography
description: Create high-end editorial typography with precise reading rhythm, intentional line breaks, and tuned text width. Use when writing, reviewing, or adjusting any text-bearing markup or CSS for this manifesto site.
---

# editorial-typography

## Purpose
Create high-end editorial typography and a precise reading experience. Typography is the primary design element; every measurement is deliberate.

## When to use
- Writing or editing any HTML/JSX that contains prose, headlines, or manifesto copy.
- Tuning font sizes, line-height, letter-spacing, or max-width.
- Reviewing a page for reading rhythm, wrapping, or hierarchy issues.
- Any time copy is added, removed, or reflowed.

## Principles
- Every line break matters. Breaks are authored, not accidental.
- Fewer, stronger lines beat dense paragraphs.
- Spacing carries meaning — whitespace is content.
- Hierarchy comes from size, weight, and spacing, never from decoration.
- Rhythm must survive every breakpoint.
- Typography is the design. There is no other design.

## Instructions
- Set `max-width` in `ch` or `rem` so measure stays between roughly 45–75 characters for body, tighter for display lines.
- Size type fluidly with `clamp()` tied to viewport width; tune each breakpoint by eye, not by formula.
- Use `text-wrap: balance` on headlines and `text-wrap: pretty` on body where supported.
- Insert authored breaks (`<br>` or hard line splits) where a wrap would weaken a line; verify at every breakpoint.
- Lock line-height per role: tight for display (1.0–1.15), open for body (1.5–1.7).
- Tune letter-spacing negatively on large display type, neutral or slightly positive on small caps/labels.
- Preserve vertical rhythm with a consistent spacing scale; avoid arbitrary margins.
- Re-read the page at 320px, 768px, 1280px, 1920px before declaring done.

## Constraints
- No decorative UI elements.
- No cards, panels, borders, shadows, or containers used as ornament.
- No icons, dividers, or visual noise.
- No font stacks chasing novelty — one or two typefaces maximum.
- No justified text. No hyphenation hacks that produce rivers.
- No font sizes below legible minimums on any device.

---
name: responsive-precision
description: Ensure viewport-exact layout and cross-device consistency with dvh units, per-breakpoint typography tuning, and handling of mobile browser UI quirks. Use for any layout, sizing, or breakpoint work.
---

# responsive-precision

## Purpose
Ensure perfect viewport-based layout and cross-device consistency. Every section should feel composed, not computed.

## When to use
- Building or adjusting any layout, section, or full-viewport block.
- Adding or tuning breakpoints.
- Debugging mobile rendering, overflow, or browser-chrome issues.
- Verifying the site on real devices before shipping.

## Principles
- Each section equals an exact viewport height unless intentionally otherwise.
- Layout must feel intentional — not default — on every screen size.
- Never rely on default browser behavior to produce a good result.
- Breakpoints are editorial decisions, not framework presets.
- The same page should feel inevitable on a 320px phone and a 2560px display.

## Instructions
- Use `100dvh` (with `100svh`/`100lvh` fallbacks where needed) for full-viewport sections; avoid raw `100vh` on mobile.
- Account for iOS Safari address bar, Android URL bar, and notch/safe-area insets via `env(safe-area-inset-*)`.
- Tune typography, measure, and spacing per breakpoint — do not scale a single design linearly.
- Test and adjust explicitly for: mobile (≤480), tablet (~768), laptop (~1280), large desktop (≥1920).
- Prefer `clamp()` and container queries over stacks of media queries where they fit.
- Verify no horizontal scroll at any width; verify no clipped glyphs on any height.
- Check landscape phone, split-screen tablet, and zoomed desktop (125%/150%).
- Disable unwanted scroll chaining and overscroll where it harms the feel.

## Constraints
- No layout hacks that break on mobile (fixed `vh`, absolute pixel heights on sections, JS-based resize loops).
- No horizontal overflow, ever.
- No compressed or clipped typography at any supported breakpoint.
- No reliance on hover for essential behavior.
- No assumptions about viewport based only on width — height matters equally.
- No untested breakpoints in shipped work.

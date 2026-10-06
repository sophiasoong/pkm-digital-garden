---
title: "Scaffold & Breakpoints (Google M3)"
date: 2026-09-10
source: https://app.notion.com/p/New-Design-3c7b3ec8a02280d6aad7c35dc3bc03ea
tags: [design, layout, material-design, responsive]
---

Structural layout reference from Google's Material 3 scaffold system — the frame itself, how it responds across screen sizes, and the standard pane arrangements. Visual treatment of these structures lives in [[Visual Language — M3 Expressive & Liquid Glass]]; transitions between pane states in [[Motion Principles & Patterns]].

## Scaffold Parts

- **Bar** — top or bottom app bar
- **Rail** — side navigation
- **Pane** — main content area

Each configurable along two axes:

- **Permanent or temporary** — always present vs. summoned
- **Fixed or flexible** — set width vs. resizes with the viewport

## Breakpoints

| Breakpoint | Width (dp) | Devices |
|---|---|---|
| Compact | under 600 | Phone (portrait) |
| Medium | 600 – 839 | Tablet (portrait), foldable (portrait) |
| Expanded | 840 – 1199 | Phone / tablet / foldable (landscape), desktop |
| Large | 1200 – 1599 | Desktop |
| Extra-large | 1600+ | Desktop, ultra-wide monitor |

## Pane Layouts

**1-pane** — compact and medium breakpoints; flexible.

**2-pane**
- *Split (flexible)* — foldable devices and dynamic resizing
- *Fixed-and-flexible* — expanded, large, extra-large; pairs a fixed temporary pane with a flexible permanent one

**3-pane**
- Trailing side sheet, with the leading navigation rail collapsed or hidden
- Example: Spotify

## Pane Expand & Resize

Driven by drag UI, with two behaviours:

- **Persistent** — the resized state sticks
- **Temporary** — reverts to a default pane width

## Canonical Layouts

- **Feed** — card grid
- **List-detail** — email list alongside message detail
- **Supporting pane** — primary display area (2/3) with secondary (1/3)

## Related

- [[22 Concepts/usability|Usability — wiki concept page]] — the five metrics and six tactics these layouts serve
- [[Visual Language — M3 Expressive & Liquid Glass]]
- [[Motion Principles & Patterns]]

---
name: SMA-BE Pricing
description: Energy pricing cards for Belgian residential consumers
colors:
  bg: "#f8f6f6"
  card: "#ffffff"
  text-primary: "#2f2d2d"
  text-secondary: "#716a6a"
  ribbon-bg: "#e8e6f4"
  ribbon-border: "#d0caef"
  ribbon-text: "#3e235b"
  cta-green: "#007250"
  cta-green-hover: "#005a3e"
  link-underline: "#84dc99"
  check-green: "#009B65"
  shadow: "rgba(47, 45, 45, 0.12)"
typography:
  display:
    fontFamily: "Etelka, system-ui, sans-serif"
    fontSize: "32px"
    fontWeight: 700
    lineHeight: "36px"
  title:
    fontFamily: "Etelka, system-ui, sans-serif"
    fontSize: "24px"
    fontWeight: 700
    lineHeight: "28px"
  body:
    fontFamily: "Etelka, system-ui, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: "24px"
    letterSpacing: "0.3px"
  label:
    fontFamily: "Etelka, system-ui, sans-serif"
    fontSize: "14px"
    fontWeight: 700
    lineHeight: "20px"
    letterSpacing: "0.3px"
  cta:
    fontFamily: "Etelka, system-ui, sans-serif"
    fontSize: "18px"
    fontWeight: 700
    lineHeight: "28px"
rounded:
  card: "16px"
  button: "8px"
  highlight: "8px"
spacing:
  card-padding: "24px"
  ribbon-padding: "16px"
  feature-gap: "4px"
  section-gap: "24px"
  column-gap: "40px"
components:
  button-primary:
    backgroundColor: "{colors.cta-green}"
    textColor: "#ffffff"
    typography: "{typography.cta}"
    rounded: "{rounded.button}"
    height: "60px"
    padding: "0 24px"
  button-primary-hover:
    backgroundColor: "{colors.cta-green-hover}"
  card-default:
    backgroundColor: "{colors.card}"
    rounded: "{rounded.card}"
    padding: "{spacing.card-padding}"
  ribbon-default:
    backgroundColor: "{colors.ribbon-bg}"
    textColor: "{colors.ribbon-text}"
    padding: "{spacing.ribbon-padding} {spacing.card-padding}"
---

# Design System: SMA-BE Pricing

## Overview

**Creative North Star: "The Transparent Meter"**

Clean, honest, utilitarian. The SMA-BE pricing system treats clarity as its entire personality — like a well-designed utility bill where every number is immediately findable and every condition is spelled out. The interface steps back so the pricing speaks.

The visual language is deliberately restrained: white cards on a warm grey canvas, a single green for all actionable elements, and purple reserved exclusively for promotional ribbons. Density is comfortable but not spacious — pricing comparisons need proximity to work. The system flexes to accommodate variable content (different ribbon counts, feature lists, conditional prices, footnotes) without breaking cross-card alignment.

**Key Characteristics:**
- Subgrid-aligned cards ensure row-level horizontal consistency across products
- Purple is promotional only — never structural, never decorative
- Green is action only — CTA buttons and checkmarks, nothing else
- Content-driven height — cards grow to fit, never pad to match

## Colors

A deliberately narrow palette: warm neutrals for structure, one green for action, one purple for promotion.

### Primary
- **Eneco Green** (#007250): The single action color. Used exclusively on CTA buttons and the "Bekijk de details" link. Its hover state (#005a3e) darkens without shifting hue.
- **Check Green** (#009B65): A lighter green for feature checkmarks only. Distinct from CTA green to avoid false affordance on non-interactive elements.

### Secondary
- **Ribbon Lavender** (#e8e6f4): Promotional background. Signals "this card has an offer" before the user reads a word. Border variant (#d0caef) separates stacked ribbon items.
- **Ribbon Plum** (#3E235B): Text inside promotional ribbons. High contrast against lavender; never used outside ribbon context.

### Neutral
- **Canvas Warm Grey** (#f8f6f6): Page background. Warm enough to feel human, light enough that white cards separate cleanly.
- **Card White** (#ffffff): Card surfaces. Pure white, no tint.
- **Text Primary** (#2f2d2d): Near-black with warmth. All headings, prices, feature text, and body copy.
- **Text Secondary** (#716a6a): Footnotes, "per maand" labels, and supporting context. Distinct enough from primary to read as secondary, dark enough to remain legible.
- **Card Shadow** (rgba(47, 45, 45, 0.12)): Ambient lift. Warm-toned to match the neutral family.

### Named Rules
**The Two-Hue Rule.** Green and purple are the only chromatic colors in the system. Green means action; purple means promotion. If a new element needs color, it uses one of these two or it stays neutral.

## Typography

**Display Font:** Etelka (system-ui fallback)
**Body Font:** Etelka (system-ui fallback)

**Character:** A single-family system. Etelka carries everything from price figures to footnotes, differentiated by weight and size alone. The result is functional and confident — no typographic ornamentation, no contrast pairing.

### Hierarchy
- **Display** (700, 32px, 36px line-height): Price amounts only. The largest type on any card.
- **Title** (700, 24px, 28px line-height): Product names and the euro symbol in the price block.
- **Body** (400, 16px, 24px line-height, 0.3px tracking): Feature text, conditional price labels. The workhorse.
- **Label** (700, 14px, 20px line-height, 0.3px tracking): Ribbon text and footnotes.
- **CTA** (700, 18px, 28px line-height): Button text and detail links. Sized between title and body.
- **Caption** (300, 16px/14px, 24px line-height): "per maand" period labels. Light weight signals supporting context.

### Named Rules
**The Weight Rule.** Bold (700) means important or interactive. Regular (400) means informational. Light (300) means secondary context. No medium weights, no italic.

## Layout

Three-column grid with CSS subgrid for cross-card row alignment. Seven shared row tracks: ribbon, title, features, price, conditional price, CTA, footnotes. Cards span all seven rows and align content at the track level regardless of content height.

- **Grid:** `repeat(3, minmax(0, 420px))`, centered, 40px column gap, 24px row gap.
- **Card padding:** 24px horizontal throughout; vertical spacing governed by subgrid tracks.
- **Compact variant:** Cards without ribbon/footnotes start at row 2 and end at row 6, with top/bottom padding on title/CTA respectively.
- **Responsive:** Below 900px, collapses to single-column (max 420px centered). Subgrid disabled; cards use intrinsic gap-based layout.

## Elevation & Depth

Flat by default. Cards lift with a single ambient shadow (`0px 4px 12px 0px rgba(47, 45, 45, 0.12)`) — warm-toned, diffuse, no directional light. No other elements cast shadows. The conditional price box and ribbon use background color for layering, not elevation.

### Named Rules
**The One Shadow Rule.** Only cards have shadows. Everything inside a card is flat. Depth is conveyed through background color (ribbon lavender, conditional price lavender), never through nested shadows.

## Shapes

Gently rounded throughout. Cards use generous rounding (16px) for a approachable feel. Buttons and highlight boxes use moderate rounding (8px) — enough to soften without looking pill-shaped. No circular elements, no sharp corners anywhere.

## Components

### Buttons
- **Shape:** Rounded rectangle (8px radius)
- **Primary:** Full-width within card, 60px height, Eneco Green background, white text, 18px bold. Centered text, no icon.
- **Hover:** Darkened green (#005a3e), 0.15s transition. No shadow, no scale.
- **Link variant:** Green text, no background, green underline bar (2px, #84dc99) as pseudo-element. Bold 18px. Padding: 6px vertical.

### Cards
- **Corner Style:** Generously rounded (16px), `overflow: clip`
- **Background:** Pure white on warm grey canvas
- **Shadow:** Single ambient (`0 4px 12px rgba(47,45,45,0.12)`)
- **Internal Padding:** 24px horizontal, vertical governed by subgrid
- **Compact variant:** No ribbon row, no footnote row; title gets 24px top padding, CTA gets 24px bottom padding

### Ribbon (Promotional)
- **Background:** Lavender (#e8e6f4), flush to card top edge
- **Text:** Plum (#3E235B), 14px bold, 0.3px tracking
- **Icon:** 20px gift icon in plum, flex-aligned with text
- **Stacked items:** Separated by a 1px lavender border (#d0caef) with 16px padding between
- **Absence:** When a card has no promotion, the ribbon row is empty and collapses via subgrid

### Conditional Price Box
- **Background:** Lavender (#e8e6f4), 8px radius, 16px padding
- **Label:** Body text with an inline 20px info icon
- **Price:** 20px bold amount + light "per maand"
- **Absence:** Empty box collapses; subgrid row remains for alignment

### Feature List
- **Layout:** Vertical stack, 4px gap
- **Check icon:** 24px, Check Green (#009B65)
- **Text:** Body (16px, 400, 0.3px tracking)

## Do's and Don'ts

### Do:
- **Do** use subgrid to keep card rows aligned — the entire comparison mechanic depends on horizontal consistency.
- **Do** let cards grow to their content. A card with two features and one ribbon item is shorter; the subgrid handles it.
- **Do** keep the ribbon visually attached to the card top — flush edges, no internal margin above.
- **Do** use the `overflow: clip` on cards to crop ribbon backgrounds cleanly at rounded corners.

### Don't:
- **Don't** use purple outside of promotional ribbons and conditional price boxes.
- **Don't** add shadows to anything inside a card — only the card itself casts a shadow.
- **Don't** use medium font weights (500/600) — the system uses only 300, 400, and 700.
- **Don't** add icons to buttons — the CTA is text-only by design.
- **Don't** force equal card heights by padding — let subgrid handle alignment naturally.

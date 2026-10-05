# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Belgian residential consumers comparing and selecting a combined electricity + gas energy plan on the SMA Belgium website. They are price-sensitive, comparing monthly costs and promotions across variable (Flex) and fixed (Vast/Fix) tariff structures.

## Product Purpose

Help households choose the right Eneco Belgium energy bundle by presenting pricing, promotional discounts, and plan features side by side. Success is a confident "Product selecteren" click with minimal cognitive load.

## Positioning

SMA Belgium (Eneco brand family) — green, Belgian-sourced electricity ("100% groene en Belgische elektriciteit") as the differentiator. Conditional pricing with promotional discounts (korting) as a conversion lever.

## Operating Context

Pricing cards appear on the SMA-BE commercial website. Users arrive via marketing, comparison sites, or direct navigation. The page must handle variable card configurations: different ribbon counts, feature lists, conditional price blocks, and footnotes per product combination.

## Capabilities and Constraints

- Three product bundles: dual-variable (Flex One + Flex One), mixed (Flex One + Fix One), fixed (Vast + Vast).
- Cards use CSS subgrid to align shared row tracks across columns.
- Responsive: collapses to single-column at 900px.
- Static HTML/CSS prototype — no framework, no build step.
- Figma reference exists as the design source of truth.

## Brand Commitments

- Font: Etelka (system-ui fallback).
- Primary CTA: #007250 (green). Link underline: #84dc99.
- Ribbon/accent: #e8e6f4 background, #3E235B text (purple).
- Card radius: 16px. Button radius: 8px.
- Voice: direct, factual, Dutch (nl-BE).

## Evidence on Hand

- Figma reference screenshot: `figma-reference.png`.
- Current implementation screenshot: `current.png`.
- No real customer testimonials, case studies, or analytics data in this prototype.

## Product Principles

1. Clarity over persuasion — pricing must be immediately scannable and comparable.
2. Promotional logic must be transparent — discounts are conditional and footnoted.
3. Cards flex to content — the layout handles variable ribbon, feature, and footnote configurations without breaking alignment.

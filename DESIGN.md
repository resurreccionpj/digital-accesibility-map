---
name: Barangay Real Access
description: Accessibility map for Brgy. Real, Calamba. Plain, high-contrast, phone-first, status shown by shape as well as color.
colors:
  brand-teal: "#115e59"
  brand-teal-hover: "#0f766e"
  status-existing: "#15803d"
  status-needs-improvement: "#c2410c"
  status-proposed: "#1d4ed8"
  status-needs-assessment: "#4b5563"
  surface: "#ffffff"
  background: "#f8fafc"
  ink: "#0f172a"
  muted: "#475569"
  line: "#cbd5e1"
  sunken: "#f1f5f9"
  hover: "#f0fdfa"
  surface-dark: "#111827"
  background-dark: "#0b1220"
  ink-dark: "#f1f5f9"
  muted-dark: "#cbd5e1"
  line-dark: "#475569"
  sunken-dark: "#1f2937"
  hover-dark: "#134e4a"
typography:
  title:
    fontFamily: "Geist, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 700
    lineHeight: 1.25
  headline:
    fontFamily: "Geist, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.25rem"
    fontWeight: 700
    lineHeight: 1.25
  body:
    fontFamily: "Geist, ui-sans-serif, system-ui, sans-serif"
    fontSize: "0.875rem"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "Geist, ui-sans-serif, system-ui, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 600
    lineHeight: 1.33
rounded:
  md: "8px"
  xl: "12px"
  "2xl": "16px"
  full: "9999px"
spacing:
  sm: "8px"
  md: "12px"
  lg: "16px"
components:
  button-primary:
    backgroundColor: "{colors.brand-teal}"
    textColor: "{colors.surface}"
    rounded: "{rounded.xl}"
    height: "44px"
    padding: "0 16px"
  button-primary-hover:
    backgroundColor: "{colors.brand-teal-hover}"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.xl}"
    height: "44px"
    padding: "0 16px"
  input:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.xl}"
    padding: "10px 12px"
---

# Design System: Barangay Real Access

## Overview

**Creative North Star: "The Field Guide"**

A map people trust outdoors, on a phone, in sun. It is plain, high-contrast and unhurried. The map is the surface; the interface is a sidebar on desktop and a search bar, chips and a bottom sheet on a phone, in the manner of Google Maps. Light and dark both follow the browser setting.

Status is the product's main message and is never carried by color alone: every status has its own color, silhouette and glyph. Everything else stays neutral slate so those four signals stand out.

**Key Characteristics:**
- Slate neutrals, one teal brand accent, four reserved status colors.
- 44px minimum touch targets, 12px corners, soft but not playful.
- Light and dark from `prefers-color-scheme`; map tiles are inverted in dark.
- Geist throughout; small, even type steps.

## Colors

A slate canvas with deep teal as the only brand accent. Green, orange, blue and gray mean status and nothing else.

### Primary
- **Deep Teal** (#115e59): primary buttons and the logo tile. Hover is **Lighter Teal** (#0f766e).

### Status (reserved)
- **Existing Green** (#15803d): existing feature; circle with check.
- **Needs-Work Orange** (#c2410c): needs improvement; teardrop with "!".
- **Proposed Blue** (#1d4ed8): proposed; rounded square with "+".
- **Unassessed Gray** (#4b5563): needs assessment; leaf shape with "?".

### Neutral
- **Surface** (#ffffff light, #111827 dark): panels, inputs, sheets.
- **Canvas** (#f8fafc, #0b1220): page behind the map.
- **Ink** (#0f172a, #f1f5f9): text. **Muted** (#475569, #cbd5e1): secondary text, at least 4.5:1 on surface.
- **Line** (#cbd5e1, #475569): borders. **Sunken** (#f1f5f9, #1f2937): empty states, hover on light buttons. **Hover Tint** (#f0fdfa, #134e4a): list row hover.

### Named Rules
**The Never-Color-Alone Rule.** A status always appears with its shape and glyph, on pins, chips, list rows and feature tiles.
**The Reserved Colors Rule.** Green, orange, blue and gray are not used for decoration, buttons or links.

## Typography

**Font:** Geist (with system sans fallback). Geist Mono is loaded but unused in the UI.

**Character:** neutral and legible. Hierarchy comes from weight and size, not from a second face.

### Hierarchy
- **Title** (700, 1.125rem, 1.25): app name in the header.
- **Headline** (700, 1.25rem, 1.25): place name in detail and form headings.
- **Body** (400, 0.875rem desktop and 1rem on inputs for mobile, 1.5): lists, notes, form fields. Notes stay under 75ch.
- **Label** (600, 0.75rem): chips, status tags, feature tiles, helper text.

### Named Rules
**The 16px Input Rule.** Inputs are 16px on phones so iOS does not zoom.

## Layout

Desktop: a 416px floating sidebar at 16px from the left and top, rounded 16px, over a full-bleed map. Mobile (375px and up): full-bleed map with a search bar, status chips and a Menu popover on top, a bottom sheet for details and a full-screen list view as an alternative to the map. Spacing steps are 8, 12 and 16px; groups are tight and sections are separated by 12 to 16px. Leaflet zoom sits bottom right on desktop and is hidden on phones.

## Elevation & Depth

Mostly flat. Depth comes from tonal surfaces (surface over canvas, sunken for wells) and 1px lines. Shadows are for things floating over the map only: the locate button (`shadow-lg`), pins and feature tiles (`0 1px 3px rgba(0,0,0,.4)`), and the sidebar.

### Named Rules
**The Floats-Only Rule.** Only elements that sit over the map get a shadow.

## Shapes

Rounded rectangles at 12px for buttons, inputs and list rows, 16px for the sidebar and sheet, full round for chips and the locate button. Pins carry the status silhouette (circle, teardrop, rounded square, leaf) with a white disc holding the category emoji. Feature tiles are 20 to 24px squares with a 2.5px border in the feature's status color and its own corner shape.

## Components

### Buttons
- **Shape:** 12px radius, 44px minimum height, 16px side padding, 14px semibold text.
- **Primary:** Deep Teal fill, white text, lighter teal on hover.
- **Secondary:** surface fill, 1px line border, Sunken on hover.
- **Press:** scale to .98.

### Chips
Pill chips for Existing, Needs work and Proposed, each with its status glyph disc. Selected chips are filled; unselected are outlined. The "To assess" chip is hidden until some place uses it.

### Inputs / Fields
Surface fill, 1px line border, 12px radius, 10px by 12px padding. Placeholder uses Muted. Focus is a 3px ink outline with 2px offset (light in dark mode).

### List rows
56px minimum height: status silhouette tile with category emoji, name, category and status line, feature tiles, then a chevron. Hover uses Hover Tint.

### Feature tiles
Small squares showing a feature icon with a border color and corner shape for its status. When a filter is active, non-matching tiles drop to 30% opacity.

### Photo gallery
Photos grouped by feature, 176px wide, 128px tall, 12px corners, captions beneath. A native dialog lightbox opens on tap and closes with Esc or a Close button.

## Do's and Don'ts

### Do:
- **Do** pair every status color with its shape and glyph.
- **Do** keep touch targets at 44px or more.
- **Do** write every string in both English and Filipino.
- **Do** use the semantic tokens (`bg-surface`, `text-ink`, `text-muted`, `border-line`) so dark mode works.
- **Do** label desk-assessed data as unverified until fieldwork confirms it.

### Don't:
- **Don't** use status colors for decoration or links.
- **Don't** rely on color alone to convey status or feature state.
- **Don't** add shadows to elements that don't float over the map.
- **Don't** hard-code slate or white utility colors where a semantic token exists.
- **Don't** list places in a bottom panel on phones; the list is its own view.

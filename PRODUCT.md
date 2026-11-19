# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users
- PWD travelers (wheelchair, crutch, low-vision and other physical disabilities) planning or making a trip in Brgy. Real, Calamba City, Laguna. Usually on a phone, outdoors.
- Caregivers and families who plan or accompany those trips.
- Barangay/LGU officials who use the needs-improvement and proposed data to plan ramps and repairs.
- Volunteer editors with named accounts who survey on site and add or update places.

## Product Purpose
A public map of accessibility in Brgy. Real: ramps, sidewalks, crossings, restrooms, entrances, signage, parking, transport, health, schools and government places. Success: a traveler can tell before leaving whether a place and its approach are usable, and the barangay can see what to fix. Requirements come from the client PDF "DIGITAL ACCESSIBILITY MAP" (Oct 27, 2026).

## Positioning
Google-Maps-style browsing for accessibility: each place has several features (ramp, entrance, restroom, sidewalk, crossing, signage, parking), each with its own status, notes and captioned photos, filterable by feature and status.

## Operating Context
Public read, authenticated write. Editors collect data in the field following docs/FIELDWORK.md. Deployed on Vercel Hobby with Neon Postgres and Vercel Blob, so free-tier limits apply.

## Capabilities and Constraints
- Location = pin or line (street, sidewalk, crossing) plus a features checklist.
- Statuses: existing, needs_improvement, proposed, needs_assessment.
- UI in English and Filipino (lib/i18n.ts). List view alternative to the map. Map via Leaflet + OpenStreetMap, no API key.
- All write endpoints verify the session. No secrets in the repo.
- Desk-assessed entries come from OpenStreetMap and public pages, not site visits. "Not recorded" never means "absent".

## Brand Commitments
Name: Barangay Real Access. Statuses are never shown by color alone; each also has a shape and icon.

## Evidence on Hand
22 places with desk assessments, docs/FIELDWORK.md. No site-verified photos or testimonials yet; do not invent any.

## Product Principles
- Say what is known and what is not: unverified data is labelled, never presented as fact.
- Color is never the only carrier of status.
- Phone first, outdoors, one hand; the list view is as complete as the map.
- Everything in English and Filipino.
- Keep it within free-tier limits.

## Accessibility & Inclusion
WCAG 2.1 AA, keyboard and screen-reader friendly, works at 375px and on desktop.

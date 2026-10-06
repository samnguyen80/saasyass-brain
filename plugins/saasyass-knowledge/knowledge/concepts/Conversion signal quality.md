---
title: Conversion signal quality
source: "Saasyass Instagram"
verified: 2026-10-06
drift-risk: low
related:
  - "[[Demo funnel six levels]]"
  - "[[Existing customer exclusion]]"
  - "[[Meta account structure]]"
---

# Conversion signal quality

Watch: [Pixel Blind Conversions API](https://www.instagram.com/reel/Dd6zqKTh-XV/) · [Starving The Algorithm](https://www.instagram.com/reel/DduWy0AB7Ih/)

Meta optimises on what you tell it. Bad or thin signal means worse audiences and worse leads.

## Missing conversions

- The browser pixel loses events to ad blockers, privacy settings and device switching, so Meta undercounts and may drift to worse people. (Illustration: Meta says 12 demos, calendar says 31.)
- Fix: server-side Conversions API. No-code route: Zapier fires a schedule event when a booking lands in the calendar tool (email, phone, name).
- Second event: when a rep marks a lead qualified in the CRM, send that as its own event.
- Send the earliest signal that still means buyer. Closed-won arrives too late in months-long cycles; qualified call is usually the sweet spot.
- B2B match problem: work email at booking vs personal email on the profile. Always include phone, plus ad click ID if available. Target match quality 8+ of 10 (*claimed*). Test with a fake booking in events manager.

## Too few conversions

- Meta needs on the order of 50 conversions a week in an ad set to learn (*claimed*); below that, quality decays into colder audiences.
- Optimise on a more frequent event that still implies buyer, send CRM-qualified events, and use fewer ad sets with more ads.
- Budget check: weekly target x cost per qualified lead gives the daily spend one ad set needs; if unaffordable, find a cheaper qualified event.
- Trial funnels: report activated users, not every sign-up ([[Trial onboarding flow]]).
- Qualification gate before booking limits what gets reported: [[Demo funnel six levels]].

Cards: [[Saasyass - Pixel Blind Conversions API]] · [[Saasyass - Starving The Algorithm]] · [[Saasyass - Six-Level Demo Funnel]]

See `/teach-saasyass`.

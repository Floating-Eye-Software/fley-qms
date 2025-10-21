# Red Witch — Daughters of the Moon

*A cultural/lunar overlay for the Red Witch calendar system.*

---

## 1. Concept summary (one-liner)

An opt-in overlay where each user has a **Moon Sign** — the lunar phase on the night of their first period — and annual celebrations/observances (First Moon Night). Each moon phase maps to an archetype (e.g., Waxing Gibbous → “The Builder”), and the overlay surfaces gentle ritual suggestions, archetypal insights, and optional reminders while never altering raw cycle logs.

---

## 2. UX / Product behavior (how it behaves in the app)

**Onboarding (first enable)**

* When user enables “Daughters of the Moon” overlay: show short explainer card: purpose, privacy, opt-in only, not a medical tool.
* Request (optional) entry: *Date of First Period* (can be entered, imported from historical logs, or left blank). Clear CTA: “Add my First Moon Night” or “I prefer not to enter.”
* If user is uncomfortable: allow “Create Moon Sign from approximate age / year” (approximate) — make uncertainty explicit.

**Display**

* Overlay toggled on → shows a transparent layer above calendar days.
* On days tied to overlay (First Moon Night anniversary, moon-phase archetype month, ritual suggestions) show small crescent glyph in corner of day tile. Tap opens card.
* Layer legend available in overlay settings.
* Option: show a *Moon Sign* badge in user profile / cycle header: “Moon Sign: Waxing Gibbous (Red Witch)”.

**Interactions**

* Tap First Moon Night anniversary → shows a modal with: archetype text, ritual ideas (1–3), permission to add calendar event, share (image or text), and privacy controls.
* Allow user to hide any ritual or archetype text if they prefer purely informational experience.

**Notifications**

* Opt-in only reminders for First Moon Night anniversaries (e.g., “Your First Moon Night is in 3 days — want a private ritual prompt?”). Include quick toggles for push, in-app, or none.

**Accessibility & Literacy**

* Short, plain-language explanations; optional expanded cultural background.
* Icon-only mode off by default. Readable fonts, high contrast option, large tap targets.

---

## 3. Archetypes — mapping to lunar phases

Use 8 canonical lunar phase buckets (matches typical astrology/computation libs):

1. **New Moon** — *The Seed*

   > Quiet, inward, new beginnings. Rituals: journaling intentions, private silence.
   > *Red Witch style*: “Roots night — plant a seed (literal or symbolic).”

2. **Waxing Crescent** — *The Seeker*

   > Curiosity, small steps. Rituals: list three things to try this year.

3. **First Quarter** — *The Challenger*

   > Action, decisions, momentum. Rituals: small boundary-setting exercise.

4. **Waxing Gibbous** — *The Builder* (example archetype for your prompt)

   > Refinement, focused growth, persistence.
   > *UI card text example*: “Waxing Gibbous: You are a Builder. This year, tend what grew from your first Moon. Small acts repeated make structures lasting.”
   > *Ritual suggestions*: light a candle and name one project to protect; a 5-minute gratitude for growth.

5. **Full Moon** — *The Radiant*

   > Culmination, visibility, celebration. Rituals: small public or private celebration.

6. **Waning Gibbous** — *The Healer*

   > Reflection, recovery, sharing. Rituals: release exercise; comfort food recipe card.

7. **Last Quarter** — *The Sage*

   > Re-evaluation, letting go. Rituals: write what no longer serves you.

8. **Waning Crescent** — *The Restorer*

   > Rest, restoration, dreamwork. Rituals: gentle breathwork, sleep intention.

**Naming / Tone:** give option for “mythic” vs “plain” UI copy (mythic = poetic “Builder”, plain = “Growth / Consistency”).

---

## 4. Feature: Moon Sign & Annual First Moon Night

**Moon Sign (one-time derived attribute)**

* Definition: `moon_sign = lunar_phase_at(datetime(first_period_date), location)` (phase bucket as above). Stored as overlay metadata (not altering raw logs).
* Display: Badge + archetype text + 1–3 ritual suggestions.

**First Moon Night (annual recurrence)**

* Create an overlay-only recurring event: `FirstMoonNight` with recurrence rule: annually on calendar date of first_period_date by default.
* Optional mode: align recurrence to **lunar calendar** (same lunar phase each year) — because the lunar cycle ~29.53d moves the phase vs Gregorian date. If chosen, compute the next occurrence that matches the original lunar phase (astronomical computation). Provide both options to user and explain difference in plain language.

**Example UI choice during setup:**

* “Celebrate on the same calendar date every year (e.g., July 11),” or “Celebrate on the same lunar phase each year (e.g., the Full Moon closest to my first night).”
* Default: calendar date (simpler & predictable) with an “advanced” toggle for lunar-phase-aligned recurrence.

---

## 5. Data model / JSON plugin manifest (modular overlay)

This is an example overlay configuration that plugs into your overlays system. It references core data but stores only interpretation metadata.

```json
{
  "overlay_id": "daughters_of_the_moon_v1",
  "display_name": "Daughters of the Moon",
  "type": "cultural",
  "opt_in": true,
  "version": "1.0",
  "default_enabled": false,
  "config_schema": {
    "first_period_date": { "type": "date", "optional": true, "description": "Date of user's first period" },
    "moon_sign_mode": { "type": "enum", "values": ["mythic","plain"], "default": "mythic" },
    "recurrence_mode": { "type": "enum", "values": ["calendar_date", "lunar_phase"], "default": "calendar_date" },
    "reminders_enabled": { "type": "boolean", "default": false }
  },
  "derived_attributes": {
    "moon_sign": { "type": "string", "computed_by": "computeMoonSign(first_period_date, user_location)" },
    "first_moon_anniversary": { "type": "date", "computed_by": "computeAnniversary(first_period_date, recurrence_mode)"}
  },
  "ui": {
    "legend": "Shows your Moon Sign and First Moon Night. Opt-in only. Not a medical tool.",
    "icon": "crescent-glyph",
    "color_token": "overlay-moon-teal"
  },
  "disclaimer": "This overlay provides cultural and reflective content only. It does not replace medical advice."
}
```

**Notes:** overlay stores *only* the date(s) and computed tags; raw cycle logs remain the single source of truth elsewhere.

---

## 6. Pseudocode — how overlay reads core data, computes Moon Sign, and shows events

(Use your app’s astronomical library in production — example uses a hypothetical `astro` lib.)

```
function enableOverlay(user):
  config = loadOverlayConfig(user, "daughters_of_the_moon_v1")
  if not config.first_period_date:
    promptUserForFirstPeriodDate()
  else:
    sign = computeMoonSign(config.first_period_date, user.location)
    saveDerivedAttribute(user.id, "moon_sign", sign)

function computeMoonSign(date, location):
  # use astronomy lib to get moon phase angle: 0-360
  phaseAngle = astro.getMoonPhaseAngle(date, location)
  # convert angle to bucket:
  # 0: New, 0-45: WaxingCrescent, 45-90: FirstQuarter, etc. (use standard mapping)
  return phaseBucketFromAngle(phaseAngle)

function computeAnniversary(first_date, mode):
  if mode == "calendar_date":
    return recurrence(rule="RRULE:FREQ=YEARLY;BYMONTH=month;BYMONTHDAY=day", start=first_date)
  else:
    # find next date each year where moon phase == original phase within +/- N days
    desiredPhase = astro.getMoonPhaseAngle(first_date)
    for yearOffset in 0..100:
      baseline = first_date + yearOffset years
      candidate = astro.findNearestDateWithPhase(baseline, desiredPhase)
      schedule candidate as recurrence for that year
```

**Important**: mark lunar-phase computations as approximate and provide disclosures. Use server-side deterministic astro lib (or an established package) and compute using `user.location` for accuracy.

---

## 7. UI elements & microcopy (legend, disclaimers, cards)

**Overlay Legend (short):**
“Daughters of the Moon: an opt-in cultural layer. Your *Moon Sign* is the lunar phase on the night of your first period. The overlay suggests reflective prompts and an optional annual recurrence. Not medical.”

**Modal header for Moon Sign card:**
“Your Moon Sign — Waxing Gibbous (The Builder)”

**Card body short example:**
“Waxing Gibbous: You are a Builder. This sign honors steady refinement and resilience. Ritual idea: for 5 minutes today, name one thing you will protect this year.”

**Risk/Compliance disclaimer (required per CO-004 & R-CO-001):**
“This overlay is a cultural and reflective tool, not a medical or contraceptive method. If you’re seeking medical guidance about fertility, menstruation, or contraception, consult a qualified healthcare provider.”

---

## 8. Privacy & consent (required behavior)

* Overlay is **opt-in only**. Never enabled by default (CO-002, R-CO-002).
* If user supplies `first_period_date`, store it only in overlay metadata scope (encrypted like other sensitive health data). Do not copy to general notes without explicit consent (CO-006).
* Allow user to: export overlay data, delete overlay (removes derived attributes but not raw logs), configure sharing (if they want to post a First Moon Night graphic).
* Age-sensitivity: if detected user is under an age threshold (app policy), show simplified language and require guardian/age-appropriate flows as per regulatory rules.

Suggested privacy microcopy on save: “Your First Moon Night date is stored with the overlay and can be deleted any time. This date isn’t shared unless you explicitly share a card.”

---

## 9. Accessibility & localization

* Provide two reading tiers: **Short** (1–2 sentences) and **Expanded** (full cultural context).
* Localize archetype names and ritual suggestions with cultural sensitivity.
* Provide alt text for all icons.
* High contrast color tokens and dyslexia-friendly font option.

---

## 10. Visual design tokens (suggested)

* Primary overlay color: `--overlay-moon-teal: #2E9EA8` (use for glyph fills)
* Accent: `--overlay-moon-gold: #F0C05A` (for badges)
* Iconography: 8 lunar glyphs (new, crescent, quarter, gibbous, full, etc.) — simple shapes that scale to 16px.
* Ensure WCAG AA contrast for text on badges; provide alternate outline-only badge for dark mode.

---

## 11. Safety / Compliance checklist (map to your doc requirements)

* CO-001: Overlay reads core logs (no duplication). ✔️
* CO-002: Toggle on/off independently. ✔️
* CO-003: Transparent visual layer + legend. ✔️
* CO-004: Include legend, explanation, and risk disclaimer. ✔️ (copy above)
* CO-005: Modular JSON plugin model included. ✔️
* CO-006: Overlay-only derived attributes; raw data untouched. ✔️
* CO-007: Clear labeling: “cultural/wellness overlay — not a medical method.” ✔️

Also mitigate R-CO-001 and R-CO-003 by surfacing the disclaimer prominently at onboarding and inside the overlay settings.

---

## 12. Developer / engineering notes

* **Compute lunar phase:** use a reliable astronomy library on backend (e.g., `astral`, `pysolar` alternatives or a deterministic in-house lib). Compute with timezone & geolocation for accuracy.
* **Storage:** overlay metadata lives in `overlay_meta` table keyed by `user_id` + `overlay_id`. Encrypt at rest.
* **UI integration:** reuse existing overlay-layer UI (toggles, legends). Add overlay-specific settings page with first_period_date input, recurrence_mode toggle, and reminders toggle.
* **Testing:** unit tests for mapping of phase angle → bucket, for recurrence options (calendar vs lunar), and for privacy flows (delete overlay removes derived attrs).
* **Export/Share:** allow user to share a stylized card (SVG) that includes their Moon Sign and ritual text; do not include `first_period_date` unless user checks a box.

---

## 13. Example archetype copy pack (short — for translation/localization)

Provide mythic and plain versions for each phase. Example (Waxing Gibbous):

* Mythic: “Waxing Gibbous — The Builder. Tends small acts that make great forms.”
* Plain: “Growth & refinement. Focus on improving something you already started.”
* Ritual (short): “Light a candle and name one thing to protect this year.”
* Accessibility alt: “Waxing Gibbous — crescent with bulging lit side.”

---

## 14. Quick implementation checklist (actionable)

1. Add overlay manifest to overlays registry.
2. Implement overlay settings UI (input, toggles).
3. Hook compute function to run whenever first_period_date saved.
4. Show Moon Sign badge on profile header when overlay enabled.
5. Implement First Moon Night recurrence generator (calendar-date default; lunar-phase advanced).
6. Add legend + risk disclaimer text to overlay UI.
7. QA: privacy deletion test + accessibility audit.

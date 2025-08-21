# 1) What to gather **before** writing requirements

As stakeholders of Web Awesome, let's work on answering these questions up front, as it prevents bikeshedding later. These help to frame requirements, and come together on scope, constraints and priorities so we don't overbuild the date picker (or spend too long bickering about features 😊).

* **Primary use cases (pick all that apply):**
 ☐ **Single-date entry** - select one calendar day in a form (birthdate, due date, publish date).
 ☐ **Date-range selection** - picking a start/end window (filters, validity periods, campaigns).
 ☐ **Quick-pick ranges** - fast selection of common windows (Today, Yesterday, Last 7/30, This/Last Month/Quarter).
 ☐ **Inline calendar browsing** - always-visible calendar (dashboards, side panels).
 ☐ **Multiple discrete dates** (optional) - select several non-contiguous days (exceptions, blackout dates).
 ☐ **Date-time composition** (optional) - compose with a time picker; unified commit semantics.
 ☐ **Mobile/touch-first mode** - full-screen or bottom-sheet presentation optimized for touch.
 ☐ **Accessibility-first workflows** - keyboard-only and screen-reader for high-compliance contexts.

* **Interaction model(s) needed**:
  ☐ text input with popup
  ☐ inline calendar
  ☐ modal dialog
  ☐ mobile full-screen
  ☐ all of the above

* **Granularity**:
  ☐ date only
  ☐ date-range
  ☐ date-time (and whether time belongs in a separate component that can compose with the calendar)

* **Internationalization**:
  ☐ locales
  ☐ first-day-of-week
  ☐ week numbers
  ☐ 12/24h preferences
  ☐ RTL
  ☐ which calendars (Gregorian only for v1?)

* **Validation**:
  ☐ min/max
  ☐ disabled rules (weekends/holidays/functions)
  ☐ required
  ☐ parsing/formatting rules
  ☐ free-typing policy

* **Performance constraints**:
  ☐ must work smoothly in forms with 100+ instances?
  ☐ SSR (Server Side Rendering)? (being SSR-safe and progressively enhanced. Don’t break when users do SSR/SSG and degrade gracefully before JS loads)
  ☐ Shadow DOM constraints?

* **Design tokens & theming**:
  ☐ which tokens (radius, spacing, color roles, focus rings) must be consumable
  ☐ dark mode
  ☐ high-contrast mode

* **Accessibility bar (W3C)**:
  ☐ Target WCAG 2.1 AA
  ☐ follow APG patterns (dialog + grid or combobox pattern)

* **API shape**:
  ☐ properties
  ☐ events
  ☐ slots/parts
  ☐ controlled vs uncontrolled value
  ☐ formatting hooks
  ☐ keyboard map

* **Ecosystem fit**:
  ☐ compose with Web Awesome inputs
  ☐ popovers
  ☐ buttons
  ☐ icons
  ☐ form field
  ☐ localization service

* **Testing matrix**:
  ☐ keyboard/screen reader (NVDA, JAWS, VoiceOver)
  ☐ RTL
  ☐ mobile (iOS/Android)
  ☐ high-contrast


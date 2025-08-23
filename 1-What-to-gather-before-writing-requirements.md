# 1) What to gather **before** writing requirements

As stakeholders of Web Awesome, let's work on answering these questions up front, as it prevents bikeshedding later. These help to frame requirements, and come together on scope, constraints and priorities so we don't overbuild the date picker (or spend too long bickering about features 😊).

Note: **APG** = W3C WAI-ARIA Authoring Practices Guide

* **Primary use cases (pick all that apply):**\
 ☐ **Single-date entry** - select one calendar day in a form (birthdate, due date, publish date).\
 ☐ **Date-range selection** - picking a start/end window (filters, validity periods, campaigns).\
 ☐ **Quick-pick ranges** - fast selection of common windows (Today, Yesterday, Last 7/30, This/Last Month/Quarter).\
 ☐ **Inline calendar browsing** - always-visible calendar (dashboards, side panels).\
 ☐ **Multiple discrete dates** (optional) - select several non-contiguous days (exceptions, blackout dates).\
 ☐ **Mobile/touch-first mode** - full-screen or bottom-sheet presentation optimized for touch.\
 ☐ **Accessibility-first workflows** - keyboard-only and screen-reader for high-compliance contexts.

* **Interaction model(s) needed**:\
  ☐ text input with popup\
  ☐ inline calendar\
  ☐ modal dialog\
  ☐ mobile full-screen\
  ☐ all of the above

* **Granularity**:\
  ☐ date only\
  ☐ date-range
  
* **Internationalization**:\
  ☐ locales\
  ☐ first-day-of-week\
  ☐ week numbers\
  ☐ 12/24h preferences\
  ☐ RTL\
  ☐ which calendars (Gregorian only for v1?)

* **Validation**:\
  ☐ min/max\
  ☐ disabled rules (weekends/holidays/functions)\
  ☐ required\
  ☐ parsing/formatting rules\
  ☐ free-typing policy

* **Performance constraints**:\
  ☐ Must work smoothly in forms with 100+ instances\
  ☐ SSR (Server Side Rendering) (can't get these bullets to format properly..)\
  -☐ Make it SSR-safe and progressively enhanced\
  -☐ Don’t break when users do SSR/SSG; degrade gracefully before JS loads\
  -☐ This could be in scope even though we are framework-neutral\
  ☐ Shadow DOM constraints?


* **Design tokens & theming**:\
  ☐ which tokens (radius, spacing, color roles, focus rings) must be consumable\
  ☐ dark mode\
  ☐ high-contrast mode

* **Accessibility bar (W3C)**:\
  ☐ Target WCAG 2.1 AA (accessability) https://www.levelaccess.com/resources/must-have-wcag-2-1-checklist/\
  ☐ follow APG patterns (dialog + grid or combobox pattern)

* **API shape**:\
  ☐ properties\
  ☐ events\
  ☐ slots/parts\
  ☐ controlled vs uncontrolled value\
  ☐ formatting hooks\
  ☐ keyboard map

* **Ecosystem fit**:\
  ☐ compose with Web Awesome inputs\
  ☐ popovers\
  ☐ buttons\
  ☐ icons\
  ☐ form field\
  ☐ localization service

* **Testing matrix**:\
  ☐ keyboard/screen reader (NVDA, JAWS, VoiceOver)\
  ☐ RTL\
  ☐ mobile (iOS/Android)\
  ☐ high-contrast

**Out-of-Scope for this Component:**
  ☐ **Date-time composition** (optional) - compose with a time picker; unified commit semantics.\
  ☐ date-time (and whether time belongs in a separate component that can compose with the calendar)
"Time picker can come later and will be a separate component if we decided to pursue it."

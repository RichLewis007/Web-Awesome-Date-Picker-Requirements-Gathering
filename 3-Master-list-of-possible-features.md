# 3) Master list of possible features (pick what matters)

## Core UX & Interaction

* Text input + popup calendar; inline mode; modal/dialog mode.
* Keyboard support (full APG (W3C WAI-ARIA Authoring Practices Guide) grid + dialog): arrows to move day; PgUp/PgDn month; Shift+PgUp/PgDn year; Home/End row; Esc close; Enter select. (Conform to the W3C WAI-ARIA Authoring Practices Guide)
* Mouse & touch friendly targets; focus trapping in dialog; typeahead for month/year.
* Controlled/uncontrolled value; open/close programmatically.

## Selection modes

* Single date.
* **Range** (with hover-preview between start & end).
* Multiple dates (optional; less common).
* **Month**, **Year**, **Decade** pickers (jump navigation).

## Validation & rules

* Min/max, disabled days, disable functions (e.g., "no weekends/holidays").
* Block out arbitrary sets ('enable'/'disable' by list, ranges, function).
* Commit semantics: immediate vs "confirm" button.
* Free typing with strict parsing + error states (and clear button).

## Calendaring & display

* Multi-month view (1–n columns), month dropdown, year dropdown.
* First day of week; week numbers toggle; today button; clear button. (Week numbers are explicitly referenced in several systems.)
* Show holidays/markers via custom render/slots.
* Timezone awareness (if composing with a time picker / date-time).

## Formatting & i18n

* Locale, numbering system, calendar system (start with **Gregorian**; consider hooks for others later).
* Custom input/output formats; alt display format vs machine format.
* RTL support; alternate day header formats (short/narrow/wide).

## Theming & customization

* Design tokens: radius, gap, spacing, stroke/focus, colors (bg, text, hover, selected, range-preview, disabled).
* CSS Parts/slots for header, nav buttons, month grid, day cells, range start/end, outside-month days.
* Icon slots (prev/next/today/clear); action bar slot.

## API & events

* 'value', 'defaultValue', 'open', 'min', 'max', 'disabledDates', 'firstDayOfWeek', 'showWeekNumbers', 'numberOfMonths', 'selectionMode', 'locale', 'dir', 'confirm'/'commitOnClose', 'presets=[{label, range|date}]', 'renderDay' (templating), 'format', 'parse'.
* Events: 'input', 'change', 'open', 'close', 'month-change', 'year-change', 'invalid', 'confirm', 'range-hover'. (Flatpickr’s event richness is a good reference.)

## Accessibility

* Role/ARIA alignment per APG; labelled fields and instructions; live region for month/year changes; high contrast and focus rings; screen reader announcements for range start/end.
* Combobox pattern parity for input variant.

## Nice quality-of-life extras

* Preset ranges (Today, Yesterday, Last 7/30, This/Last month/quarter).
* "Keep open after selection" and "close on range selection" toggles.
* Auto-apply on blur vs require explicit confirm (configurable).
* Multiple calendars (Buddhist, ISO week date, etc.) — **advanced**.
* Virtualized year/month lists for perf on low-power devices.
* Holiday providers hook.

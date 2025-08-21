# 2) Date Picker Landscape scan - how others do it (highlights)

* WAI-ARIA Authoring Practices document two canonical approaches: a date-picker dialog with grid navigation and a combobox that opens a dialog. Both define concrete keyboard behavior (arrows, PgUp/PgDn to change months/years, Esc to close, etc.). This is the north star for a11y. https://www.w3.org/WAI/ARIA/apg/patterns/dialog-modal/examples/datepicker-dialog/

* Open UI’s Date Picker research aggregates behaviors across major systems; useful as a neutral spec reference when bikeshedding. https://open-ui.org/components/datepicker.research/

* Material UI (MUI X): Desktop vs Mobile variants, strong a11y and keyboard coverage, slot-based subcomponents for extensibility, validation API, and timezone support. Good model for a "composable but opinionated" design. https://mui.com/x/react-date-pickers/date-picker/

* Ant Design: rich picker modes (date/month/quarter/year), confirm-button option (needConfirm) that alters commit semantics. https://ant.design/components/date-picker

* Flatpickr (vanilla JS): small, fast, feature-dense: range mode, multiple months, enable/disable via functions, custom formatter/hooks. Useful benchmark for options density. https://flatpickr.js.org/options/

* PrimeReact: multiple selection modes (single/multiple/range) and explicit keyboard maps in docs; a good public reference for keyboard expectations. https://www.primefaces.org/primereact-v8/calendar/ and https://v9.primereact.org/calendar/

* Kendo/Syncfusion (paid): deep enterprise features (decade navigation depth, templates, date-time and range variants, theming bundles). They set the "power-user" bar. https://www.telerik.com/kendo-jquery-ui/documentation/controls/datepicker/overview and https://demos.telerik.com/kendo-ui/datepicker/index

* FullCalendar (scheduler, not a field widget): shows advanced selection behaviors and API semantics for ranges — relevant if WA ever adds a "big calendar". https://fullcalendar.io/docs

* Carbon (IBM) provides a11y guidance you can mirror for docs. https://carbondesignsystem.com/components/date-picker/accessibility/

# Changelog

## 8.4.0.3

- Migrated the component to FullCalendar 7.0.1 and its Angular-specific plugin entrypoints.
- Added the required `fullcalendar` and `temporal-polyfill` peer dependencies.
- Added the FullCalendar 7 Classic theme and required skeleton styles.
- Migrated removed or renamed v6 options (`buttonText`, `eventClassNames`, and `multiMonthTitleFormat`).
- Kept the public `buttonText` input as a backwards-compatible mapping to FullCalendar 7 buttons.
- Documented the shared component, its inputs, controls, dependencies, and output events.
- Added the official Convertigo 8.4 GitHub Actions and Gradle build resources.

## 8.4.0.1

- Migrated the NGX application and project reference to the Convertigo 8.4 template.
- Made every public calendar input reactive after component initialization.
- Prevented input-change fall-through between locale, events, and initial date.
- Made event updates immutable and safe for missing or previously unknown identifiers.

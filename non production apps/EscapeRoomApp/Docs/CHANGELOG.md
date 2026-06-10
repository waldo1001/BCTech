# Changelog

All notable changes to the BCTalent.EscapeRoom framework are documented here.

---

## [1.4.0.0] - 2026-06-10

### Added

- **Custom Telemetry Events API** — New public `LogCustomEvent` overloads on codeunit 73925 "Escape Room Telemetry" allow room extension apps to emit custom scoring and diagnostic events.
  - Task-scoped and room-scoped variants
  - Optional `ExtraDimensions` parameter for caller-provided custom dimensions
  - Score clamped to -5..+5 to keep leaderboards balanced
  - All custom events use the fixed event name `EscapeRoomCustomEvent` with `EventSource = Custom` dimension
- **Custom Events Overview** KQL query in `LeaderboardQueries.kql` for facilitator auditing
- All scoring KQL queries and dashboard tiles now include `EscapeRoomCustomEvent`

---

## [1.3.x] - Previous releases

Initial framework with seven built-in telemetry events, interface-based venue/room/task system, leaderboard KQL queries, and Azure Data Explorer dashboard.

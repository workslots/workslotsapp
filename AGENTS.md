# WorkSlots Agent Notes

## Timezone behavior

- `userTimeZone` comes from `devUserTz` override or browser timezone.
- `calendarTimeZone` comes from the selected WorkSlots calendar settings.
- A timezone mismatch is when `calendarTimeZone !== userTimeZone`.
- When loading events, API calls use `timeZone: userTimeZone` and day keys are mapped in `userTimeZone`.
- Calendar badges display `slot.start`/`slot.end` directly from `SLOT_TYPES_JSON` (no runtime timezone conversion for label text).
- On sync, slot datetime values are converted from `userTimeZone` to `calendarTimeZone` before insert, and created events use `timeZone: calendarTimeZone`.

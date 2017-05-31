---
title: ThaiBuddhistChronology
---

[java.time.chrono]({{'reference/javadoc/packages/#java.time.chrono' | relative_url }})

# public final class ThaiBuddhistChronology


The Thai Buddhist calendar system.
 <p>
 This chronology defines the rules of the Thai Buddhist calendar system.
 This calendar system is primarily used in Thailand.
 Dates are aligned such that {@code 2484-01-01 (Buddhist)} is {@code 1941-01-01 (ISO)}.
 <p>
 The fields are defined as follows:
 <ul>
 <li>era - There are two eras, the current 'Buddhist' (ERA_BE) and the previous era (ERA_BEFORE_BE).
 <li>year-of-era - The year-of-era for the current era increases uniformly from the epoch at year one.
  For the previous era the year increases from one as time goes backwards.
  The value for the current era is equal to the ISO proleptic-year plus 543.
 <li>proleptic-year - The proleptic year is the same as the year-of-era for the
  current era. For the previous era, years have zero, then negative values.
  The value is equal to the ISO proleptic-year plus 543.
 <li>month-of-year - The ThaiBuddhist month-of-year exactly matches ISO.
 <li>day-of-month - The ThaiBuddhist day-of-month exactly matches ISO.
 <li>day-of-year - The ThaiBuddhist day-of-year exactly matches ISO.
 <li>leap-year - The ThaiBuddhist leap-year pattern exactly matches ISO, such that the two calendars
  are never out of step.
 </ul>
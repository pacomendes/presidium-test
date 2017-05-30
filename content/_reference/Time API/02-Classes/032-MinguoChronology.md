---
title: MinguoChronology
---

[java.time.chrono](../packages/#java.time.chrono)

# public final class MinguoChronology


The Minguo calendar system.
 <p>
 This chronology defines the rules of the Minguo calendar system.
 This calendar system is primarily used in the Republic of China, often known as Taiwan.
 Dates are aligned such that {@code 0001-01-01 (Minguo)} is {@code 1912-01-01 (ISO)}.
 <p>
 The fields are defined as follows:
 <ul>
 <li>era - There are two eras, the current 'Republic' (ERA_ROC) and the previous era (ERA_BEFORE_ROC).
 <li>year-of-era - The year-of-era for the current era increases uniformly from the epoch at year one.
  For the previous era the year increases from one as time goes backwards.
  The value for the current era is equal to the ISO proleptic-year minus 1911.
 <li>proleptic-year - The proleptic year is the same as the year-of-era for the
  current era. For the previous era, years have zero, then negative values.
  The value is equal to the ISO proleptic-year minus 1911.
 <li>month-of-year - The Minguo month-of-year exactly matches ISO.
 <li>day-of-month - The Minguo day-of-month exactly matches ISO.
 <li>day-of-year - The Minguo day-of-year exactly matches ISO.
 <li>leap-year - The Minguo leap-year pattern exactly matches ISO, such that the two calendars
  are never out of step.
 </ul>
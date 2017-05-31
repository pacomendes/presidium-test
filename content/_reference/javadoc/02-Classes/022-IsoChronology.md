---
title: IsoChronology
---

[java.time.chrono]({{'reference/javadoc/packages/#java.time.chrono' | relative_url }})

# public final class IsoChronology


The ISO calendar system.
 <p>
 This chronology defines the rules of the ISO calendar system.
 This calendar system is based on the ISO-8601 standard, which is the
 <i>de facto</i> world calendar.
 <p>
 The fields are defined as follows:
 <ul>
 <li>era - There are two eras, 'Current Era' (CE) and 'Before Current Era' (BCE).
 <li>year-of-era - The year-of-era is the same as the proleptic-year for the current CE era.
  For the BCE era before the ISO epoch the year increases from 1 upwards as time goes backwards.
 <li>proleptic-year - The proleptic year is the same as the year-of-era for the
  current era. For the previous era, years have zero, then negative values.
 <li>month-of-year - There are 12 months in an ISO year, numbered from 1 to 12.
 <li>day-of-month - There are between 28 and 31 days in each of the ISO month, numbered from 1 to 31.
  Months 4, 6, 9 and 11 have 30 days, Months 1, 3, 5, 7, 8, 10 and 12 have 31 days.
  Month 2 has 28 days, or 29 in a leap year.
 <li>day-of-year - There are 365 days in a standard ISO year and 366 in a leap year.
  The days are numbered from 1 to 365 or 1 to 366.
 <li>leap-year - Leap years occur every 4 years, except where the year is divisble by 100 and not divisble by 400.
 </ul>
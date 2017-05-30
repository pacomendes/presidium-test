---
title: WeekFields
---

[java.time.temporal](../packages/#java.time.temporal)

# public final class WeekFields


Localized definitions of the day-of-week, week-of-month and week-of-year fields.
 <p>
 A standard week is seven days long, but cultures have different definitions for some
 other aspects of a week. This class represents the definition of the week, for the
 purpose of providing {@link TemporalField} instances.
 <p>
 WeekFields provides five fields,
 {@link #dayOfWeek()}, {@link #weekOfMonth()}, {@link #weekOfYear()},
 {@link #weekOfWeekBasedYear()}, and {@link #weekBasedYear()}
 that provide access to the values from any {@linkplain Temporal temporal object}.
 <p>
 The computations for day-of-week, week-of-month, and week-of-year are based
 on the  {@linkplain ChronoField#YEAR proleptic-year},
 {@linkplain ChronoField#MONTH_OF_YEAR month-of-year},
 {@linkplain ChronoField#DAY_OF_MONTH day-of-month}, and
 {@linkplain ChronoField#DAY_OF_WEEK ISO day-of-week} which are based on the
 {@linkplain ChronoField#EPOCH_DAY epoch-day} and the chronology.
 The values may not be aligned with the {@linkplain ChronoField#YEAR_OF_ERA year-of-Era}
 depending on the Chronology.
 <p>A week is defined by:
 <ul>
 <li>The first day-of-week.
 For example, the ISO-8601 standard considers Monday to be the first day-of-week.
 <li>The minimal number of days in the first week.
 For example, the ISO-8601 standard counts the first week as needing at least 4 days.
 </ul>
 Together these two values allow a year or month to be divided into weeks.

 <h3>Week of Month</h3>
 One field is used: week-of-month.
 The calculation ensures that weeks never overlap a month boundary.
 The month is divided into periods where each period starts on the defined first day-of-week.
 The earliest period is referred to as week 0 if it has less than the minimal number of days
 and week 1 if it has at least the minimal number of days.

 <table cellpadding="0" cellspacing="3" border="0" style="text-align: left; width: 50%;">
 <caption>Examples of WeekFields</caption>
 <tr><th>Date</th><td>Day-of-week</td>
  <td>First day: Monday<br>Minimal days: 4</td><td>First day: Monday<br>Minimal days: 5</td></tr>
 <tr><th>2008-12-31</th><td>Wednesday</td>
  <td>Week 5 of December 2008</td><td>Week 5 of December 2008</td></tr>
 <tr><th>2009-01-01</th><td>Thursday</td>
  <td>Week 1 of January 2009</td><td>Week 0 of January 2009</td></tr>
 <tr><th>2009-01-04</th><td>Sunday</td>
  <td>Week 1 of January 2009</td><td>Week 0 of January 2009</td></tr>
 <tr><th>2009-01-05</th><td>Monday</td>
  <td>Week 2 of January 2009</td><td>Week 1 of January 2009</td></tr>
 </table>

 <h3>Week of Year</h3>
 One field is used: week-of-year.
 The calculation ensures that weeks never overlap a year boundary.
 The year is divided into periods where each period starts on the defined first day-of-week.
 The earliest period is referred to as week 0 if it has less than the minimal number of days
 and week 1 if it has at least the minimal number of days.

 <h3>Week Based Year</h3>
 Two fields are used for week-based-year, one for the
 {@link #weekOfWeekBasedYear() week-of-week-based-year} and one for
 {@link #weekBasedYear() week-based-year}.  In a week-based-year, each week
 belongs to only a single year.  Week 1 of a year is the first week that
 starts on the first day-of-week and has at least the minimum number of days.
 The first and last weeks of a year may contain days from the
 previous calendar year or next calendar year respectively.

 <table cellpadding="0" cellspacing="3" border="0" style="text-align: left; width: 50%;">
 <caption>Examples of WeekFields for week-based-year</caption>
 <tr><th>Date</th><td>Day-of-week</td>
  <td>First day: Monday<br>Minimal days: 4</td><td>First day: Monday<br>Minimal days: 5</td></tr>
 <tr><th>2008-12-31</th><td>Wednesday</td>
  <td>Week 1 of 2009</td><td>Week 53 of 2008</td></tr>
 <tr><th>2009-01-01</th><td>Thursday</td>
  <td>Week 1 of 2009</td><td>Week 53 of 2008</td></tr>
 <tr><th>2009-01-04</th><td>Sunday</td>
  <td>Week 1 of 2009</td><td>Week 53 of 2008</td></tr>
 <tr><th>2009-01-05</th><td>Monday</td>
  <td>Week 2 of 2009</td><td>Week 1 of 2009</td></tr>
 </table>
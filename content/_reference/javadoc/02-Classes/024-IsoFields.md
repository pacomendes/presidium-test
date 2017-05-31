---
title: IsoFields
---

[java.time.temporal]({{'reference/javadoc/packages/#java.time.temporal' | relative_url }})

# public final class IsoFields


Fields and units specific to the ISO-8601 calendar system,
 including quarter-of-year and week-based-year.
 <p>
 This class defines fields and units that are specific to the ISO calendar system.

 <h3>Quarter of year</h3>
 The ISO-8601 standard is based on the standard civic 12 month year.
 This is commonly divided into four quarters, often abbreviated as Q1, Q2, Q3 and Q4.
 <p>
 January, February and March are in Q1.
 April, May and June are in Q2.
 July, August and September are in Q3.
 October, November and December are in Q4.
 <p>
 The complete date is expressed using three fields:
 <ul>
 <li>{@link #DAY_OF_QUARTER DAY_OF_QUARTER} - the day within the quarter, from 1 to 90, 91 or 92
 <li>{@link #QUARTER_OF_YEAR QUARTER_OF_YEAR} - the week within the week-based-year
 <li>{@link ChronoField#YEAR YEAR} - the standard ISO year
 </ul>

 <h3>Week based years</h3>
 The ISO-8601 standard was originally intended as a data interchange format,
 defining a string format for dates and times. However, it also defines an
 alternate way of expressing the date, based on the concept of week-based-year.
 <p>
 The date is expressed using three fields:
 <ul>
 <li>{@link ChronoField#DAY_OF_WEEK DAY_OF_WEEK} - the standard field defining the
  day-of-week from Monday (1) to Sunday (7)
 <li>{@link #WEEK_OF_WEEK_BASED_YEAR} - the week within the week-based-year
 <li>{@link #WEEK_BASED_YEAR WEEK_BASED_YEAR} - the week-based-year
 </ul>
 The week-based-year itself is defined relative to the standard ISO proleptic year.
 It differs from the standard year in that it always starts on a Monday.
 <p>
 The first week of a week-based-year is the first Monday-based week of the standard
 ISO year that has at least 4 days in the new year.
 <ul>
 <li>If January 1st is Monday then week 1 starts on January 1st
 <li>If January 1st is Tuesday then week 1 starts on December 31st of the previous standard year
 <li>If January 1st is Wednesday then week 1 starts on December 30th of the previous standard year
 <li>If January 1st is Thursday then week 1 starts on December 29th of the previous standard year
 <li>If January 1st is Friday then week 1 starts on January 4th
 <li>If January 1st is Saturday then week 1 starts on January 3rd
 <li>If January 1st is Sunday then week 1 starts on January 2nd
 </ul>
 There are 52 weeks in most week-based years, however on occasion there are 53 weeks.
 <p>
 For example:

 <table cellpadding="0" cellspacing="3" border="0" style="text-align: left; width: 50%;">
 <caption>Examples of Week based Years</caption>
 <tr><th>Date</th><th>Day-of-week</th><th>Field values</th></tr>
 <tr><th>2008-12-28</th><td>Sunday</td><td>Week 52 of week-based-year 2008</td></tr>
 <tr><th>2008-12-29</th><td>Monday</td><td>Week 1 of week-based-year 2009</td></tr>
 <tr><th>2008-12-31</th><td>Wednesday</td><td>Week 1 of week-based-year 2009</td></tr>
 <tr><th>2009-01-01</th><td>Thursday</td><td>Week 1 of week-based-year 2009</td></tr>
 <tr><th>2009-01-04</th><td>Sunday</td><td>Week 1 of week-based-year 2009</td></tr>
 <tr><th>2009-01-05</th><td>Monday</td><td>Week 2 of week-based-year 2009</td></tr>
 </table>
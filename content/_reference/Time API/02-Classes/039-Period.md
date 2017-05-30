---
title: Period
---

[java.time](../packages/#java.time)

# public final class Period


A date-based amount of time in the ISO-8601 calendar system,
 such as '2 years, 3 months and 4 days'.
 <p>
 This class models a quantity or amount of time in terms of years, months and days.
 See {@link Duration} for the time-based equivalent to this class.
 <p>
 Durations and periods differ in their treatment of daylight savings time
 when added to {@link ZonedDateTime}. A {@code Duration} will add an exact
 number of seconds, thus a duration of one day is always exactly 24 hours.
 By contrast, a {@code Period} will add a conceptual day, trying to maintain
 the local time.
 <p>
 For example, consider adding a period of one day and a duration of one day to
 18:00 on the evening before a daylight savings gap. The {@code Period} will add
 the conceptual day and result in a {@code ZonedDateTime} at 18:00 the following day.
 By contrast, the {@code Duration} will add exactly 24 hours, resulting in a
 {@code ZonedDateTime} at 19:00 the following day (assuming a one hour DST gap).
 <p>
 The supported units of a period are {@link ChronoUnit#YEARS YEARS},
 {@link ChronoUnit#MONTHS MONTHS} and {@link ChronoUnit#DAYS DAYS}.
 All three fields are always present, but may be set to zero.
 <p>
 The ISO-8601 calendar system is the modern civil calendar system used today
 in most of the world. It is equivalent to the proleptic Gregorian calendar
 system, in which today's rules for leap years are applied for all time.
 <p>
 The period is modeled as a directed amount of time, meaning that individual parts of the
 period may be negative.

 <p>
 This is a <a href="{@docRoot}/java/lang/doc-files/ValueBased.html">value-based</a>
 class; use of identity-sensitive operations (including reference equality
 ({@code ==}), identity hash code, or synchronization) on instances of
 {@code Period} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
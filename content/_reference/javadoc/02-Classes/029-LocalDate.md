---
title: LocalDate
---

[java.time]({{'reference/javadoc/packages/#java.time' | relative_url }})

# public final class LocalDate


A date without a time-zone in the ISO-8601 calendar system,
 such as {@code 2007-12-03}.
 <p>
 {@code LocalDate} is an immutable date-time object that represents a date,
 often viewed as year-month-day. Other date fields, such as day-of-year,
 day-of-week and week-of-year, can also be accessed.
 For example, the value "2nd October 2007" can be stored in a {@code LocalDate}.
 <p>
 This class does not store or represent a time or time-zone.
 Instead, it is a description of the date, as used for birthdays.
 It cannot represent an instant on the time-line without additional information
 such as an offset or time-zone.
 <p>
 The ISO-8601 calendar system is the modern civil calendar system used today
 in most of the world. It is equivalent to the proleptic Gregorian calendar
 system, in which today's rules for leap years are applied for all time.
 For most applications written today, the ISO-8601 rules are entirely suitable.
 However, any application that makes use of historical dates, and requires them
 to be accurate will find the ISO-8601 approach unsuitable.

 <p>
 This is a <a href="{@docRoot}/java/lang/doc-files/ValueBased.html">value-based</a>
 class; use of identity-sensitive operations (including reference equality
 ({@code ==}), identity hash code, or synchronization) on instances of
 {@code LocalDate} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
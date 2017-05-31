---
title: YearMonth
---

[java.time]({{'reference/javadoc/packages/#java.time' | relative_url }})

# public final class YearMonth


A year-month in the ISO-8601 calendar system, such as {@code 2007-12}.
 <p>
 {@code YearMonth} is an immutable date-time object that represents the combination
 of a year and month. Any field that can be derived from a year and month, such as
 quarter-of-year, can be obtained.
 <p>
 This class does not store or represent a day, time or time-zone.
 For example, the value "October 2007" can be stored in a {@code YearMonth}.
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
 {@code YearMonth} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
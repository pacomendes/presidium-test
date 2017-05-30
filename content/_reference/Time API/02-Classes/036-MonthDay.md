---
title: MonthDay
---

[java.time](../packages/#java.time)

# public final class MonthDay


A month-day in the ISO-8601 calendar system, such as {@code --12-03}.
 <p>
 {@code MonthDay} is an immutable date-time object that represents the combination
 of a month and day-of-month. Any field that can be derived from a month and day,
 such as quarter-of-year, can be obtained.
 <p>
 This class does not store or represent a year, time or time-zone.
 For example, the value "December 3rd" can be stored in a {@code MonthDay}.
 <p>
 Since a {@code MonthDay} does not possess a year, the leap day of
 February 29th is considered valid.
 <p>
 This class implements {@link TemporalAccessor} rather than {@link Temporal}.
 This is because it is not possible to define whether February 29th is valid or not
 without external information, preventing the implementation of plus/minus.
 Related to this, {@code MonthDay} only provides access to query and set the fields
 {@code MONTH_OF_YEAR} and {@code DAY_OF_MONTH}.
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
 {@code MonthDay} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
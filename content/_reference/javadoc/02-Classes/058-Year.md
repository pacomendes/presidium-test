---
title: Year
---

[java.time]({{'reference/javadoc/packages/#java.time' | relative_url }})

# public final class Year


A year in the ISO-8601 calendar system, such as {@code 2007}.
 <p>
 {@code Year} is an immutable date-time object that represents a year.
 Any field that can be derived from a year can be obtained.
 <p>
 <b>Note that years in the ISO chronology only align with years in the
 Gregorian-Julian system for modern years. Parts of Russia did not switch to the
 modern Gregorian/ISO rules until 1920.
 As such, historical years must be treated with caution.</b>
 <p>
 This class does not store or represent a month, day, time or time-zone.
 For example, the value "2007" can be stored in a {@code Year}.
 <p>
 Years represented by this class follow the ISO-8601 standard and use
 the proleptic numbering system. Year 1 is preceded by year 0, then by year -1.
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
 {@code Year} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
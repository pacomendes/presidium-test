---
title: LocalTime
---

[java.time]({{'reference/javadoc/packages/#java.time' | relative_url }})

# public final class LocalTime


A time without a time-zone in the ISO-8601 calendar system,
 such as {@code 10:15:30}.
 <p>
 {@code LocalTime} is an immutable date-time object that represents a time,
 often viewed as hour-minute-second.
 Time is represented to nanosecond precision.
 For example, the value "13:45.30.123456789" can be stored in a {@code LocalTime}.
 <p>
 This class does not store or represent a date or time-zone.
 Instead, it is a description of the local time as seen on a wall clock.
 It cannot represent an instant on the time-line without additional information
 such as an offset or time-zone.
 <p>
 The ISO-8601 calendar system is the modern civil calendar system used today
 in most of the world. This API assumes that all calendar systems use the same
 representation, this class, for time-of-day.

 <p>
 This is a <a href="{@docRoot}/java/lang/doc-files/ValueBased.html">value-based</a>
 class; use of identity-sensitive operations (including reference equality
 ({@code ==}), identity hash code, or synchronization) on instances of
 {@code LocalTime} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
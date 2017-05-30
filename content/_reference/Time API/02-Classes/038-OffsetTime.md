---
title: OffsetTime
---

[java.time](../packages/#java.time)

# public final class OffsetTime


A time with an offset from UTC/Greenwich in the ISO-8601 calendar system,
 such as {@code 10:15:30+01:00}.
 <p>
 {@code OffsetTime} is an immutable date-time object that represents a time, often
 viewed as hour-minute-second-offset.
 This class stores all time fields, to a precision of nanoseconds,
 as well as a zone offset.
 For example, the value "13:45.30.123456789+02:00" can be stored
 in an {@code OffsetTime}.

 <p>
 This is a <a href="{@docRoot}/java/lang/doc-files/ValueBased.html">value-based</a>
 class; use of identity-sensitive operations (including reference equality
 ({@code ==}), identity hash code, or synchronization) on instances of
 {@code OffsetTime} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
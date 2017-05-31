---
title: ZoneOffset
---

[java.time]({{'reference/javadoc/packages/#java.time' | relative_url }})

# public final class ZoneOffset


A time-zone offset from Greenwich/UTC, such as {@code +02:00}.
 <p>
 A time-zone offset is the amount of time that a time-zone differs from Greenwich/UTC.
 This is usually a fixed number of hours and minutes.
 <p>
 Different parts of the world have different time-zone offsets.
 The rules for how offsets vary by place and time of year are captured in the
 {@link ZoneId} class.
 <p>
 For example, Paris is one hour ahead of Greenwich/UTC in winter and two hours
 ahead in summer. The {@code ZoneId} instance for Paris will reference two
 {@code ZoneOffset} instances - a {@code +01:00} instance for winter,
 and a {@code +02:00} instance for summer.
 <p>
 In 2008, time-zone offsets around the world extended from -12:00 to +14:00.
 To prevent any problems with that range being extended, yet still provide
 validation, the range of offsets is restricted to -18:00 to 18:00 inclusive.
 <p>
 This class is designed for use with the ISO calendar system.
 The fields of hours, minutes and seconds make assumptions that are valid for the
 standard ISO definitions of those fields. This class may be used with other
 calendar systems providing the definition of the time fields matches those
 of the ISO calendar system.
 <p>
 Instances of {@code ZoneOffset} must be compared using {@link #equals}.
 Implementations may choose to cache certain common offsets, however
 applications must not rely on such caching.

 <p>
 This is a <a href="{@docRoot}/java/lang/doc-files/ValueBased.html">value-based</a>
 class; use of identity-sensitive operations (including reference equality
 ({@code ==}), identity hash code, or synchronization) on instances of
 {@code ZoneOffset} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
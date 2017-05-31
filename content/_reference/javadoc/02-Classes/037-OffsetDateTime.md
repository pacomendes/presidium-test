---
title: OffsetDateTime
---

[java.time]({{'reference/javadoc/packages/#java.time' | relative_url }})

# public final class OffsetDateTime


A date-time with an offset from UTC/Greenwich in the ISO-8601 calendar system,
 such as {@code 2007-12-03T10:15:30+01:00}.
 <p>
 {@code OffsetDateTime} is an immutable representation of a date-time with an offset.
 This class stores all date and time fields, to a precision of nanoseconds,
 as well as the offset from UTC/Greenwich. For example, the value
 "2nd October 2007 at 13:45.30.123456789 +02:00" can be stored in an {@code OffsetDateTime}.
 <p>
 {@code OffsetDateTime}, {@link ZonedDateTime} and {@link Instant} all store an instant
 on the time-line to nanosecond precision.
 {@code Instant} is the simplest, simply representing the instant.
 {@code OffsetDateTime} adds to the instant the offset from UTC/Greenwich, which allows
 the local date-time to be obtained.
 {@code ZonedDateTime} adds full time-zone rules.
 <p>
 It is intended that {@code ZonedDateTime} or {@code Instant} is used to model data
 in simpler applications. This class may be used when modeling date-time concepts in
 more detail, or when communicating to a database or in a network protocol.

 <p>
 This is a <a href="{@docRoot}/java/lang/doc-files/ValueBased.html">value-based</a>
 class; use of identity-sensitive operations (including reference equality
 ({@code ==}), identity hash code, or synchronization) on instances of
 {@code OffsetDateTime} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
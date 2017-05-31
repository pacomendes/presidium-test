---
title: ChronoLocalDateTime
---

[java.time.chrono]({{'reference/javadoc/packages/#java.time.chrono' | relative_url }})

# public interface ChronoLocalDateTime


A date-time without a time-zone in an arbitrary chronology, intended
 for advanced globalization use cases.
 <p>
 <b>Most applications should declare method signatures, fields and variables
 as {@link LocalDateTime}, not this interface.</b>
 <p>
 A {@code ChronoLocalDateTime} is the abstract representation of a local date-time
 where the {@code Chronology chronology}, or calendar system, is pluggable.
 The date-time is defined in terms of fields expressed by {@link TemporalField},
 where most common implementations are defined in {@link ChronoField}.
 The chronology defines how the calendar system operates and the meaning of
 the standard fields.

 <h3>When to use this interface</h3>
 The design of the API encourages the use of {@code LocalDateTime} rather than this
 interface, even in the case where the application needs to deal with multiple
 calendar systems. The rationale for this is explored in detail in {@link ChronoLocalDate}.
 <p>
 Ensure that the discussion in {@code ChronoLocalDate} has been read and understood
 before using this interface.
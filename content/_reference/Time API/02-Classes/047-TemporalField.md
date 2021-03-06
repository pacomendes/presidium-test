---
title: TemporalField
---

[java.time.temporal](../packages/#java.time.temporal)

# public interface TemporalField


A field of date-time, such as month-of-year or hour-of-minute.
 <p>
 Date and time is expressed using fields which partition the time-line into something
 meaningful for humans. Implementations of this interface represent those fields.
 <p>
 The most commonly used units are defined in {@link ChronoField}.
 Further fields are supplied in {@link IsoFields}, {@link WeekFields} and {@link JulianFields}.
 Fields can also be written by application code by implementing this interface.
 <p>
 The field works using double dispatch. Client code calls methods on a date-time like
 {@code LocalDateTime} which check if the field is a {@code ChronoField}.
 If it is, then the date-time must handle it.
 Otherwise, the method call is re-dispatched to the matching method in this interface.
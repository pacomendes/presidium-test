---
title: TemporalAccessor
---

[java.time.temporal]({{'reference/javadoc/packages/#java.time.temporal' | relative_url }})

# public interface TemporalAccessor


Framework-level interface defining read-only access to a temporal object,
 such as a date, time, offset or some combination of these.
 <p>
 This is the base interface type for date, time and offset objects.
 It is implemented by those classes that can provide information
 as {@linkplain TemporalField fields} or {@linkplain TemporalQuery queries}.
 <p>
 Most date and time information can be represented as a number.
 These are modeled using {@code TemporalField} with the number held using
 a {@code long} to handle large values. Year, month and day-of-month are
 simple examples of fields, but they also include instant and offsets.
 See {@link ChronoField} for the standard set of fields.
 <p>
 Two pieces of date/time information cannot be represented by numbers,
 the {@linkplain Chronology chronology} and the
 {@linkplain ZoneId time-zone}.
 These can be accessed via {@linkplain #query(TemporalQuery) queries} using
 the static methods defined on {@link TemporalQuery}.
 <p>
 A sub-interface, {@link Temporal}, extends this definition to one that also
 supports adjustment and manipulation on more complete temporal objects.
 <p>
 This interface is a framework-level interface that should not be widely
 used in application code. Instead, applications should create and pass
 around instances of concrete types, such as {@code LocalDate}.
 There are many reasons for this, part of which is that implementations
 of this interface may be in calendar systems other than ISO.
 See {@link ChronoLocalDate} for a fuller discussion of the issues.
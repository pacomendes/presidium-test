---
title: Chronology
---

[java.time.chrono](../packages/#java.time.chrono)

# public interface Chronology


A calendar system, used to organize and identify dates.
 <p>
 The main date and time API is built on the ISO calendar system.
 The chronology operates behind the scenes to represent the general concept of a calendar system.
 For example, the Japanese, Minguo, Thai Buddhist and others.
 <p>
 Most other calendar systems also operate on the shared concepts of year, month and day,
 linked to the cycles of the Earth around the Sun, and the Moon around the Earth.
 These shared concepts are defined by {@link ChronoField} and are available
 for use by any {@code Chronology} implementation:
 <pre>
   LocalDate isoDate = ...
   ThaiBuddhistDate thaiDate = ...
   int isoYear = isoDate.get(ChronoField.YEAR);
   int thaiYear = thaiDate.get(ChronoField.YEAR);
 </pre>
 As shown, although the date objects are in different calendar systems, represented by different
 {@code Chronology} instances, both can be queried using the same constant on {@code ChronoField}.
 For a full discussion of the implications of this, see {@link ChronoLocalDate}.
 In general, the advice is to use the known ISO-based {@code LocalDate}, rather than
 {@code ChronoLocalDate}.
 <p>
 While a {@code Chronology} object typically uses {@code ChronoField} and is based on
 an era, year-of-era, month-of-year, day-of-month model of a date, this is not required.
 A {@code Chronology} instance may represent a totally different kind of calendar system,
 such as the Mayan.
 <p>
 In practical terms, the {@code Chronology} instance also acts as a factory.
 The {@link #of(String)} method allows an instance to be looked up by identifier,
 while the {@link #ofLocale(Locale)} method allows lookup by locale.
 <p>
 The {@code Chronology} instance provides a set of methods to create {@code ChronoLocalDate} instances.
 The date classes are used to manipulate specific dates.
 <ul>
 <li> {@link #dateNow() dateNow()}
 <li> {@link #dateNow(Clock) dateNow(clock)}
 <li> {@link #dateNow(ZoneId) dateNow(zone)}
 <li> {@link #date(int, int, int) date(yearProleptic, month, day)}
 <li> {@link #date(Era, int, int, int) date(era, yearOfEra, month, day)}
 <li> {@link #dateYearDay(int, int) dateYearDay(yearProleptic, dayOfYear)}
 <li> {@link #dateYearDay(Era, int, int) dateYearDay(era, yearOfEra, dayOfYear)}
 <li> {@link #date(TemporalAccessor) date(TemporalAccessor)}
 </ul>

 <h3 id="addcalendars">Adding New Calendars</h3>
 The set of available chronologies can be extended by applications.
 Adding a new calendar system requires the writing of an implementation of
 {@code Chronology}, {@code ChronoLocalDate} and {@code Era}.
 The majority of the logic specific to the calendar system will be in the
 {@code ChronoLocalDate} implementation.
 The {@code Chronology} implementation acts as a factory.
 <p>
 To permit the discovery of additional chronologies, the {@link java.util.ServiceLoader ServiceLoader}
 is used. A file must be added to the {@code META-INF/services} directory with the
 name 'java.time.chrono.Chronology' listing the implementation classes.
 See the ServiceLoader for more details on service loading.
 For lookup by id or calendarType, the system provided calendars are found
 first followed by application provided calendars.
 <p>
 Each chronology must define a chronology ID that is unique within the system.
 If the chronology represents a calendar system defined by the
 CLDR specification then the calendar type is the concatenation of the
 CLDR type and, if applicable, the CLDR variant,
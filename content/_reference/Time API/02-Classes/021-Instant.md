---
title: Instant
---

[java.time](../packages/#java.time)

# public final class Instant


An instantaneous point on the time-line.
 <p>
 This class models a single instantaneous point on the time-line.
 This might be used to record event time-stamps in the application.
 <p>
 The range of an instant requires the storage of a number larger than a {@code long}.
 To achieve this, the class stores a {@code long} representing epoch-seconds and an
 {@code int} representing nanosecond-of-second, which will always be between 0 and 999,999,999.
 The epoch-seconds are measured from the standard Java epoch of {@code 1970-01-01T00:00:00Z}
 where instants after the epoch have positive values, and earlier instants have negative values.
 For both the epoch-second and nanosecond parts, a larger value is always later on the time-line
 than a smaller value.

 <h3>Time-scale</h3>
 <p>
 The length of the solar day is the standard way that humans measure time.
 This has traditionally been subdivided into 24 hours of 60 minutes of 60 seconds,
 forming a 86400 second day.
 <p>
 Modern timekeeping is based on atomic clocks which precisely define an SI second
 relative to the transitions of a Caesium atom. The length of an SI second was defined
 to be very close to the 86400th fraction of a day.
 <p>
 Unfortunately, as the Earth rotates the length of the day varies.
 In addition, over time the average length of the day is getting longer as the Earth slows.
 As a result, the length of a solar day in 2012 is slightly longer than 86400 SI seconds.
 The actual length of any given day and the amount by which the Earth is slowing
 are not predictable and can only be determined by measurement.
 The UT1 time-scale captures the accurate length of day, but is only available some
 time after the day has completed.
 <p>
 The UTC time-scale is a standard approach to bundle up all the additional fractions
 of a second from UT1 into whole seconds, known as <i>leap-seconds</i>.
 A leap-second may be added or removed depending on the Earth's rotational changes.
 As such, UTC permits a day to have 86399 SI seconds or 86401 SI seconds where
 necessary in order to keep the day aligned with the Sun.
 <p>
 The modern UTC time-scale was introduced in 1972, introducing the concept of whole leap-seconds.
 Between 1958 and 1972, the definition of UTC was complex, with minor sub-second leaps and
 alterations to the length of the notional second. As of 2012, discussions are underway
 to change the definition of UTC again, with the potential to remove leap seconds or
 introduce other changes.
 <p>
 Given the complexity of accurate timekeeping described above, this Java API defines
 its own time-scale, the <i>Java Time-Scale</i>.
 <p>
 The Java Time-Scale divides each calendar day into exactly 86400
 subdivisions, known as seconds.  These seconds may differ from the
 SI second.  It closely matches the de facto international civil time
 scale, the definition of which changes from time to time.
 <p>
 The Java Time-Scale has slightly different definitions for different
 segments of the time-line, each based on the consensus international
 time scale that is used as the basis for civil time. Whenever the
 internationally-agreed time scale is modified or replaced, a new
 segment of the Java Time-Scale must be defined for it.  Each segment
 must meet these requirements:
 <ul>
 <li>the Java Time-Scale shall closely match the underlying international
  civil time scale;</li>
 <li>the Java Time-Scale shall exactly match the international civil
  time scale at noon each day;</li>
 <li>the Java Time-Scale shall have a precisely-defined relationship to
  the international civil time scale.</li>
 </ul>
 There are currently, as of 2013, two segments in the Java time-scale.
 <p>
 For the segment from 1972-11-03 (exact boundary discussed below) until
 further notice, the consensus international time scale is UTC (with
 leap seconds).  In this segment, the Java Time-Scale is identical to
 <a href="http://www.cl.cam.ac.uk/~mgk25/time/utc-sls/">UTC-SLS</a>.
 This is identical to UTC on days that do not have a leap second.
 On days that do have a leap second, the leap second is spread equally
 over the last 1000 seconds of the day, maintaining the appearance of
 exactly 86400 seconds per day.
 <p>
 For the segment prior to 1972-11-03, extending back arbitrarily far,
 the consensus international time scale is defined to be UT1, applied
 proleptically, which is equivalent to the (mean) solar time on the
 prime meridian (Greenwich). In this segment, the Java Time-Scale is
 identical to the consensus international time scale. The exact
 boundary between the two segments is the instant where UT1 = UTC
 between 1972-11-03T00:00 and 1972-11-04T12:00.
 <p>
 Implementations of the Java time-scale using the JSR-310 API are not
 required to provide any clock that is sub-second accurate, or that
 progresses monotonically or smoothly. Implementations are therefore
 not required to actually perform the UTC-SLS slew or to otherwise be
 aware of leap seconds. JSR-310 does, however, require that
 implementations must document the approach they use when defining a
 clock representing the current instant.
 See {@link Clock} for details on the available clocks.
 <p>
 The Java time-scale is used for all date-time classes.
 This includes {@code Instant}, {@code LocalDate}, {@code LocalTime}, {@code OffsetDateTime},
 {@code ZonedDateTime} and {@code Duration}.

 <p>
 This is a <a href="{@docRoot}/java/lang/doc-files/ValueBased.html">value-based</a>
 class; use of identity-sensitive operations (including reference equality
 ({@code ==}), identity hash code, or synchronization) on instances of
 {@code Instant} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
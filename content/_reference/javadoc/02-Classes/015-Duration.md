---
title: Duration
---

[java.time]({{'reference/javadoc/packages/#java.time' | relative_url }})

# public final class Duration


A time-based amount of time, such as '34.5 seconds'.
 <p>
 This class models a quantity or amount of time in terms of seconds and nanoseconds.
 It can be accessed using other duration-based units, such as minutes and hours.
 In addition, the {@link ChronoUnit#DAYS DAYS} unit can be used and is treated as
 exactly equal to 24 hours, thus ignoring daylight savings effects.
 See {@link Period} for the date-based equivalent to this class.
 <p>
 A physical duration could be of infinite length.
 For practicality, the duration is stored with constraints similar to {@link Instant}.
 The duration uses nanosecond resolution with a maximum value of the seconds that can
 be held in a {@code long}. This is greater than the current estimated age of the universe.
 <p>
 The range of a duration requires the storage of a number larger than a {@code long}.
 To achieve this, the class stores a {@code long} representing seconds and an {@code int}
 representing nanosecond-of-second, which will always be between 0 and 999,999,999.
 The model is of a directed duration, meaning that the duration may be negative.
 <p>
 The duration is measured in "seconds", but these are not necessarily identical to
 the scientific "SI second" definition based on atomic clocks.
 This difference only impacts durations measured near a leap-second and should not affect
 most applications.
 See {@link Instant} for a discussion as to the meaning of the second and time-scales.

 <p>
 This is a <a href="{@docRoot}/java/lang/doc-files/ValueBased.html">value-based</a>
 class; use of identity-sensitive operations (including reference equality
 ({@code ==}), identity hash code, or synchronization) on instances of
 {@code Duration} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
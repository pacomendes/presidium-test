---
title: HijrahDate
---

[java.time.chrono]({{'reference/javadoc/packages/#java.time.chrono' | relative_url }})

# public final class HijrahDate


A date in the Hijrah calendar system.
 <p>
 This date operates using one of several variants of the
 {@linkplain HijrahChronology Hijrah calendar}.
 <p>
 The Hijrah calendar has a different total of days in a year than
 Gregorian calendar, and the length of each month is based on the period
 of a complete revolution of the moon around the earth
 (as between successive new moons).
 Refer to the {@link HijrahChronology} for details of supported variants.
 <p>
 Each HijrahDate is created bound to a particular HijrahChronology,
 The same chronology is propagated to each HijrahDate computed from the date.
 To use a different Hijrah variant, its HijrahChronology can be used
 to create new HijrahDate instances.
 Alternatively, the {@link #withVariant} method can be used to convert
 to a new HijrahChronology.

 <p>
 This is a <a href="{@docRoot}/java/lang/doc-files/ValueBased.html">value-based</a>
 class; use of identity-sensitive operations (including reference equality
 ({@code ==}), identity hash code, or synchronization) on instances of
 {@code HijrahDate} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
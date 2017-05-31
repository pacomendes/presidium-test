---
title: JapaneseChronology
---

[java.time.chrono]({{'reference/javadoc/packages/#java.time.chrono' | relative_url }})

# public final class JapaneseChronology


The Japanese Imperial calendar system.
 <p>
 This chronology defines the rules of the Japanese Imperial calendar system.
 This calendar system is primarily used in Japan.
 The Japanese Imperial calendar system is the same as the ISO calendar system
 apart from the era-based year numbering.
 <p>
 Japan introduced the Gregorian calendar starting with Meiji 6.
 Only Meiji and later eras are supported;
 dates before Meiji 6, January 1 are not supported.
 <p>
 The supported {@code ChronoField} instances are:
 <ul>
 <li>{@code DAY_OF_WEEK}
 <li>{@code DAY_OF_MONTH}
 <li>{@code DAY_OF_YEAR}
 <li>{@code EPOCH_DAY}
 <li>{@code MONTH_OF_YEAR}
 <li>{@code PROLEPTIC_MONTH}
 <li>{@code YEAR_OF_ERA}
 <li>{@code YEAR}
 <li>{@code ERA}
 </ul>
---
title: JapaneseDate
---

[java.time.chrono]({{'reference/javadoc/packages/#java.time.chrono' | relative_url }})

# public final class JapaneseDate


A date in the Japanese Imperial calendar system.
 <p>
 This date operates using the {@linkplain JapaneseChronology Japanese Imperial calendar}.
 This calendar system is primarily used in Japan.
 <p>
 The Japanese Imperial calendar system is the same as the ISO calendar system
 apart from the era-based year numbering. The proleptic-year is defined to be
 equal to the ISO proleptic-year.
 <p>
 Japan introduced the Gregorian calendar starting with Meiji 6.
 Only Meiji and later eras are supported;
 dates before Meiji 6, January 1 are not supported.
 <p>
 For example, the Japanese year "Heisei 24" corresponds to ISO year "2012".<br>
 Calling {@code japaneseDate.get(YEAR_OF_ERA)} will return 24.<br>
 Calling {@code japaneseDate.get(YEAR)} will return 2012.<br>
 Calling {@code japaneseDate.get(ERA)} will return 2, corresponding to
 {@code JapaneseChronology.ERA_HEISEI}.<br>

 <p>
 This is a <a href="{@docRoot}/java/lang/doc-files/ValueBased.html">value-based</a>
 class; use of identity-sensitive operations (including reference equality
 ({@code ==}), identity hash code, or synchronization) on instances of
 {@code JapaneseDate} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
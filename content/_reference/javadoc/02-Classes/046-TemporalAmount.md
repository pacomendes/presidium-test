---
title: TemporalAmount
---

[java.time.temporal]({{'reference/javadoc/packages/#java.time.temporal' | relative_url }})

# public interface TemporalAmount


Framework-level interface defining an amount of time, such as
 "6 hours", "8 days" or "2 years and 3 months".
 <p>
 This is the base interface type for amounts of time.
 An amount is distinct from a date or time-of-day in that it is not tied
 to any specific point on the time-line.
 <p>
 The amount can be thought of as a {@code Map} of {@link TemporalUnit} to
 {@code long}, exposed via {@link #getUnits()} and {@link #get(TemporalUnit)}.
 A simple case might have a single unit-value pair, such as "6 hours".
 A more complex case may have multiple unit-value pairs, such as
 "7 years, 3 months and 5 days".
 <p>
 There are two common implementations.
 {@link Period} is a date-based implementation, storing years, months and days.
 {@link Duration} is a time-based implementation, storing seconds and nanoseconds,
 but providing some access using other duration based units such as minutes,
 hours and fixed 24-hour days.
 <p>
 This interface is a framework-level interface that should not be widely
 used in application code. Instead, applications should create and pass
 around instances of concrete types, such as {@code Period} and {@code Duration}.
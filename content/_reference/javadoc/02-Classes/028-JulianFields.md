---
title: JulianFields
---

[java.time.temporal]({{'reference/javadoc/packages/#java.time.temporal' | relative_url }})

# public final class JulianFields


A set of date fields that provide access to Julian Days.
 <p>
 The Julian Day is a standard way of expressing date and time commonly used in the scientific community.
 It is expressed as a decimal number of whole days where days start at midday.
 This class represents variations on Julian Days that count whole days from midnight.
 <p>
 The fields are implemented relative to {@link ChronoField#EPOCH_DAY EPOCH_DAY}.
 The fields are supported, and can be queried and set if {@code EPOCH_DAY} is available.
 The fields work with all chronologies.
---
title: ChronoPeriod
---

[java.time.chrono]({{'reference/javadoc/packages/#java.time.chrono' | relative_url }})

# public interface ChronoPeriod


A date-based amount of time, such as '3 years, 4 months and 5 days' in an
 arbitrary chronology, intended for advanced globalization use cases.
 <p>
 This interface models a date-based amount of time in a calendar system.
 While most calendar systems use years, months and days, some do not.
 Therefore, this interface operates solely in terms of a set of supported
 units that are defined by the {@code Chronology}.
 The set of supported units is fixed for a given chronology.
 The amount of a supported unit may be set to zero.
 <p>
 The period is modeled as a directed amount of time, meaning that individual
 parts of the period may be negative.
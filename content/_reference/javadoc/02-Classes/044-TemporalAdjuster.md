---
title: TemporalAdjuster
---

[java.time.temporal]({{'reference/javadoc/packages/#java.time.temporal' | relative_url }})

# public interface TemporalAdjuster


Strategy for adjusting a temporal object.
 <p>
 Adjusters are a key tool for modifying temporal objects.
 They exist to externalize the process of adjustment, permitting different
 approaches, as per the strategy design pattern.
 Examples might be an adjuster that sets the date avoiding weekends, or one that
 sets the date to the last day of the month.
 <p>
 There are two equivalent ways of using a {@code TemporalAdjuster}.
 The first is to invoke the method on this interface directly.
 The second is to use {@link Temporal#with(TemporalAdjuster)}:
 <pre>
   // these two lines are equivalent, but the second approach is recommended
   temporal = thisAdjuster.adjustInto(temporal);
   temporal = temporal.with(thisAdjuster);
 </pre>
 It is recommended to use the second approach, {@code with(TemporalAdjuster)},
 as it is a lot clearer to read in code.
 <p>
 The {@link TemporalAdjusters} class contains a standard set of adjusters,
 available as static methods.
 These include:
 <ul>
 <li>finding the first or last day of the month
 <li>finding the first day of next month
 <li>finding the first or last day of the year
 <li>finding the first day of next year
 <li>finding the first or last day-of-week within a month, such as "first Wednesday in June"
 <li>finding the next or previous day-of-week, such as "next Thursday"
 </ul>
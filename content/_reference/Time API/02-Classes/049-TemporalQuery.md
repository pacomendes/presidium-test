---
title: TemporalQuery
---

[java.time.temporal](../packages/#java.time.temporal)

# public interface TemporalQuery


Strategy for querying a temporal object.
 <p>
 Queries are a key tool for extracting information from temporal objects.
 They exist to externalize the process of querying, permitting different
 approaches, as per the strategy design pattern.
 Examples might be a query that checks if the date is the day before February 29th
 in a leap year, or calculates the number of days to your next birthday.
 <p>
 The {@link TemporalField} interface provides another mechanism for querying
 temporal objects. That interface is limited to returning a {@code long}.
 By contrast, queries can return any type.
 <p>
 There are two equivalent ways of using a {@code TemporalQuery}.
 The first is to invoke the method on this interface directly.
 The second is to use {@link TemporalAccessor#query(TemporalQuery)}:
 <pre>
   // these two lines are equivalent, but the second approach is recommended
   temporal = thisQuery.queryFrom(temporal);
   temporal = temporal.query(thisQuery);
 </pre>
 It is recommended to use the second approach, {@code query(TemporalQuery)},
 as it is a lot clearer to read in code.
 <p>
 The most common implementations are method references, such as
 {@code LocalDate::from} and {@code ZoneId::from}.
 Additional common queries are provided as static methods in {@link TemporalQueries}.
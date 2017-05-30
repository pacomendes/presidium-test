---
title: ValueRange
---

[java.time.temporal](../packages/#java.time.temporal)

# public final class ValueRange


The range of valid values for a date-time field.
 <p>
 All {@link TemporalField} instances have a valid range of values.
 For example, the ISO day-of-month runs from 1 to somewhere between 28 and 31.
 This class captures that valid range.
 <p>
 It is important to be aware of the limitations of this class.
 Only the minimum and maximum values are provided.
 It is possible for there to be invalid values within the outer range.
 For example, a weird field may have valid values of 1, 2, 4, 6, 7, thus
 have a range of '1 - 7', despite that fact that values 3 and 5 are invalid.
 <p>
 Instances of this class are not tied to a specific field.
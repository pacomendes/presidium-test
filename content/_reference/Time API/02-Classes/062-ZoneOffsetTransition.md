---
title: ZoneOffsetTransition
---

[java.time.zone](../packages/#java.time.zone)

# public final class ZoneOffsetTransition


A transition between two offsets caused by a discontinuity in the local time-line.
 <p>
 A transition between two offsets is normally the result of a daylight savings cutover.
 The discontinuity is normally a gap in spring and an overlap in autumn.
 {@code ZoneOffsetTransition} models the transition between the two offsets.
 <p>
 Gaps occur where there are local date-times that simply do not exist.
 An example would be when the offset changes from {@code +03:00} to {@code +04:00}.
 This might be described as 'the clocks will move forward one hour tonight at 1am'.
 <p>
 Overlaps occur where there are local date-times that exist twice.
 An example would be when the offset changes from {@code +04:00} to {@code +03:00}.
 This might be described as 'the clocks will move back one hour tonight at 2am'.
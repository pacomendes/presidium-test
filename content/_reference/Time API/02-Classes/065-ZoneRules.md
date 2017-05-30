---
title: ZoneRules
---

[java.time.zone](../packages/#java.time.zone)

# public final class ZoneRules


The rules defining how the zone offset varies for a single time-zone.
 <p>
 The rules model all the historic and future transitions for a time-zone.
 {@link ZoneOffsetTransition} is used for known transitions, typically historic.
 {@link ZoneOffsetTransitionRule} is used for future transitions that are based
 on the result of an algorithm.
 <p>
 The rules are loaded via {@link ZoneRulesProvider} using a {@link ZoneId}.
 The same rules may be shared internally between multiple zone IDs.
 <p>
 Serializing an instance of {@code ZoneRules} will store the entire set of rules.
 It does not store the zone ID as it is not part of the state of this object.
 <p>
 A rule implementation may or may not store full information about historic
 and future transitions, and the information stored is only as accurate as
 that supplied to the implementation by the rules provider.
 Applications should treat the data provided as representing the best information
 available to the implementation of this rule.
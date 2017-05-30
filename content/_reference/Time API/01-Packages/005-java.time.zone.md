---
title: java.time.zone
---

 Support for time-zones and their rules.

# Classes

| Classes | Description 
|:---|:---
|[ZoneOffsetTransition](../classes#zoneoffsettransition) |A transition between two offsets caused by a discontinuity in the local time-line. 
|[ZoneOffsetTransitionRule](../classes#zoneoffsettransitionrule) |A rule expressing how to create a transition. 
|[ZoneOffsetTransitionRule.TimeDefinition](../classes#zoneoffsettransitionrule.timedefinition) |A definition of the way a local time can be converted to the actual 
|[ZoneRules](../classes#zonerules) |The rules defining how the zone offset varies for a single time-zone. 
|[ZoneRulesProvider](../classes#zonerulesprovider) |Provider of time-zone rules to the system. 


# Exceptions

| Exceptions | Description 
|:---|:---
|[ZoneRulesException](../classes#zonerulesexception) |Thrown to indicate a problem with time-zone configuration. 



# Package Description


<p>
 Support for time-zones and their rules.
 </p>
 <p>
 Daylight Saving Time and Time-Zones are concepts used by Governments to alter local time.
 This package provides support for time-zones, their rules and the resulting
 gaps and overlaps in the local time-line typically caused by Daylight Saving Time.
 </p>

 <h3>Package specification</h3>
 <p>
 Unless otherwise noted, passing a null argument to a constructor or method in any class or interface
 in this package will cause a {@link java.lang.NullPointerException NullPointerException} to be thrown.
 The Comment "@param" definition is used to summarise the null-behavior.
 The "@throws {@link java.lang.NullPointerException}" is not explicitly documented in each method.
 </p>
 <p>
 All calculations should check for numeric overflow and throw either an {@link java.lang.ArithmeticException}
 or a {@link java.time.DateTimeException}.
 </p>
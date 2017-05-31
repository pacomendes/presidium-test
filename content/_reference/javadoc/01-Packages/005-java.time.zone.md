---
title: java.time.zone
---

 Support for time-zones and their rules.

# Classes

| Classes | Description 
|:---|:---
|[ZoneOffsetTransition]({{'reference/javadoc/classes#zoneoffsettransition' | relative_url }}) |A transition between two offsets caused by a discontinuity in the local time-line. 
|[ZoneOffsetTransitionRule]({{'reference/javadoc/classes#zoneoffsettransitionrule' | relative_url }}) |A rule expressing how to create a transition. 
|[ZoneOffsetTransitionRule.TimeDefinition]({{'reference/javadoc/classes#zoneoffsettransitionrule.timedefinition' | relative_url }}) |A definition of the way a local time can be converted to the actual 
|[ZoneRules]({{'reference/javadoc/classes#zonerules' | relative_url }}) |The rules defining how the zone offset varies for a single time-zone. 
|[ZoneRulesProvider]({{'reference/javadoc/classes#zonerulesprovider' | relative_url }}) |Provider of time-zone rules to the system. 


# Exceptions

| Exceptions | Description 
|:---|:---
|[ZoneRulesException]({{'reference/javadoc/classes#zonerulesexception' | relative_url }}) |Thrown to indicate a problem with time-zone configuration. 



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
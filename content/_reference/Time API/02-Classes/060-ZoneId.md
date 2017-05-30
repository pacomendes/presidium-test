---
title: ZoneId
---

[java.time](../packages/#java.time)

# public abstract class ZoneId


A time-zone ID, such as {@code Europe/Paris}.
 <p>
 A {@code ZoneId} is used to identify the rules used to convert between
 an {@link Instant} and a {@link LocalDateTime}.
 There are two distinct types of ID:
 <ul>
 <li>Fixed offsets - a fully resolved offset from UTC/Greenwich, that uses
  the same offset for all local date-times
 <li>Geographical regions - an area where a specific set of rules for finding
  the offset from UTC/Greenwich apply
 </ul>
 Most fixed offsets are represented by {@link ZoneOffset}.
 Calling {@link #normalized()} on any {@code ZoneId} will ensure that a
 fixed offset ID will be represented as a {@code ZoneOffset}.
 <p>
 The actual rules, describing when and how the offset changes, are defined by {@link ZoneRules}.
 This class is simply an ID used to obtain the underlying rules.
 This approach is taken because rules are defined by governments and change
 frequently, whereas the ID is stable.
 <p>
 The distinction has other effects. Serializing the {@code ZoneId} will only send
 the ID, whereas serializing the rules sends the entire data set.
 Similarly, a comparison of two IDs only examines the ID, whereas
 a comparison of two rules examines the entire data set.

 <h3>Time-zone IDs</h3>
 The ID is unique within the system.
 There are three types of ID.
 <p>
 The simplest type of ID is that from {@code ZoneOffset}.
 This consists of 'Z' and IDs starting with '+' or '-'.
 <p>
 The next type of ID are offset-style IDs with some form of prefix,
 such as 'GMT+2' or 'UTC+01:00'.
 The recognised prefixes are 'UTC', 'GMT' and 'UT'.
 The offset is the suffix and will be normalized during creation.
 These IDs can be normalized to a {@code ZoneOffset} using {@code normalized()}.
 <p>
 The third type of ID are region-based IDs. A region-based ID must be of
 two or more characters, and not start with 'UTC', 'GMT', 'UT' '+' or '-'.
 Region-based IDs are defined by configuration, see {@link ZoneRulesProvider}.
 The configuration focuses on providing the lookup from the ID to the
 underlying {@code ZoneRules}.
 <p>
 Time-zone rules are defined by governments and change frequently.
 There are a number of organizations, known here as groups, that monitor
 time-zone changes and collate them.
 The default group is the IANA Time Zone Database (TZDB).
 Other organizations include IATA (the airline industry body) and Microsoft.
 <p>
 Each group defines its own format for the region ID it provides.
 The TZDB group defines IDs such as 'Europe/London' or 'America/New_York'.
 TZDB IDs take precedence over other groups.
 <p>
 It is strongly recommended that the group name is included in all IDs supplied by
 groups other than TZDB to avoid conflicts. For example, IATA airline time-zone
 region IDs are typically the same as the three letter airport code.
 However, the airport of Utrecht has the code 'UTC', which is obviously a conflict.
 The recommended format for region IDs from groups other than TZDB is 'group~region'.
 Thus if IATA data were defined, Utrecht airport would be 'IATA~UTC'.

 <h3>Serialization</h3>
 This class can be serialized and stores the string zone ID in the external form.
 The {@code ZoneOffset} subclass uses a dedicated format that only stores the
 offset from UTC/Greenwich.
 <p>
 A {@code ZoneId} can be deserialized in a Java Runtime where the ID is unknown.
 For example, if a server-side Java Runtime has been updated with a new zone ID, but
 the client-side Java Runtime has not been updated. In this case, the {@code ZoneId}
 object will exist, and can be queried using {@code getId}, {@code equals},
 {@code hashCode}, {@code toString}, {@code getDisplayName} and {@code normalized}.
 However, any call to {@code getRules} will fail with {@code ZoneRulesException}.
 This approach is designed to allow a {@link ZonedDateTime} to be loaded and
 queried, but not modified, on a Java Runtime with incomplete time-zone information.

 <p>
 This is a <a href="{@docRoot}/java/lang/doc-files/ValueBased.html">value-based</a>
 class; use of identity-sensitive operations (including reference equality
 ({@code ==}), identity hash code, or synchronization) on instances of
 {@code ZoneId} may have unpredictable results and should be avoided.
 The {@code equals} method should be used for comparisons.
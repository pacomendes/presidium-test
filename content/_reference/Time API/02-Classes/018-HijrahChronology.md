---
title: HijrahChronology
---

[java.time.chrono](../packages/#java.time.chrono)

# public final class HijrahChronology


The Hijrah calendar is a lunar calendar supporting Islamic calendars.
 <p>
 The HijrahChronology follows the rules of the Hijrah calendar system. The Hijrah
 calendar has several variants based on differences in when the new moon is
 determined to have occurred and where the observation is made.
 In some variants the length of each month is
 computed algorithmically from the astronomical data for the moon and earth and
 in others the length of the month is determined by an authorized sighting
 of the new moon. For the algorithmically based calendars the calendar
 can project into the future.
 For sighting based calendars only historical data from past
 sightings is available.
 <p>
 The length of each month is 29 or 30 days.
 Ordinary years have 354 days; leap years have 355 days.

 <p>
 CLDR and LDML identify variants:
 <table cellpadding="2" summary="Variants of Hijrah Calendars">
 <thead>
 <tr class="tableSubHeadingColor">
 <th class="colFirst" align="left" >Chronology ID</th>
 <th class="colFirst" align="left" >Calendar Type</th>
 <th class="colFirst" align="left" >Locale extension, see {@link java.util.Locale}</th>
 <th class="colLast" align="left" >Description</th>
 </tr>
 </thead>
 <tbody>
 <tr class="altColor">
 <td>Hijrah-umalqura</td>
 <td>islamic-umalqura</td>
 <td>ca-islamic-umalqura</td>
 <td>Islamic - Umm Al-Qura calendar of Saudi Arabia</td>
 </tr>
 </tbody>
 </table>
 <p>Additional variants may be available through {@link Chronology#getAvailableChronologies()}.

 <p>Example</p>
 <p>
 Selecting the chronology from the locale uses {@link Chronology#ofLocale}
 to find the Chronology based on Locale supported BCP 47 extension mechanism
 to request a specific calendar ("ca"). For example,
 </p>
 <pre>
      Locale locale = Locale.forLanguageTag("en-US-u-ca-islamic-umalqura");
      Chronology chrono = Chronology.ofLocale(locale);
 </pre>
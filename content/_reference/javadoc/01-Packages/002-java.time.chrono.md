---
title: java.time.chrono
---

 Generic API for calendar systems other than the default ISO.

# Interfaces

| Interfaces | Description 
|:---|:---
|[ChronoLocalDate]({{'reference/javadoc/classes#chronolocaldate' | relative_url }}) |A date without time-of-day or time-zone in an arbitrary chronology, intended 
|[ChronoLocalDateTime]({{'reference/javadoc/classes#chronolocaldatetime' | relative_url }}) |A date-time without a time-zone in an arbitrary chronology, intended 
|[Chronology]({{'reference/javadoc/classes#chronology' | relative_url }}) |A calendar system, used to organize and identify dates. 
|[ChronoPeriod]({{'reference/javadoc/classes#chronoperiod' | relative_url }}) |A date-based amount of time, such as '3 years, 4 months and 5 days' in an 
|[ChronoZonedDateTime]({{'reference/javadoc/classes#chronozoneddatetime' | relative_url }}) |A date-time with a time-zone in an arbitrary chronology, 
|[Era]({{'reference/javadoc/classes#era' | relative_url }}) |An era of the time-line. 


# Classes

| Classes | Description 
|:---|:---
|[AbstractChronology]({{'reference/javadoc/classes#abstractchronology' | relative_url }}) |An abstract implementation of a calendar system, used to organize and identify dates. 
|[HijrahChronology]({{'reference/javadoc/classes#hijrahchronology' | relative_url }}) |The Hijrah calendar is a lunar calendar supporting Islamic calendars. 
|[HijrahDate]({{'reference/javadoc/classes#hijrahdate' | relative_url }}) |A date in the Hijrah calendar system. 
|[HijrahEra]({{'reference/javadoc/classes#hijrahera' | relative_url }}) |An era in the Hijrah calendar system. 
|[IsoChronology]({{'reference/javadoc/classes#isochronology' | relative_url }}) |The ISO calendar system. 
|[IsoEra]({{'reference/javadoc/classes#isoera' | relative_url }}) |An era in the ISO calendar system. 
|[JapaneseChronology]({{'reference/javadoc/classes#japanesechronology' | relative_url }}) |The Japanese Imperial calendar system. 
|[JapaneseDate]({{'reference/javadoc/classes#japanesedate' | relative_url }}) |A date in the Japanese Imperial calendar system. 
|[JapaneseEra]({{'reference/javadoc/classes#japaneseera' | relative_url }}) |An era in the Japanese Imperial calendar system. 
|[MinguoChronology]({{'reference/javadoc/classes#minguochronology' | relative_url }}) |The Minguo calendar system. 
|[MinguoDate]({{'reference/javadoc/classes#minguodate' | relative_url }}) |A date in the Minguo calendar system. 
|[MinguoEra]({{'reference/javadoc/classes#minguoera' | relative_url }}) |An era in the Minguo calendar system. 
|[ThaiBuddhistChronology]({{'reference/javadoc/classes#thaibuddhistchronology' | relative_url }}) |The Thai Buddhist calendar system. 
|[ThaiBuddhistDate]({{'reference/javadoc/classes#thaibuddhistdate' | relative_url }}) |A date in the Thai Buddhist calendar system. 
|[ThaiBuddhistEra]({{'reference/javadoc/classes#thaibuddhistera' | relative_url }}) |An era in the Thai Buddhist calendar system. 



# Package Description


<p>
 Generic API for calendar systems other than the default ISO.
 </p>
 <p>
 The main API is based around the calendar system defined in ISO-8601.
 However, there are other calendar systems, and this package provides basic support for them.
 The alternate calendars are provided in the {@link java.time.chrono} package.
 </p>
 <p>
 A calendar system is defined by the {@link java.time.chrono.Chronology} interface,
 while a date in a calendar system is defined by the {@link java.time.chrono.ChronoLocalDate} interface.
 </p>
 <p>
 It is intended that applications use the main API whenever possible, including code to read and write
 from a persistent data store, such as a database, and to send dates and times across a network.
 The "chrono" classes are then used at the user interface level to deal with localized input/output.
 See {@link java.time.chrono.ChronoLocalDate ChronoLocalDate}
 for a full discussion of the issues.
 </p>
 <p>
 Using non-ISO calendar systems in an application introduces significant extra complexity.
 Ensure that the warnings and recommendations in {@code ChronoLocalDate} have been read before
 working with the "chrono" interfaces.
 </p>
 <p>
 The supported calendar systems includes:
 </p>
 <ul>
 <li>{@link java.time.chrono.HijrahChronology Hijrah calendar}</li>
 <li>{@link java.time.chrono.JapaneseChronology Japanese calendar}</li>
 <li>{@link java.time.chrono.MinguoChronology Minguo calendar}</li>
 <li>{@link java.time.chrono.ThaiBuddhistChronology Thai Buddhist calendar}</li>
 </ul>

 <h3>Example</h3>
 <p>
 This example lists todays date for all of the available calendars.
 </p>
 <pre>
   // Enumerate the list of available calendars and print todays date for each.
       Set&lt;Chronology&gt; chronos = Chronology.getAvailableChronologies();
       for (Chronology chrono : chronos) {
           ChronoLocalDate date = chrono.dateNow();
           System.out.printf("   %20s: %s%n", chrono.getId(), date.toString());
       }
 </pre>

 <p>
 This example creates and uses a date in a named non-ISO calendar system.
 </p>
 <pre>
   // Print the Thai Buddhist date
       ChronoLocalDate now1 = Chronology.of("ThaiBuddhist").dateNow();
       int day = now1.get(ChronoField.DAY_OF_MONTH);
       int dow = now1.get(ChronoField.DAY_OF_WEEK);
       int month = now1.get(ChronoField.MONTH_OF_YEAR);
       int year = now1.get(ChronoField.YEAR);
       System.out.printf("  Today is %s %s %d-%s-%d%n", now1.getChronology().getId(),
                 dow, day, month, year);
   // Print today's date and the last day of the year for the Thai Buddhist Calendar.
       ChronoLocalDate first = now1
                 .with(ChronoField.DAY_OF_MONTH, 1)
                 .with(ChronoField.MONTH_OF_YEAR, 1);
       ChronoLocalDate last = first
                 .plus(1, ChronoUnit.YEARS)
                 .minus(1, ChronoUnit.DAYS);
       System.out.printf("  %s: 1st of year: %s; end of year: %s%n", last.getChronology().getId(),
                 first, last);
  </pre>

 <p>
 This example creates and uses a date in a specific ThaiBuddhist calendar system.
 </p>
 <pre>
   // Print the Thai Buddhist date
       ThaiBuddhistDate now1 = ThaiBuddhistDate.now();
       int day = now1.get(ChronoField.DAY_OF_MONTH);
       int dow = now1.get(ChronoField.DAY_OF_WEEK);
       int month = now1.get(ChronoField.MONTH_OF_YEAR);
       int year = now1.get(ChronoField.YEAR);
       System.out.printf("  Today is %s %s %d-%s-%d%n", now1.getChronology().getId(),
                 dow, day, month, year);

   // Print today's date and the last day of the year for the Thai Buddhist Calendar.
       ThaiBuddhistDate first = now1
                 .with(ChronoField.DAY_OF_MONTH, 1)
                 .with(ChronoField.MONTH_OF_YEAR, 1);
       ThaiBuddhistDate last = first
                 .plus(1, ChronoUnit.YEARS)
                 .minus(1, ChronoUnit.DAYS);
       System.out.printf("  %s: 1st of year: %s; end of year: %s%n", last.getChronology().getId(),
                 first, last);
  </pre>

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
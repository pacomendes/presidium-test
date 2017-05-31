---
title: Clock
---

[java.time]({{'reference/javadoc/packages/#java.time' | relative_url }})

# public abstract class Clock


A clock providing access to the current instant, date and time using a time-zone.
 <p>
 Instances of this class are used to find the current instant, which can be
 interpreted using the stored time-zone to find the current date and time.
 As such, a clock can be used instead of {@link System#currentTimeMillis()}
 and {@link TimeZone#getDefault()}.
 <p>
 Use of a {@code Clock} is optional. All key date-time classes also have a
 {@code now()} factory method that uses the system clock in the default time zone.
 The primary purpose of this abstraction is to allow alternate clocks to be
 plugged in as and when required. Applications use an object to obtain the
 current time rather than a static method. This can simplify testing.
 <p>
 Best practice for applications is to pass a {@code Clock} into any method
 that requires the current instant. A dependency injection framework is one
 way to achieve this:
 <pre>
  public class MyBean {
    private Clock clock;  // dependency inject
    ...
    public void process(LocalDate eventDate) {
      if (eventDate.isBefore(LocalDate.now(clock)) {
        ...
      }
    }
  }
 </pre>
 This approach allows an alternate clock, such as {@link #fixed(Instant, ZoneId) fixed}
 or {@link #offset(Clock, Duration) offset} to be used during testing.
 <p>
 The {@code system} factory methods provide clocks based on the best available
 system clock This may use {@link System#currentTimeMillis()}, or a higher
 resolution clock if one is available.
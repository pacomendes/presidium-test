---
title: ZoneRulesProvider
---

[java.time.zone](../packages/#java.time.zone)

# public abstract class ZoneRulesProvider


Provider of time-zone rules to the system.
 <p>
 This class manages the configuration of time-zone rules.
 The static methods provide the public API that can be used to manage the providers.
 The abstract methods provide the SPI that allows rules to be provided.
 <p>
 ZoneRulesProvider may be installed in an instance of the Java Platform as
 extension classes, that is, jar files placed into any of the usual extension
 directories. Installed providers are loaded using the service-provider loading
 facility defined by the {@link ServiceLoader} class. A ZoneRulesProvider
 identifies itself with a provider configuration file named
 {@code java.time.zone.ZoneRulesProvider} in the resource directory
 {@code META-INF/services}. The file should contain a line that specifies the
 fully qualified concrete zonerules-provider class name.
 Providers may also be made available by adding them to the class path or by
 registering themselves via {@link #registerProvider} method.
 <p>
 The Java virtual machine has a default provider that provides zone rules
 for the time-zones defined by IANA Time Zone Database (TZDB). If the system
 property {@code java.time.zone.DefaultZoneRulesProvider} is defined then
 it is taken to be the fully-qualified name of a concrete ZoneRulesProvider
 class to be loaded as the default provider, using the system class loader.
 If this system property is not defined, a system-default provider will be
 loaded to serve as the default provider.
 <p>
 Rules are looked up primarily by zone ID, as used by {@link ZoneId}.
 Only zone region IDs may be used, zone offset IDs are not used here.
 <p>
 Time-zone rules are political, thus the data can change at any time.
 Each provider will provide the latest rules for each zone ID, but they
 may also provide the history of how the rules changed.
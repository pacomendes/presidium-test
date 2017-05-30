---
title: ThaiBuddhistEra
---

[java.time.chrono](../packages/#java.time.chrono)

# public final enum ThaiBuddhistEra


An era in the Thai Buddhist calendar system.
 <p>
 The Thai Buddhist calendar system has two eras.
 The current era, for years from 1 onwards, is known as the 'Buddhist' era.
 All previous years, zero or earlier in the proleptic count or one and greater
 in the year-of-era count, are part of the 'Before Buddhist' era.

 <table summary="Buddhist years and eras" cellpadding="2" cellspacing="3" border="0" >
 <thead>
 <tr class="tableSubHeadingColor">
 <th class="colFirst" align="left">year-of-era</th>
 <th class="colFirst" align="left">era</th>
 <th class="colFirst" align="left">proleptic-year</th>
 <th class="colLast" align="left">ISO proleptic-year</th>
 </tr>
 </thead>
 <tbody>
 <tr class="rowColor">
 <td>2</td><td>BE</td><td>2</td><td>-542</td>
 </tr>
 <tr class="altColor">
 <td>1</td><td>BE</td><td>1</td><td>-543</td>
 </tr>
 <tr class="rowColor">
 <td>1</td><td>BEFORE_BE</td><td>0</td><td>-544</td>
 </tr>
 <tr class="altColor">
 <td>2</td><td>BEFORE_BE</td><td>-1</td><td>-545</td>
 </tr>
 </tbody>
 </table>
 <p>
 <b>Do not use {@code ordinal()} to obtain the numeric representation of {@code ThaiBuddhistEra}.
 Use {@code getValue()} instead.</b>
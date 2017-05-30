---
title: MinguoEra
---

[java.time.chrono](../packages/#java.time.chrono)

# public final enum MinguoEra


An era in the Minguo calendar system.
 <p>
 The Minguo calendar system has two eras.
 The current era, for years from 1 onwards, is known as the 'Republic of China' era.
 All previous years, zero or earlier in the proleptic count or one and greater
 in the year-of-era count, are part of the 'Before Republic of China' era.

 <table summary="Minguo years and eras" cellpadding="2" cellspacing="3" border="0" >
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
 <td>2</td><td>ROC</td><td>2</td><td>1913</td>
 </tr>
 <tr class="altColor">
 <td>1</td><td>ROC</td><td>1</td><td>1912</td>
 </tr>
 <tr class="rowColor">
 <td>1</td><td>BEFORE_ROC</td><td>0</td><td>1911</td>
 </tr>
 <tr class="altColor">
 <td>2</td><td>BEFORE_ROC</td><td>-1</td><td>1910</td>
 </tr>
 </tbody>
 </table>
 <p>
 <b>Do not use {@code ordinal()} to obtain the numeric representation of {@code MinguoEra}.
 Use {@code getValue()} instead.</b>
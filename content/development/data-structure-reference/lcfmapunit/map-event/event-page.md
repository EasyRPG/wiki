---
title: "Event Page"
---
-   Data Type: 2 Dimensional Array

<table>
<thead>
<tr class="header">
<th>Index</th>
<th>Detail</th>
<th>Data Type</th>
<th>Default Value</th>
<th>etc.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>2</td>
<td><a href="/Event Page/Trigger Term">./Event Page/Trigger Term</a></td>
<td>1 Dimensional Array</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>21</td>
<td>CharSet</td>
<td>String</td>
<td>""</td>
<td>If this element is empty event graphic will be upper ChipSet.</td>
</tr>
<tr class="odd">
<td>22</td>
<td>CharSet/Upper ChipSet Index</td>
<td>Integer</td>
<td>0</td>
<td>* When CharSet: 0 〜 7<br />
* When Upper ChipSet: 0 〜 143</td>
</tr>
<tr class="even">
<td>23</td>
<td>CharSet Direction</td>
<td>Integer</td>
<td>2</td>
<td>* 0: Up<br />
* 1: Right<br />
* 2: Down<br />
* 3: Left</td>
</tr>
<tr class="odd">
<td>24</td>
<td>Event Graphic Semi-Transparency</td>
<td>bool</td>
<td>false</td>
<td></td>
</tr>
<tr class="even">
<td>31</td>
<td>Move Type</td>
<td>Integer</td>
<td>0</td>
<td>* 0: No Move<br />
* 1: Random Move<br />
* 2: Vertical Ply<br />
* 3: Horizontal Ply<br />
* 4: Move to Party<br />
* 5: Move from Party<br />
* 6: Set Move Route</td>
</tr>
<tr class="odd">
<td>32</td>
<td>Move Frequency</td>
<td>Integer</td>
<td>3</td>
<td>1 〜 8</td>
</tr>
<tr class="even">
<td>33</td>
<td>Event Trigger Type</td>
<td>Integer</td>
<td>0</td>
<td>* 0: Press Enter<br />
* 1: Touch from Party<br />
* 2: Touch from Event<br />
* 3: Auto<br />
* 4: Parallel</td>
</tr>
<tr class="odd">
<td>34</td>
<td>Draw Priority</td>
<td>Integer</td>
<td>0</td>
<td>* 0: Below Character<br />
* 1: Doesn't Pile<br />
* 2: Above Character</td>
</tr>
<tr class="even">
<td>35</td>
<td>Draw Priority/Doesn't Pile with another Event</td>
<td>Boolean</td>
<td>false</td>
<td></td>
</tr>
<tr class="odd">
<td>36</td>
<td>Animation Type</td>
<td>Integer</td>
<td>0</td>
<td>* 0: Normal/Disable Step<br />
* 1: Normal/Enable Step<br />
* 2: Fix Direction/Disable Step<br />
* 3: Fix Direction/Enable Step<br />
* 4: Fix Graphic<br />
* 5: 4 Frame Animation(Clockwise)</td>
</tr>
<tr class="even">
<td>41</td>
<td><a href="/Event Page/Move Route">./Event Page/Move Route</a></td>
<td>1 Dimensional Array</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>51</td>
<td>Event Data Size</td>
<td>Integer</td>
<td>0</td>
<td></td>
</tr>
<tr class="even">
<td>52</td>
<td>Event Data</td>
<td>Event</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

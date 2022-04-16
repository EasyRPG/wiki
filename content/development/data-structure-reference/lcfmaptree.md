---
title: "LcfMapTree"
---
## File Name

-   "RPG_RT.lmt"
-   "lmt" stands for "Lcf" "Map" "Tree"

## Header

-   "LcfMapTree"

## Global Array

-   Data Type: 2 Dimensional Array
-   \[0\]: Root. This "map name" is the game title.

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
<td>1</td>
<td>Map Name</td>
<td>String</td>
<td>""</td>
<td>smaller than 12 byte</td>
</tr>
<tr class="even">
<td>2</td>
<td>Parent Map ID</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>3</td>
<td></td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>4</td>
<td>Type</td>
<td>Integer</td>
<td></td>
<td>* 1: Normal Map<br />
* 2: Area</td>
</tr>
<tr class="odd">
<td>5</td>
<td>Horizontal Scroll Bar</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>6</td>
<td>Vertical Scroll Bar</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Extracted Node</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>11</td>
<td>BGM</td>
<td>Integer</td>
<td></td>
<td>* 0: Same as Parent<br />
* 1: Leave to Event<br />
* 2: Set</td>
</tr>
<tr class="odd">
<td>12</td>
<td>BGM</td>
<td><a href="/development/data-structure-reference/audio-information">Music</a></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>21</td>
<td>Backdrop</td>
<td>Integer</td>
<td></td>
<td>* 0: Same as Parent<br />
* 1: Leave to Event<br />
* 2: Set</td>
</tr>
<tr class="odd">
<td>22</td>
<td>Backdrop/File Name</td>
<td>String</td>
<td>""</td>
<td></td>
</tr>
<tr class="even">
<td>31</td>
<td>Teleport</td>
<td>Integer</td>
<td></td>
<td>* 0: Same as Parent<br />
* 1: Leave to Event<br />
* 2: Set</td>
</tr>
<tr class="odd">
<td>32</td>
<td>Escape</td>
<td>Integer</td>
<td></td>
<td>〃</td>
</tr>
<tr class="even">
<td>33</td>
<td>Save</td>
<td>Integer</td>
<td></td>
<td>〃</td>
</tr>
<tr class="odd">
<td>41</td>
<td><a href="/LcfMapTree/Encounter Enemy Group">./LcfMapTree/Encounter Enemy Group</a></td>
<td>2 Dimensional Array</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>44</td>
<td>Enemy Appear Step</td>
<td>Integer</td>
<td>25</td>
<td></td>
</tr>
<tr class="odd">
<td>51</td>
<td>Area Range</td>
<td>Binary</td>
<td></td>
<td>array&lt;uint32_t, 4&gt;<br />
* [0]: begin x<br />
* [1]: begin y<br />
* [2]: end x<br />
* [3]: end y<br />
(Normal Map will be { 0, 0, 0, 0 })</td>
</tr>
</tbody>
</table>

## BER Number Enumeration

-   Element Number(BER) + BER Number\[Element Number \* 1\]

## Start Point

-   Data Type: 1 Dimensional Array

| Index | Detail               | Data Type | Default Value | etc. |
|-------|----------------------|-----------|---------------|------|
| 1     | Party Map ID         | Integer   |               |      |
| 2     | Party X Coordinate   | Integer   | 0             |      |
| 3     | Party Y Coordinate   | Integer   | 0             |      |
| 11    | Boat Map ID          | Integer   |               |      |
| 12    | Boat X Coordinate    | Integer   | 0             |      |
| 13    | Boat Y Coordinate    | Integer   | 0             |      |
| 21    | Ship Map ID          | Integer   |               |      |
| 22    | Ship X Coordinate    | Integer   | 0             |      |
| 23    | Ship Y Coordinate    | Integer   | 0             |      |
| 31    | Airship Map ID       | Integer   |               |      |
| 32    | Airship X Coordinate | Integer   | 0             |      |
| 33    | Airship Y Coordinate | Integer   | 0             |      |

---
title: "LcfMapUnit"
---
## File Name

-   "Map%04d.lmu"
-   "lmu" stands for "Lcf" "Map" "Unit"

## Header

-   "LcfMapUnit"

## Global Array

-   Data Type: 1 Dimensional Array

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
<td>ChipSet ID</td>
<td>Integer</td>
<td>1</td>
<td></td>
</tr>
<tr class="even">
<td>2</td>
<td>Width</td>
<td>Integer</td>
<td>20</td>
<td></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Height</td>
<td>Integer</td>
<td>15</td>
<td></td>
</tr>
<tr class="even">
<td>11</td>
<td>Scroll Type</td>
<td>Integer</td>
<td></td>
<td>* 0: No Loop<br />
* 1: Vertical Loop Only<br />
* 2: Horizontal Loop Only<br />
* 3: Vertical and Horizontal Loop</td>
</tr>
<tr class="odd">
<td>31</td>
<td>Panorama/Use Panorama</td>
<td>Boolean</td>
<td>false</td>
<td></td>
</tr>
<tr class="even">
<td>32</td>
<td>Panorama/Panorama File Name</td>
<td>String</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>33</td>
<td>Panorama/Option/Horizontal Loop</td>
<td>Boolean</td>
<td>false</td>
<td></td>
</tr>
<tr class="even">
<td>34</td>
<td>Panorama/Option/Vertical Loop</td>
<td>Boolean</td>
<td>false</td>
<td></td>
</tr>
<tr class="odd">
<td>35</td>
<td>Panorama/Option/Horizontal Loop/Auto Scroll</td>
<td>Boolean</td>
<td>false</td>
<td></td>
</tr>
<tr class="even">
<td>36</td>
<td>Panorama/Option/Horizontal Loop/Auto Scroll/Speed</td>
<td>Integer</td>
<td>0</td>
<td>-8 〜 8</td>
</tr>
<tr class="odd">
<td>37</td>
<td>Panorama/Option/Vertical Loop/Auto Scroll</td>
<td>Boolean</td>
<td>false</td>
<td></td>
</tr>
<tr class="even">
<td>38</td>
<td>Panorama/Option/Vertical Loop/Auto Scroll/Speed</td>
<td>Integer</td>
<td>0</td>
<td>-8 〜 8</td>
</tr>
<tr class="odd">
<td>71</td>
<td>Lower Map</td>
<td>Binary</td>
<td></td>
<td>* vector&lt;uint16_t&gt;(Width * Height)<br />
* [0] is (0, 0)<br />
* [Width * Height -1] is (Width - 1, Height - 1)</td>
</tr>
<tr class="even">
<td>72</td>
<td>Upper Map</td>
<td>Binary</td>
<td></td>
<td>〃</td>
</tr>
<tr class="odd">
<td>81</td>
<td><a href="/LcfMapUnit/Map Event">./LcfMapUnit/Map Event</a></td>
<td>2 Dimensional Array</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>91</td>
<td>Save Time</td>
<td>Integer</td>
<td></td>
<td>While loading save data, if this element is modified, the event execution state will be reloaded</td>
</tr>
</tbody>
</table>

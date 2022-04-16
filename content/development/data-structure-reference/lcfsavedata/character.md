---
title: "Character"
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
<td>1</td>
<td>Name</td>
<td>String</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>2</td>
<td>Title</td>
<td>String</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>11</td>
<td>CharSet</td>
<td>String</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>12</td>
<td>CharSet Index</td>
<td>String</td>
<td></td>
<td>0 〜 7</td>
</tr>
<tr class="odd">
<td>21</td>
<td>FaceSet</td>
<td>String</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>22</td>
<td>FaceSet Index</td>
<td>Integer</td>
<td></td>
<td>0 ～ 15</td>
</tr>
<tr class="odd">
<td>31</td>
<td>Level</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>32</td>
<td>Experience</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>33</td>
<td>HP Fix</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>34</td>
<td>MP Fix</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>41</td>
<td>Attack Fix</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>42</td>
<td>Gaurd Fix</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>43</td>
<td>Mental Fix</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>44</td>
<td>Speed Fix</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>51</td>
<td>Mastered Skill Number</td>
<td>Integer</td>
<td>0</td>
<td></td>
</tr>
<tr class="even">
<td>52</td>
<td>Mastered Skill</td>
<td>Binary</td>
<td></td>
<td>* set&lt;uint16_t&gt;<br />
* Enumeration of skill ID that is sorted</td>
</tr>
<tr class="odd">
<td>61</td>
<td>Equipment</td>
<td>BInary</td>
<td></td>
<td>array&lt;uint16_t, 5&gt;<br />
* [0]: WEAPON<br />
* [1]: SHIELD<br />
* [2]: ARMOR<br />
* [3]: HELMET<br />
* [4]: OTHER<br />
If item ID is ZERO it's unequiped</td>
</tr>
<tr class="even">
<td>71</td>
<td>Current HP</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td>72</td>
<td>Current MP</td>
<td>Integer</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>80</td>
<td>Job</td>
<td>Integer</td>
<td></td>
<td>RPG2003</td>
</tr>
<tr class="odd">
<td>82</td>
<td>Double Hand</td>
<td>Boolean</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

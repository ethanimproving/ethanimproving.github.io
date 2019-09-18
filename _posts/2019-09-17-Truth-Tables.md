A simple blog post to explore the 16 possible [boolean operators](https://en.wikipedia.org/wiki/Truth_table).

## 1. NOT Operator

| a | !a |
|---|---|
| true | false |
| false | true |

## 2. OR Operator

| a     | b     | a &#124;&#124; b |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | true       |
| false | true  | true       |
| false | false | false      |

## 3. AND Operator

| a     | b     | a && b |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | false      |
| false | true  | false      |
| false | false | false      |

## 4. Exclusive OR Operator

| a     | b     | a ^ b |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | true       |
| false | true  | true       |
| false | false | false      |

## 5. Contradiction

| a     | b     | result |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | false      |
| false | true  | false      |
| false | false | false      |

## 6. Joint Denial

| a     | b     | !(a &#124;&#124; b) |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | false      |
| false | true  | false      |
| false | false | true       |

## 7. Converse Nonimplication

| a     | b     | a </- b |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | false      |
| false | true  | true       |
| false | false | false      |

## 8. Negation of A

| a     | b     |  !a |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | false      |
| false | true  | true       |
| false | false | true       |

## 9. Material Nonimplication

| a     | b     |  a -/> b |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | true       |
| false | true  | false      |
| false | false | false      |

## 10. Negation of B

| a     | b     |  !b |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | true       |
| false | true  | false      |
| false | false | true       |

## 11. Sheffer Stroke

| a     | b     |  !(a && b) |
|-------|-------|------------|
| true  | true  | false      |
| true  | false | true       |
| false | true  | true       |
| false | false | true       |

## 12. Projection of B

| a     | b     |  b |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | false      |
| false | true  | true       |
| false | false | false      |

## 13. Material Condition

| a     | b     |  a –> b |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | false      |
| false | true  | true       |
| false | false | true       |

## 14. Projection of A

| a     | b     |  a |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | true       |
| false | true  | false      |
| false | false | false      |

## 15. Converse Implication

| a     | b     |  a <– b |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | true       |
| false | true  | false      |
| false | false | true       |

## 16. Tautology

| a     | b     |  result |
|-------|-------|------------|
| true  | true  | true       |
| true  | false | true       |
| false | true  | true       |
| false | false | true       |

## [Jekyll Tables](https://idratherbewriting.com/documentation-theme-jekyll/mydoc_tables.html)

 Column1    Column2   result 
 ------------------------------
 true        false     true
 false       false     true
 true        true      true
 false       true      true

---
layout: post
title: You're up and running!
---

| Priority apples | Second priority | Third priority |
|-------|--------|---------|
| ambrosia | gala | red delicious |
| pink lady | jazz | macintosh |
| honeycrisp | granny smith | fuji |


<div class="datatable-begin"></div>

Food    | Description                           | Category | Sample type
------- | ------------------------------------- | -------- | -----------
Apples  | A small, somewhat round ...           | Fruit    | Fuji
Bananas | A long and curved, often-yellow ...   | Fruit    | Snow
Kiwis   | A small, hairy-skinned sweet ...      | Fruit    | Golden
Oranges | A spherical, orange-colored sweet ... | Fruit    | Navel

<div class="datatable-end"></div>

<table>
<colgroup>
<col width="30%" />
<col width="70%" />
</colgroup>
<thead>
<tr class="header">
<th>Field</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td markdown="span">First column **fields**</td>
<td markdown="span">Some descriptive text. This is a markdown link to [Google](http://google.com). Or see [some link][mydoc_tags].</td>
</tr>
<tr>
<td markdown="span">Second column **fields**</td>
<td markdown="span">Some more descriptive text.
</td>
</tr>
</tbody>
</table>

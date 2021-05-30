## .math.range

Find the range of integers between two integers. It is inclusive on both ends.


**Author**: David Han


**Parameters:**

|Name|Type|Description|
|---|---|---|
|startVal|integer|An integer to start a range|
|stopVal|integer|An integer to stop a range|

**Returns:**

|Type|Description|
|---|---|
|integer[]|A list of integers|

**Example:** Find the range between 2 and 6

```q
 .math.range[2;6]
 /=> 2 3 4 5 6
```
## .math.factorial

Calculate the factorial of a given positive integer.


**Author**: David Han


**Parameter:**

|Name|Type|Description|
|---|---|---|
|n|integer|An integer|

**Returns:**

|Type|Description|
|---|---|
|integer|An integer|

**Example:** Compute the factorial of 5

```q
 .math.factorial 5
```

## .math.isInteger

Check whether the given input is an integer


**Parameter:**

|Name|Type|Description|
|---|---|---|
|x|number|A number|

**Returns:**

|Type|Description|
|---|---|
|boolean|A boolean to indicate whether the input is an integer|

**Example:** Check whether a float is an integer

```q
 .math.isInteger 3.4
```


**Example:** Check whether a short is an integer

```q
 .math.isInteger 6h
```

## .math.primeRange

Enter a description here...

**Returns:**

|Type|Description|
|---|---|
|Type|Enter a return description here...|

## .math.range

Find the range of integers between two integers. It is inclusive on both ends.


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
 .math.range[2;6] / 2 3 4 5 6
```
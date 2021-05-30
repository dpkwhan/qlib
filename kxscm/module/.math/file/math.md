## .math.PI

PI represents the ratio of the circumference of a circle to its diameter, approximately 3.14159.

## .math.columnSum

Enter a description here...

**Returns:**

|Type|Description|
|---|---|
|Type|Enter a return description here...|

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

## .math.groupSum

Sum numbers based on their group.


**Author**: David Han


**Parameters:**

|Name|Type|Description|
|---|---|---|
|x|number[]|a list of values|
|y|any[]|a list of groups|

**Returns:**

|Type|Description|
|---|---|
|number[]|A list of numbers|

**Example:** Sum numbers according to a group of integers

```q
 .math.groupSum[1 2 3 4 5;1 2 1 2 1]
```


**Example:** Sum numbers according to a group of symbols

```q
 .math.groupSum[1 2 3 4 5;`a`b`a`b`a]
```


**Example:** Sum numbers according to a group of mixed type values

```q
 .math.groupSum[1 2 3 4 5;(`a;2;`a;2;`a)]
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

## .math.rowSum

Calculate the sum of each row in a matrix.


**Parameter:**

|Name|Type|Description|
|---|---|---|
|x|(number)[]|An matrix|

**Returns:**

|Type|Description|
|---|---|
|number|The sum of each row in a matrix|

## .math.spline

Perform cubic spline interpolation of given data points, returning either table of 
 data points obtained by the interpolation. If the x values are of categorical type, the index of 
 the table rows are used.


**Parameters:**

|Name|Type|Description|
|---|---|---|
|tbl|table|A table|
|x|symbol|A column from the table|
|y|symbol|A column from the table|

**Returns:**

|Type|Description|
|---|---|
|table|A table of data points after the cubic spline interpolation.|
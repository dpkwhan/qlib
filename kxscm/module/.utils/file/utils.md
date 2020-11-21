## .utils.download

Download files and uncompress them.

If the file to download is [http://www.example.com/afile.txt](http://www.example.com/afile.txt), 
then the base URL is [http://www.example.com/](http://www.example.com/).

The extention name for compressed files include:

- ``.zip`` for zipped file
- ``.gz`` for gzipped file, and 
- ``.tar.gz`` for tarred and zipped file


**Parameters:**

|Name|Type|Description|
|---|---|---|
|baseUrl|string|The base URL to download the file from|
|fileName|string \| string[]|File(s) to download|
|extName|string|Extention name of compressed file|
|unzipFunc|fn|A function to uncompress the downloaded file|

**Returns:**

|Type|Description|
|---|---|
|symbol|A file handle to the file downloaded|

**Example:** Download the market volume history for U.S. equities market in 2020

```q
 baseUrl:"http://markets.cboe.com/us/equities/market_statistics/historical_market_volume/";
 fileName:"market_history_2020.csv-dl";
 .utils.download[baseUrl;fileName;"";""]
```

## .utils.execFuncOnHandle

Execute a function on a handle to a remote q session


**Author**: David Han


**Parameters:**

|Name|Type|Description|
|---|---|---|
|h|hsym|a handle to a remote q session|
|fn|symbol|a function name|
|p|any[]|a list of parameters|

**Returns:**

|Type|Description|
|---|---|
|any|Return the result of the function call|

**Example:** Execute a function without parameter

```q
 twoSquared:{2*2};
 h:hopen `:localhost:5000;
 res:.utils.execFuncOnHandle[h;`twoSquared;(::)];
 hclose h;
 show res;
```


**Example:** Execute a function with one single parameter

```q
 tc:('[til;count]);
 h:hopen `:localhost:5000;
 res:.utils.execFuncOnHandle[h;`tc;(4 5 6 7 8 9)];
 hclose h;
 show res;
```


**Example:** Execute a function with one multiple parameters

```q
 add:{x+y};
 h:hopen `:localhost:5000;
 res:.utils.execFuncOnHandle[h;`add;(4;5)];
 hclose h;
 show res;
```

## .utils.getFuncName

Retrieve the function name.


**Parameter:**

|Name|Type|Description|
|---|---|---|
|f|fn|a function|

**Returns:**

|Type|Description|
|---|---|
|string|The function name of the given function|

**Example:** Show the current function name

```q
 .ex.logFuncName:{.utils.getFuncName .z.s};
 .ex.logFuncName[];
```

## .utils.toFixed

Format numerical values to a given decimal place.


**Author**: David Han


**Parameters:**

|Name|Type|Description|
|---|---|---|
|n|integer|Number of decimal points|
|v|number \| number[]|A single number or a list of numbers|

**Returns:**

|Type|Description|
|---|---|
|string \| string[]|A string or a list of strings|

**Example:** Format a single number to 2 decimal places

```q
 .utils.toFixed[2; 3.1415926]
```


**Example:** Format a list of numbers to 2 decimal places

```q
 .utils.toFixed[2;] 1.2 123 1.235 -123.5522
```


**Example:** Format a list of numbers of mixed types to 3 decimal places

```q
 .utils.toFixed[3;] (1.23456; 123j; 543i; -123.5522e)
```
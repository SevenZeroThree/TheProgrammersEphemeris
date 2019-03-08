---
title: "String.Format"
date: 2019-02-04T20:34:49-05:00
taxonomies:
    category: Method
---

The `String` object in the C# language exposes a method for string formatting that is very easy to use. The most common use case of the `string.Format` method is for passing a string representing the desired format as the first argument, and an array of objects to insert into the string.

The parameter indicators in the format string are 0 based indexes. The first parameter is {0}, the second is {1}, etc. Objects passed into the `string.Format` method will be converted to a string and placed into the format string at the indicated position.

See below for some examples on how to use the `string.Format` method.

## Method Signature

``` c#
public static string Format(string format, params object[] args);
```

## Standard Formatting

### Single Position

``` c#
using System;

public void Test()
{
    String.Format("This is a {0}", "Test");
}

// Output
/*
 *  This is a Test
 */

```

### Multiple Positions

``` c#
using System;

public void Test()
{
    int errorCode = 500;
    string errorMessage = "System unavailable";

    String.Format("An error occurred:  Code=[{0}] Message=[{1}]", errorCode, errorMessage);
}

// Output
/*
 *  An error occurred:  Code=[500] Message=[System unavailable]
 */

```

## Controlling the Format with a Format Identifier

Every index in the format string can be followed with a format identifier if desired. This will change the output of the object to the specified format. `{0:d}` applies the `d` formatting to the first object in the list, `{0:C2}` applies the `C` formatting with 2 decimal places to the first object in the list, and so on.

Several types support these format identifiers, including dates ([supported identifiers](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-date-and-time-format-strings)) and numbers ([supported identifiers](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings)).

### Date Formatting

``` c#
using System;

public void Test()
{
    String.Format("The current date and time is {0:d} at {0:t}", DateTime.Now);
}

// Output
/*
 *  The current date and time is 03/07/2019 at 01:52
 */

```

### Numeric Formatting

``` c#
using System;

public void Test()
{
    decimal price = 10.364324m;

    String.Format("The price is: {0:C2}", price);
}

// Output
/*
 *  The price is: $10.36
 */

```

### Padding

It is possible to control the padding for each of the positions in the format string. This padding can be used to left or right align the objects in the format string. A positive number indicates right-alignment, while a negative number will left align the field.

``` c#
using System;

public void Test()
{
    string.Format("{0:d} {1,12:N0}", DateTime.Now, 123456);
    string.Format("{0:d} {1,-12:N0} more data.", DateTime.Now, 123456);
}

// Output
/*
 *  3/6/19      123,456
 *  3/6/19 123,456      more data.
 */

```

## Exceptions

A `FormatException` will be thrown if the `format` argument is invalid, or if the index of an item is greater than or equal to the length of the `args` array.

## Alternatives

- string.Concat
- string interpolation
- StringBuilder

## Resources

Check out the [docs](https://docs.microsoft.com/en-us/dotnet/api/system.string.format) at Microsoft for more details.
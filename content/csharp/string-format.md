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
    const int errorCode = 500;
    const string errorMessage = "System unavailable";

    String.Format("An error occurred:  Code=[{0}] Message=[{1}]", errorCode, errorMessage);
}

// Output
/*
 *  An error occurred:  Code=[500] Message=[System unavailable]
 */

```

## Date Formatting

## Exceptions

## Alternatives

string.Concat

string interpolation

StringBuilder

## Resources

Check out the [docs](https://docs.microsoft.com/en-us/dotnet/api/system.string.format) at Microsoft for more details.
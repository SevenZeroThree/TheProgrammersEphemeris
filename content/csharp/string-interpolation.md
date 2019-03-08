---
title: "String Interpolation"
date: 2019-03-07
taxonomies:
    category: Concept
---

String interpolation provides an alternative to the `string.Format` method. While the end result is the same, string interpolation provides a more readable and convenient syntax for formatting strings. This feature is available in C# versions 6 and later.

To begin the string interpolation, the string must be prefixed with the `$` character:

``` c#
public void Test()
{
    var amount = 1.23;
    var message = $"The cost is {amount:C2}";
}

// Output
/*
 *  The cost is $1.23
 */

```

Example comparing `string.Format` to string interpolation:

``` c#
using System;

public void Test()
{
    int errorCode = 500;
    string errorMessage = "System unavailable";

    String.Format("An error occurred:  Code=[{0}] Message=[{1}]", errorCode, errorMessage);
    var message = $"An error occurred:  Code=[{errorCode}] Message=[{errorMessage}]";
}

// Output
/*
 *  An error occurred:  Code=[500] Message=[System unavailable]
 */

```

## Alternatives

- string.Concat
- [string.Format]({{< ref "/csharp/string-format.md" >}})
- StringBuilder

## Resources

Check out the [docs](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/tokens/interpolated) at Microsoft for more details.
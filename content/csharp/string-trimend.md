---
title: "String.TrimEnd"
date: 2019-03-08
taxonomies:
    category: Method
keywords: [string]
---

The `TrimEnd(char[])` method removes all trailing instances of the specified characters from a given string.

``` c#
public string TrimEnd(params char[] trimChars);
```

## Examples

``` c#

using System;

public class Program
{
    public static void Main()
    {
        char[] charsToTrim = { '*', ' ' };
        string message = "*** some string ***";
        Console.WriteLine(message.TrimEnd(charsToTrim));
    }
}

// Output
/*
 *  *** some string
 */

```
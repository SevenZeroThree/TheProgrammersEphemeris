---
title: "String.TrimStart"
date: 2019-03-08
taxonomies:
    category: Method
keywords: [string]
---

The `TrimStart(char[])` method removes all leading instances of the specified characters from a given string.

``` c#
public string TrimStart(params char[] trimChars);
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
        Console.WriteLine(message.TrimStart(charsToTrim));
    }
}

// Output
/*
 *  some string ***
 */

```
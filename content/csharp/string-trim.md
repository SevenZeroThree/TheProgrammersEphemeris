---
title: "String.Trim"
date: 2019-03-08
taxonomies:
    category: Method
keywords: [string]
---

There are 2 overloads to the `Trim()` method:

| Method        | Description |
| ------------- |-------------|
| [Trim()](#trim)        | Removes all leading and trailing whitespace from a given string. |
| [Trim(Char[])](#trim-char)  | Removes all leading and trailing instances of the specified characters from a given string      |

## Trim

The `Trim()` method removes all leading and trailing whitespace from a given string.

``` c#
public string Trim();
```

### Examples

``` c#

using System;

public class Program
{
    public static void Main()
    {
        var testString = "   some string   ";
        testString.Trim();
    }
}

// Output
/*
 *  some string
 */

```

## Trim(char[])

The `Trim(Char[])` method removes all leading and trailing instances of the specified characters from a given string.

``` c#
public string Trim(params char[] trimChars);
```

### Examples

``` c#

using System;

public class Program
{
    public static void Main()
    {
        char[] charsToTrim = { '*', ' ' };
        string message = "*** some string ***";
        Console.WriteLine(message.Trim(charsToTrim));
    }
}

// Output
/*
 *  some string
 */

```
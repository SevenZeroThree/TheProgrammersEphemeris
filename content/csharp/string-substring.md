---
title: "String.Substring"
date: 2019-03-09
taxonomies:
    category: Method
keywords: [string]
---

There are 2 overloads to the `Substring()` method:

| Method        | Description |
| ------------- |-------------|
| [Substring(Int32)](#substring-int32)        | Returns a substring from the specified string. It begins at the specified index and continues to the end of the string. |
| [Substring(Int32, Int32)](#substring-int32-int32)  | Returns a substring from the specified string. It begins at the specified index and continues to the specified length. |

## Substring(Int32)

The `Substring(Int32)` method returns a substring from the specified string. It begins at the specified index and continues to the end of the string.

``` c#
public string Substring(int startIndex);
```

The `Substring(Int32)` method is used to extract a substring from a string. The substring begins at the specified position and ends at the end of the string. The starting character position is a zero based index. The first character of the string begins at position 0, not 1. If the substring doesn't end at the end of the string, the [`Substring(Int32, Int32)`](#substring-int32-int32) method can be used.

This method does not modify the existing string. Instead, it returns a new string.

### Examples

``` c#

using System;

public class Program
{
    public static void Main()
    {
        var testString = "A test string";
        var message = testString.Substring(2);

        Console.WriteLine(message);
    }
}

// Output
/*
 *  test string
 */

```

## Substring(Int32, Int32)

The `Substring(Int32, Int32)` method returns a substring from the specified string. It begins at the specified index and continues to the specified length.

``` c#
public string Substring(int startIndex, int length);
```

The `Substring(Int32, Int32)` method is used to extract a substring from a string. The substring begins at the specified position and ends after the specified length. The starting character position is a zero based index. The first character of the string begins at position 0, not 1.

This method does not modify the existing string. Instead, it returns a new string.

### Examples

``` c#

using System;

public class Program
{
    public static void Main()
    {
        var testString = "A test string";
        var message = testString.Substring(2, 4);

        Console.WriteLine(message);
    }
}

// Output
/*
 *  test
 */

```
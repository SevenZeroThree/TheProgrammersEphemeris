---
title: "String.Format"
date: 2019-02-04T20:34:49-05:00
---

String formatting is an essential tool in any programming language. The string object in the C# language exposes a method for string formatting that is easy to use.

Check out the [docs](https://docs.microsoft.com/en-us/dotnet/api/system.string.format) at Microsoft for more details.

## Examples

The most common use case of the string.Format method is for passing a string representing the desired format as the first argument, and an array of objects to insert into the string.

The parameter indicators in the format string are 0 based indexes. The first parameter is {0}, the second is {1}, etc.

``` c#
public static string Format(string format, params object[] args);
```

### Standard Formatting

``` c#
public void Test()
{
    string.Format("This is a {0}", "Test");
}
```

Output

``` plain
This is a Test
```

### Date Formatting

### Exceptions

### Alternatives

string.Concat

string interpolation

StringBuilder

{{< gist SevenZeroThree 0733fd702948079fa176f46b126858d0 >}}
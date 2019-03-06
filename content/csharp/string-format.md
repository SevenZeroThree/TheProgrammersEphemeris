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

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras in suscipit felis. Mauris ac nunc eget leo aliquet viverra. Maecenas sed diam dui. Donec suscipit mauris nisi, quis volutpat magna sagittis at. Integer sed sapien posuere, finibus risus sed, semper velit. Nulla id vulputate lacus, vel posuere ligula. Integer ultrices aliquam erat vel blandit. Maecenas eget nulla quis velit congue varius.

Vestibulum in vulputate nunc. Cras commodo elit et sem pellentesque, sed mattis orci viverra. Nullam lobortis dapibus quam, eu convallis augue viverra sed. Nam viverra aliquam turpis, vitae dignissim ex sagittis in. Aenean at nibh lacus. Duis ac semper elit, eu facilisis augue. Suspendisse porta elit in magna convallis, nec finibus nulla rutrum. Donec sagittis ultrices libero vel vestibulum.

``` c#
public void Test()
{
    string.Format("This is a {0}", "Test");
}
```

Maecenas et justo a dolor auctor mattis. Aenean varius tempor porttitor. Vivamus tincidunt eros in lectus mattis scelerisque. Praesent non aliquet eros. Aenean elit sem, congue vel magna et, efficitur mattis turpis. Ut eget nibh egestas, mattis ex a, laoreet felis. Donec ultricies massa nec velit venenatis, et mattis tellus fringilla. Cras nec molestie urna. In nec commodo erat. Phasellus elementum nibh sed eleifend scelerisque. Sed lectus sem, posuere ac est sed, commodo elementum dui. Ut consequat arcu et dui dignissim ornare.

Vivamus volutpat ante vitae volutpat accumsan. Etiam volutpat ornare egestas. Nunc ultricies dapibus erat non malesuada. Nam eu fermentum nisi, in tristique lectus. Vivamus ut egestas mauris. Suspendisse non ante elit. Mauris non odio ornare, maximus lectus non, ultrices sapien. Donec non euismod neque. Donec eu commodo nisi. Quisque consectetur porttitor leo non dapibus. In eu mauris sem.

Praesent eget risus id eros commodo molestie. Etiam lobortis, quam sit amet fermentum facilisis, felis massa eleifend leo, id laoreet risus enim nec nibh. Phasellus cursus ornare sapien, in gravida sapien iaculis sit amet. Maecenas tincidunt ipsum in justo ultricies accumsan. Integer eu suscipit sem. Integer nulla risus, sollicitudin in imperdiet vulputate, commodo quis sem. Fusce fermentum nisl non laoreet eleifend. Mauris luctus a massa at vulputate. Praesent vel mi vel augue imperdiet sollicitudin. Nam viverra lectus commodo, tempor mauris id, laoreet nulla. Vivamus neque quam, suscipit convallis urna ac, imperdiet rutrum ante.
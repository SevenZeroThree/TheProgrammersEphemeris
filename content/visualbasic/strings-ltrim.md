---
title: "Strings.LTrim"
date: 2019-03-08
taxonomies:
    category: Method
keywords: [strings]
---

Leading whitespace can be removed from strings in Visual Basic using the `LTrim` method.

``` vb

Dim TestString As String = "  Extra spaces"
Dim TrimString As String

TrimString = LTrim(TestString)

' Output
' Extra spaces

```
---
title: "Strings.Trim"
date: 2019-03-08
taxonomies:
    category: Method
keywords: [strings]
---

Leading and trailing whitespace can be removed from strings in Visual Basic using the Trim method.

``` vb

Dim TestString As String = "  Extra spaces  "
Dim TrimString As String

TrimString = Trim(TestString)

' Output
' Extra spaces

```
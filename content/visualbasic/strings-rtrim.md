---
title: "Strings.RTrim"
date: 2019-03-08
taxonomies:
    category: Method
keywords: [strings]
---

Trailing whitespace can be removed from strings in Visual Basic using the `RTrim` method.

``` vb

Dim TestString As String = "Extra spaces  "
Dim TrimString As String

TrimString = RTrim(TestString)

' Output
' Extra spaces

```
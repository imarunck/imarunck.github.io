---
layout: post
title: Naming the “Glyphs”?
date: 2024-07-13
categories: blog english article
author: arun
image: /assets/images/dot.jpg
image1: /assets/images/glyph1.png
image2: /assets/images/glyph2.png
tag: type design
---
## Why shouldn’t we use dots When naming the “Glyphs”? in python scripting.

> #### While technically it's possible to use dots in Python object (Glyphs) names, it is strongly **discouraged**.

## When using underscores ✓
![]({{page.image1 | relative_url}})

## When using dot ✗
![]({{page.image2 | relative_url}})


## Here’s why:
* In Type Design Software we can’t use the “Go to Glyph” option while python scripting.
* Because the dot (.) is a special character in Python.
* Syntax Errors: Using dots in names would lead to syntax errors. For example, trying to name a variable my.var would result in an error because Python interprets the dot as an attempt to access an attribute var of an object my.
* Code Readability: Even if it were allowed, using dots in names would significantly reduce code readability and maintainability. It would be unclear whether a dot is meant to separate components of an object name or to access an attribute or method.
* PEP 8, the style guide for Python code, recommends using lowercase letters, numbers, and underscores for variable and object names.

## Alternative:

To avoid these issues, stick to standard naming conventions, such as using underscores (_) to separate words in names (my_var, my_function) and following PEP 8 guidelines for Python code style.

> Example: Instead of my.object.name, use my_object_name.

_____
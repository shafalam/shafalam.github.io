---
layout: post
title: Java Cheatsheet
---


Below are the few necessary methods I often look for:

### Sub Array
Arrays.copyOf(int[] original, int from, int to)

`from` must be within the `original.length`. `to` can be greater than or euqal to `from`.

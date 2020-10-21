---
layout: post
title: Today I Learnt
---

## 27.09.2020

## Java LinkedList can be used both as Stack and Queue

While using LinkedList as Stack use `push()` method to add and `pop()` method to retrieve an element.

And for Queue, use `add()` to add and `poll()` to remove an element from the queue.

## 20.10.2020

## Escaping twice inside a string

### The problem:

I was trying to use `querySelector()` function to get an element by an attribute. However the attribute was not so standard css attribute. It was like `row:id`.

So, whenever I was trying to query like this way: `document.querySelector('["row:id"]')`, it threw a syntax error that `row:id` is not a valid selector.

### The solution:

I needed to escape the ":" twice. Once for the javascript itself and another for the css.
So, I ended up writing this way `document.querySelector('["row\\:id"]')`. This time it worked. :D

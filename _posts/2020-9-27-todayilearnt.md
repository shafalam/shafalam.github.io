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

## 07.12.2020

### The problem:

I needed a data structure that can identify duplicate while inserting and can be retrieved by using an index.

### The solution:

First issue can be solved by using HashSet. I was aware of that. I just didn't know that HashSet can be converted into an `Object[]` array. Like this:
`Object[] array = set.toArray()`

After that, I can retrieve any value by simply indexing and casting to a data type. i.e.
`int val = (int) array[i]`

## 17.12.2020

### The problem:

Suppose you have two strings `s1 = watercooler` and `s2 = ercoolerwat`. Determine `s2` is a rotated array of `s1`. You can only use `isSubstring()` method only once.
This constraint makes this problem a bit difficult to solve.

### The solution:

We can always divide a string into x and y. Like `s1 = x + y`. In this case, `x = wat` and `y = cooler`.
For s2 it becomes `s2 = y + x`.

Now, what if we concatenate the `s1` twice. `s1s1 = x + y + x + y = x + s2 + y`
Now we can use `isSubtring` only once and get our desired result.

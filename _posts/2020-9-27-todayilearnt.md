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

## 03.01.2021

### The problem:

`5/2` returns 2.0
I expected 2.5.

### Solution:

`(double)5 / 2` returns 2.5
Reason is: When java performs division, it assumes 5 as int and divides accordingly. So, we need to tell java that in this case 5 is not int rather double and divide it accordingly.

### Problem:

Oftentimes, I have to disregard all non-letters in a sentence. I used to create a hashset containing all the punctuations. Then while traversing through the string, I would check in the hashset.
Which is inefficient.

### Better Way:

Replace all the non-letter characters with spaces. Then while traversing only look for the space.
E.g.: `"this is a very short sentence! I wonder, why?".replaceAll("[^a-zA-Z0-9]", " ");`

Here we are using a regex which simply looks for everything except a-z, A-Z and 0-9.

## 14.03.2021

### Problem: Converting an arryList of integer array to a 2D int array.

### Solution:

```
    List<int[]> list = new ArrayList<int[]>();
    int[][] arr = list.toArray(new int[list.size()][list.get(0).length]);
```

## 17.03.2021

### Problem: When you want to use wildcard matching but don't want to go through the complexities of regex, what can you do?

### Solution: You can use glob pattern. It's not as powerful or flexible as RegEx, however, it's quite simple to use. In many cases it's good enough for wildcard searching. E.g. `src/*.js` will find all the javascript files inside the src directory.

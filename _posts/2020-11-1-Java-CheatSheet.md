---
layout: post
title: Java Cheatsheet
---

Below are the few necessary methods I often look for:

### Sub Array

Arrays.copyOfRange(int[] original, int from, int to)

`from` must be within the `original.length`. `to` can be greater than or euqal to `from`.

### Substring

string.subtring(int beginIndex, int endIndex)

`beginIndex` is inclusive of the substring and `endIndex` is exclusive of the substring.

### SubList
list.subList(int beginIndex, int endIndex);
`endIndex` exclusive.

### Some usefull Collections method
`Collections.sort(list, customComparator);`
`Collections.reverse(list)` it will reverse the list

### Is letter?

Character.isLetter('a')

### Implement a custom comparator
```
    Comparator<String> comp = new Comparator<String>(){
        @Override
        public int compare(String a, String b){
            return b.compareTo(a);
        }
    };
```

### Things to remember while implementing a custom comparator
Giver two data x and y
0: if (x==y)
-1: if (x < y)
1: if (x > y)


### string.split() function can take second parameter 
`String[] word = "function can take second parameter".split(" ",2);`
`word` will have `["function","can take second parameter"]`

### string.trim() will remove empty space from corner
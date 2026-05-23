---
tags: [mistake]
---
# Off-by-one Error

### Goal
I wanted to access the last element of an array using its length property.

### Problem
I used `array[array.length]` instead of `array[array.length - 1]`, resulting in an undefined value. Sometimes this triggers a [[Null Pointer Exception]] down the line. It's almost as bad as an [[Infinite Loop Error]].

### Fix
I corrected the index to `array.length - 1`. I also added a unit test to catch edge cases for empty arrays.

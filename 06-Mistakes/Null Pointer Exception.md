---
tags: [mistake]
---
# Null Pointer Exception

### Goal
I was trying to access a property of an object returned from an API call.

### Problem
The API call failed, and the object was null. I didn't check for null before accessing the property. This was caused by an [[Off-by-one Error]] on the backend. This is also related to my [[Uncaught Promise Rejection]].

### Fix
I added optional chaining (`object?.property`) and a null check before accessing properties.

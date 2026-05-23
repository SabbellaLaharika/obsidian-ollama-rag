---
tags: [mistake]
---
# Infinite Loop Error

### Goal
I wanted to iterate through a list and process each item until the list was empty.

### Problem
I forgot to remove items from the list during iteration, causing an infinite loop. This is a common error, similar to an [[Off-by-one Error]].

### Fix
I added a `list.pop()` inside the while loop to ensure the condition eventually evaluates to false. Also checking the [[Database Connection Timeout]] since it masked the real issue initially.

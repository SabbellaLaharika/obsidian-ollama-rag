---
tags: [mistake]
---
# Uncaught Promise Rejection

### Goal
I wanted to fetch user data asynchronously and display it on the screen.

### Problem
I didn't wrap my async/await call in a try/catch block, so when the network failed, the app crashed. Sometimes a [[Null Pointer Exception]] causes a similar crash. This might happen due to a [[Database Connection Timeout]].

### Fix
I added a `try...catch` block around the async code to gracefully handle the error and show a user-friendly message.

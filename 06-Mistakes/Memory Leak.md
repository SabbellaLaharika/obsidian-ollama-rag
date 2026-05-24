---
tags: [mistake]
---
# Memory Leak

### Goal
I wanted to keep a background process running to listen for real-time WebSocket events.

### Problem
I failed to properly close event listeners when the React component unmounted. This caused thousands of listeners to pile up, crashing the browser tab. This feels similar to an [[Infinite Loop Error]] because it locks up the main thread. It's fundamentally an issue of mismanaging [[Data Structures]] that store the callbacks.

### Fix
I added a cleanup function in the `useEffect` hook to explicitly call `.removeEventListener()` before unmounting.

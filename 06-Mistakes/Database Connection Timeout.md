---
tags: [mistake]
---
# Database Connection Timeout

### Goal
I needed to connect to the PostgreSQL database on application startup.

### Problem
The database URL was pointing to the wrong port, leading to a timeout after 30 seconds. This blocked the startup and eventually threw an [[Uncaught Promise Rejection]]. I initially thought it was an [[Infinite Loop Error]].

### Fix
I corrected the port number in the environment variables and decreased the connection timeout to 5 seconds to fail faster.

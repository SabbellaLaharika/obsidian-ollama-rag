---
tags: [mistake]
---
# Incorrect API Endpoint

### Goal
I wanted to fetch user profile data from the backend to display on the dashboard.

### Problem
I misspelled the API endpoint (`/api/usrs` instead of `/api/users`), which returned a 404 error. Because of this, the frontend data object was empty, leading to a [[Null Pointer Exception]] later in the render cycle. It also triggered an [[Uncaught Promise Rejection]].

### Fix
I corrected the spelling in the Axios request and added a global constant file for API routes to prevent hardcoding URLs in the future.

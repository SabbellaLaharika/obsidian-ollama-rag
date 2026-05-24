---
tags: [mistake]
---
# Git Rebase Conflict

### Goal
I wanted to update my feature branch with the latest changes from the main branch to keep the [[Knowledge Base Project]] history clean.

### Problem
I ran a rebase instead of a merge, resulting in multiple conflicts across several commits. In the confusion, I accidentally dropped a commit related to my [[Database Connection Timeout]] fix.

### Fix
I immediately aborted the rebase (`git rebase --abort`). I reviewed Git logs and used a standard `git merge main` instead, handling the conflict safely in one unified step.

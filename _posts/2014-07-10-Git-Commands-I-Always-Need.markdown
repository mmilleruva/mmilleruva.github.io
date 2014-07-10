---
layout: post
title:  "Git Commands I Always Need"
date:   2014-07-10 23:08:03
categories: Git
---


## `git fetch origin --prune`
At work we follow the github git workflow
and I always have trouble cleaning up branches that were deleted on master. This command will do that for you.

## `git clean -f`
This command will **remove** any untracked files from your directory. This is great for getting your directory back to a clean state.

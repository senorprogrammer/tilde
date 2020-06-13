---
date: 2020-06-12T21:41:47-07:00
title: Remove All Docker Images
tags: 
---

# Remove All Docker Images

```bash
❯ docker volume rm $(docker volume ls -q)
```
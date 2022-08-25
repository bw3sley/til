---
title: "Remover um `git worktree` que não será mais usado"
author: "bw3sley"
slug: "remove-unused-git-worktree"
tags:
  - git
  - worktree
created_at: "2025-11-27"

---

# Remover um `git worktree` que não será mais usado

Depois de terminar trabalho naquele diretório, use `git worktree remove` para desfazer registro do worktree e apagar pasta vinculada.

```bash
git worktree remove ../til-feature
```

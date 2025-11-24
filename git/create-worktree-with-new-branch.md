---
title: "Criar um `git worktree` com uma nova branch"
author: "bw3sley"
slug: "create-git-worktree-with-new-branch"
tags:
  - git
  - worktree
  - branch
created_at: "2026-07-04"

---

# Criar um `git worktree` com uma nova branch

O comando `git worktree add -b` cria um novo diretório de trabalho e já inicializa uma branch nova apontando para base escolhida.

```bash
git worktree add ../til-feature -b feature/worktree origin/main
```

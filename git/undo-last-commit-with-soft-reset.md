---
title: "Voltar o último commit sem perder alterações"
author: "bw3sley"
slug: "undo-last-commit-with-soft-reset"
tags:
  - git
  - reset
  - commits
created_at: "2023-01-11"

---

# Voltar o último commit sem perder alterações

O comando `git reset --soft HEAD~1` desfaz o último commit, mas mantém as mudanças no stage para você ajustar e commitar de novo.

```bash
git reset --soft HEAD~1
```

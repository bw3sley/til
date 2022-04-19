---
title: "Remover uma branch local"
author: "bw3sley"
slug: "remove-a-local-branch"
tags:
  - git
  - branch
created_at: "2026-07-05"

---

# Remover uma branch local

Use `git branch -d` para apagar uma branch local que já foi integrada. Se quiser forçar a remoção, use `-D`.

```bash
git branch -d feature/login
git branch -D feature/login
```

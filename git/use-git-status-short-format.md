---
title: "Usar `git status --short` para ver mudanças resumidas"
author: "bw3sley"
slug: "use-git-status-short-format"
tags:
  - git
  - status
  - cli
created_at: "2024-07-06"

---

# Usar `git status --short` para ver mudanças resumidas

`git status --short` mostra estado dos arquivos em formato compacto. Ele exibe mudanças entre index e working tree com códigos curtos como `M`, `A` e `??`.

Exemplo: `M` indica arquivo modificado, `A` arquivo adicionado e `??` arquivo ainda não rastreado.

```bash
git status --short
```

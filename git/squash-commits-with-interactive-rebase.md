---
title: "Juntar commits com rebase interativo"
author: "bw3sley"
slug: "squash-commits-with-interactive-rebase"
tags:
  - git
  - rebase
  - commits
created_at: "2022-05-17"

---

# Juntar commits com rebase interativo

Para transformar vários commits em um só, abra um rebase interativo e marque os commits seguintes como `squash`.

```bash
git rebase -i HEAD~3
# troque pick por squash nos commits que serão agrupados
```

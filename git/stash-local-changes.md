---
title: "Guardar mudanças locais com `git stash`"
author: "bw3sley"
slug: "stash-local-changes"
tags:
  - git
  - stash
created_at: "2022-05-17"

---

# Guardar mudanças locais com `git stash`

Quando precisar trocar de contexto sem commitar, `git stash` ajuda a guardar alterações locais fora do commit atual.

## Guardar alterações

O comando `git stash` salva mudanças não commitadas em uma pilha temporária.

```bash
git stash
```

## Reaplicar sem remover

Use `git stash apply` quando quiser restaurar o conteúdo guardado, mas manter o stash disponível na pilha.

```bash
git stash apply
```

## Reaplicar e remover

Use `git stash pop` quando quiser restaurar o conteúdo guardado e já remover essa entrada da pilha.

```bash
git stash pop
```

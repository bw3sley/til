---
title: "Seguir logs de um container em tempo real"
author: "bw3sley"
slug: "follow-container-logs-in-real-time"
tags:
  - docker
  - containers
  - logs
created_at: "2026-07-04"

---

# Seguir logs de um container em tempo real

O comando `docker logs -f` mantém saída aberta e mostra novas linhas assim que container escreve nos logs.

```bash
docker logs -f minha-api
```
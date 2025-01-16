---
title: "Remover imagens Docker sem uso"
author: "bw3sley"
slug: "remove-unused-docker-images-with-prune"
tags:
  - docker
  - images
  - cleanup
created_at: "2024-04-01"

---

# Remover imagens Docker sem uso

Use `docker image prune` para apagar imagens dangling, liberando espaço sem remover imagens ainda referenciadas por containers.

```bash
docker image prune
```

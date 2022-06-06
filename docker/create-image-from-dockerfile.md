---
title: "Criar uma imagem a partir de um `Dockerfile`"
author: "bw3sley"
slug: "create-image-from-dockerfile"
tags:
  - docker
  - images
  - dockerfile
created_at: "2026-07-04"

---

# Criar uma imagem a partir de um `Dockerfile`

Para gerar uma imagem Docker a partir do `Dockerfile` do diretório atual, use `docker build` com a tag desejada.

```bash
docker build -t minha-api:latest .
```

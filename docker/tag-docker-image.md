---
title: "Adicionar uma tag em uma imagem Docker"
author: "bw3sley"
slug: "tag-docker-image"
tags:
  - docker
  - images
  - tags
created_at: "2022-06-07"

---

# Adicionar uma tag em uma imagem Docker

O comando `docker tag` cria outro nome para a mesma imagem, útil para preparar envio para registry ou marcar versão.

```bash
docker tag minha-api:latest bw3sley/minha-api:v1
```

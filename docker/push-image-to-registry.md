---
title: "Enviar uma imagem Docker para um registry"
author: "bw3sley"
slug: "push-image-to-registry"
tags:
  - docker
  - images
  - registry
created_at: "2022-06-08"

---

# Enviar uma imagem Docker para um registry

Depois de taguear a imagem com nome compatível com registry, use `docker push` para publicar essa tag.

```bash
docker push bw3sley/minha-api:v1
```

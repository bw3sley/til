---
title: "Remover containers e volumes do Docker Compose"
author: "bw3sley"
slug: "remove-compose-containers-and-volumes"
tags:
  - docker
  - compose
  - volumes
created_at: "2024-04-02"

---

# Remover containers e volumes do Docker Compose

O comando `docker compose down -v` derruba os serviços e também remove os volumes associados ao projeto.

```bash
docker compose down -v
```

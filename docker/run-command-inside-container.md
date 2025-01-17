---
title: "Executar comando dentro de um container em execução"
author: "bw3sley"
slug: "run-command-inside-running-container"
tags:
  - docker
  - containers
  - exec
created_at: "2022-06-10"

---

# Executar comando dentro de um container em execução

Use `docker exec` quando precisar rodar um comando em um container já iniciado, como abrir shell ou inspecionar arquivos.

```bash
docker exec -it minha-api sh
```

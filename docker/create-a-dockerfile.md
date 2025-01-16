---
title: "Definir imagem com um `Dockerfile`"
author: "bw3sley"
slug: "define-image-with-dockerfile"
tags:
  - docker
  - dockerfile
created_at: "2022-06-09"

---

# Definir imagem com um `Dockerfile`

O `Dockerfile` descreve como a imagem deve ser montada, incluindo imagem base, diretório de trabalho e comando inicial.

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY . .
RUN npm install
CMD ["npm", "run", "dev"]
```

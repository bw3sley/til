---
title: "Usar multi-stage build para reduzir imagem de uma API"
author: "bw3sley"
slug: "use-multi-stage-build-for-api-image"
tags:
  - docker
  - dockerfile
  - api
  - images
created_at: "2022-06-16"

---

# Usar multi-stage build para reduzir imagem de uma API

No multi-stage build, dependencias de build ficam em um estágio separado e imagem final recebe só artefatos e dependencias de runtime.

Isso evita levar código temporário, cache e ferramentas de compilação para container da API.

```dockerfile
FROM node:20-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm ci
COPY . .
RUN npm run build

FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --omit=dev
COPY --from=builder /app/dist ./dist
CMD ["node", "dist/server.js"]
```

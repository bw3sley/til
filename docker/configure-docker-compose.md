# Configurar o `docker-compose.yml`

Para deixar o docker configurável por outros usuários, é necessário criar um arquivo `docker-compose.yml`

```bash
version: "3"

services:
  api-solid-pg:
    image: bitnami/postgresql
    ports: 
      - 5432:5432
    environment:
      - POSTGRESQL_USERNAME=docker
      - POSTGRESQL_PASSWORD=docker
      - POSTGRESQL_DATABASE=apisolid
```

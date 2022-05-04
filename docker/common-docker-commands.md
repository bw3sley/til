# Comandos comuns do Docker

- Para criar um banco de dados POSTGRESQL com a imagem da bitnami/postgresql

```bash
docker run --name api-solid-pg -e POSTGRESQL_USERNAME=docker -e POSTGRESQL_PASSWORD=docker -e POSTGRESQL_DATABASE=apisolid -p 5432:5432 bitnami/postgresql
```

- Listar os container que estão em execução

```bash
docker ps
```

- Listar os últimos containers criados

```bash
docker ps -a
```

- Rodar um já criado container

```bash
docker start NOME_DO_DOCKER ou ID_DO_DOCKER

// Example: docker start api-solid-pg
```

- Parar um container que está executando

```bash
docker stop NOME_DO_DOCKER ou ID_DO_DOCKER
```

- Remover um container criado

```bash
docker rm NOME_DO_DOCKER
```

- Seguindo os logs

```bash
docker logs api-solid-pg -f
```

- Para deixar o docker configurável por outros usuários, é necessário criar um arquivo `docker-compose.yml`

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

- Para rodar o arquivo `docker-compose.yml` basta digitar

```bash
docker compose up -d
```

- Para parar o container sem deletar ele

```bash
docker compose stop
```

- Para deletar e parar de rodar um container de um arquivo `docker-compose.yml`
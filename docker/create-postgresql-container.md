# Criar PostgreSQL container

Para criar um banco de dados POSTGRESQL com a imagem da bitnami/postgresql

```bash
docker run --name api-solid-pg -e POSTGRESQL_USERNAME=docker -e POSTGRESQL_PASSWORD=docker -e POSTGRESQL_DATABASE=apisolid -p 5432:5432 bitnami/postgresql
```
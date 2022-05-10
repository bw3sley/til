# Listar Bancos de Dados e Tabelas

Se você iniciou uma sessão no [MySQL](https://dev.mysql.com/), mas ainda não se conectou a um banco de dados específico, pode listar os bancos de dados disponíveis assim:

```sql
> show databases;
+-----------------------------+
| Database                    |
+-----------------------------+
| information_schema          |
| my_app_dev                  |
+-----------------------------+
```

Se você estiver curioso sobre as tabelas em um banco de dados específico, pode listá-las especificando o nome do banco de dados:

```sql
> show tables in my_app_dev;
+------------------------------+
| Tables_in_my_app_dev         |
+------------------------------+
| pokemons                     |
| trainers                     |
+------------------------------+
```

Alternativamente, você pode se conectar ao banco de dados de interesse e, a partir daí, não é necessário especificar o nome do banco de dados nas próximas consultas.

```sql
> use my_app_dev;
> show tables;
+------------------------------+
| Tables_in_my_app_dev         |
+------------------------------+
| pokemons                     |
| trainers                     |
+------------------------------+
```

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)
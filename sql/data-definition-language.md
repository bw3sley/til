# DDL - Linguagem de Definição de Dados

**DDL** (*Data Definition Language*) é um conjunto de comandos SQL usados para criar, modificar e excluir estruturas do banco de dados, mas não os dados em si. Esses comandos geralmente não são utilizados por usuários finais, que acessam o banco de dados por meio de uma aplicação.

</br>

## CREATE

O comando `CREATE` é usado para criar bancos de dados ou seus objetos (como tabelas, índices, funções, views, procedures e triggers).

Exemplo:

```sql
CREATE DATABASE Loja;

CREATE TABLE Clientes (
    Id BIGINT PRIMARY KEY IDENTITY,
    NomeCliente VARCHAR(50),
    GeneroCliente CHAR(1)
);
```

</br>

## DROP

O comando `DROP` é usado para excluir objetos do banco de dados.

Exemplo:

```sql
DROP DATABASE Loja;

DROP TABLE Clientes;
```

</br>

## ALTER

O comando `ALTER` é utilizado para alterar a estrutura de objetos existentes no banco de dados.

### Adicionando colunas

Exemplo:

```sql
ALTER TABLE Estudantes ADD (Idade NUMERIC(5,2), Curso VARCHAR(40));
```

### Modificando colunas

Exemplo:

```sql
ALTER TABLE Estudantes ALTER COLUMN Curso VARCHAR(20);
```

### Removendo colunas

Exemplo:

```sql
ALTER TABLE Estudantes DROP COLUMN Curso;
```

</br>

## TRUNCATE

O comando `TRUNCATE` é utilizado para remover todos os registros de uma tabela, liberando o espaço alocado para esses dados.

- `TRUNCATE` é extremamente rápido e ideal para esvaziar tabelas temporárias.
- Ele preserva a estrutura da tabela para uso futuro, ao contrário do `DROP`, que apaga a tabela por completo.
- Exclusões feitas com `DROP` não podem ser desfeitas (*rollback*), por isso, o comando deve ser usado com cautela.

Exemplo:

```sql
TRUNCATE TABLE Clientes;
```

## Referências

- [📄 W3Schools — SQL DDL](https://www.w3schools.com/sql/sql_ref_ddl.asp)
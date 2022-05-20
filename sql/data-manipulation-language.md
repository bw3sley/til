# DML - Linguagem de Manipulação de Dados

Os comandos SQL que lidam com a manipulação de dados presentes no banco de dados fazem parte da **DML** (*Data Manipulation Language*). Esses comandos permitem inserir, atualizar e excluir dados em tabelas. Além disso, é uma parte essencial do SQL que controla o acesso e a modificação dos dados armazenados.

</br>

## INSERT

O comando **INSERT** é usado para inserir registros ou linhas em uma tabela do banco de dados. No comando **INSERT**, é necessário especificar o nome das colunas e os respectivos valores que serão inseridos.

Exemplo:

```sql
INSERT INTO Cliente (
    Nome_Cliente, 
    Genero_Cliente, 
    Email_Cliente
) 
VALUES (
    'Wesley', 
    'M', 
    'w3sley@example.com'
);
```

</br>

## UPDATE

O comando **UPDATE** é utilizado para modificar valores existentes em colunas de uma tabela do banco de dados.

Exemplo:

```sql
UPDATE Cliente 
    SET Email = 'exemplo@exemplo.com' 
WHERE Id_Cliente = 1;
```

### Atualizando mais de um valor

Exemplo:

```sql
UPDATE Cliente 
    SET Genero_Cliente = 'M' 
WHERE Id_Cliente IN (1, 2, 3, 4);
```

### UPDATE usando JOIN

Exemplo:

```sql
UPDATE Users 
    SET Biography = 'Novo conteúdo'
FROM Users
INNER JOIN Biography
    ON Users.Id = Biography.FK_Id_User
WHERE Users.Id = 3;
```

</br>

## DELETE

O comando **DELETE** é utilizado para remover uma ou mais linhas de uma tabela do banco de dados. Esse comando não apaga permanentemente os registros, permitindo realizar um **ROLLBACK** caso necessário. É possível usar a cláusula **WHERE** para filtrar quais registros serão deletados.

Exemplo:

```sql
DELETE FROM Cliente
WHERE Id_Cliente = 1;
```

### Deletando mais de um valor

Exemplo:

```sql
DELETE FROM Cliente
WHERE Id_Cliente IN (1, 2, 3, 4);
```

### DELETE usando JOIN

Exemplo:

```sql
DELETE Users
FROM Users
INNER JOIN Biography
    ON Users.Id = Biography.FK_Id_User
WHERE Users.Id = 3;
```

## Referências

- [📄 W3Schools — SQL DML](https://www.w3schools.com/sql/sql_ref_dml.asp)
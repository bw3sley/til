# DCL – Linguagem de Controle de Dados

A **DCL** (*Data Control Language*) é um subconjunto do SQL utilizado para controlar o acesso e os privilégios dos usuários em um banco de dados. Os comandos DCL permitem conceder ou revogar permissões sobre objetos do banco, garantindo a segurança e o controle adequado dos dados.

</br>

## Principais Comandos DCL

### GRANT

O comando **GRANT** é usado para conceder privilégios a usuários ou roles (funções) em tabelas, views, procedimentos armazenados ou em todo o banco de dados.

Exemplo:

```sql
GRANT SELECT, INSERT, UPDATE 
ON Customers 
TO UserName;
```

Este comando concede ao usuário **UserName** permissão para realizar **SELECT**, **INSERT** e **UPDATE** na tabela **Customers**.

---

### REVOKE

O comando **REVOKE** remove privilégios previamente concedidos a usuários ou roles.

Exemplo:

```sql
REVOKE SELECT, INSERT 
ON Customers 
FROM UserName;
```

Este comando revoga as permissões de **SELECT** e **INSERT** do usuário **UserName** na tabela **Customers**.

---

## Permissões Comuns em DCL

- **SELECT** — Permite ler dados de uma tabela ou view.  
- **INSERT** — Permite inserir novos registros em uma tabela.  
- **UPDATE** — Permite modificar registros existentes.  
- **DELETE** — Permite remover registros de uma tabela.  
- **EXECUTE** — Permite executar stored procedures ou funções.  
- **ALL PRIVILEGES** — Concede todas as permissões disponíveis.

---

## Exemplo Completo

### Concedendo todas as permissões a um usuário:

```sql
GRANT ALL PRIVILEGES 
ON Orders 
TO AdminUser;
```

### Revogando todas as permissões:

```sql
REVOKE ALL PRIVILEGES 
ON Orders 
FROM AdminUser;
```

## Referências

- [📄 W3Schools — SQL GRANT and REVOKE](https://www.w3schools.com/sql/sql_grant_revoke.asp)  
- [📄 Documentação Microsoft — GRANT (Transact-SQL)](https://learn.microsoft.com/en-us/sql/t-sql/statements/grant-transact-sql)
# Criando Procedures no MySQL

Procedures (ou procedimentos armazenados) são blocos de código SQL salvos no banco de dados que podem ser executados para realizar uma tarefa específica. Eles são úteis para encapsular lógica SQL e reutilizar o código em várias partes de um aplicativo.

## Exemplo de criação de uma procedure

Vamos criar uma procedure simples que exibe informações de um usuário com base no ID fornecido.

```sql
DELIMITER //

CREATE PROCEDURE GetUserInfo(IN userId INT)
BEGIN
    SELECT * FROM users WHERE id = userId;
END //

DELIMITER ;
```

### Explicação:

- `DELIMITER //`: Altera o delimitador temporariamente para `//`, permitindo que usemos `;` dentro da procedure sem encerrar sua definição.
- `CREATE PROCEDURE GetUserInfo(IN userId INT)`: Define a procedure `GetUserInfo` que recebe um parâmetro de entrada `userId` do tipo `INT`.
- `BEGIN ... END`: Delimita o bloco de código da procedure.
- `SELECT * FROM users WHERE id = userId;`: Executa uma consulta que retorna as informações do usuário com o `id` especificado.

## Chamando uma Procedure

Para chamar a procedure `GetUserInfo` e visualizar os dados de um usuário específico, execute:

```sql
CALL GetUserInfo(1);
```

Esse comando executa a procedure com o `userId` fornecido, retornando os dados do usuário com ID igual a 1.

## Vantagens de Usar Procedures:

- **Reutilização de código**: Evita repetir lógica SQL.
- **Performance**: Procedures podem ser otimizadas pelo banco de dados.
- **Segurança**: Permite encapsular lógica sem expor o código ao cliente.
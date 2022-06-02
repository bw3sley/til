# Transações

As **transações** agrupam um conjunto de tarefas em uma única unidade de execução. Cada transação inicia com uma tarefa específica e termina quando todas as tarefas do grupo são concluídas com sucesso. Se qualquer uma das tarefas falhar, toda a transação falha. Portanto, uma transação tem apenas dois resultados possíveis: **sucesso** ou **falha**.

</br>

## COMMIT

Se todas as instruções em uma transação forem executadas corretamente, as alterações são gravadas permanentemente no banco de dados. O comando **COMMIT** salva todas as alterações feitas desde o último **COMMIT** ou **ROLLBACK**.

Exemplo:

```sql
BEGIN TRAN
    UPDATE Customer
        SET Customer.CustomerName = 'w3sLeYY'
    WHERE Customer.Id > 2;

COMMIT TRAN;
```

---

## ROLLBACK

Se ocorrer algum erro em qualquer uma das instruções SQL agrupadas, todas as alterações feitas até aquele momento serão desfeitas. O comando **ROLLBACK** reverte todas as alterações desde o último **COMMIT** ou **SAVE TRANSACTION**.

Exemplo:

```sql
BEGIN TRAN
    UPDATE Customer
        SET Customer.CustomerName = 'w3sLeYY'
    WHERE Customer.Id > 2;

ROLLBACK TRAN;
```

---

## SAVE TRANSACTION

No **SQL Server**, o comando **SAVE TRANSACTION** cria um ponto de salvamento dentro de uma transação. Você pode reverter até esse ponto usando o **ROLLBACK** sem desfazer toda a transação.

Exemplo:

```sql
BEGIN TRAN;

    UPDATE Accounts SET Balance = Balance - 500 WHERE AccountID = 1;

    SAVE TRANSACTION SavePoint1;

    UPDATE Accounts SET Balance = Balance + 500 WHERE AccountID = 2;

    -- Revertendo até o ponto de salvamento
    ROLLBACK TRAN SavePoint1;

COMMIT TRAN;
```

Neste exemplo, o **ROLLBACK TRAN SavePoint1** desfaz apenas as alterações feitas após o **SAVE TRANSACTION SavePoint1**, mantendo as anteriores.

---

### Observações sobre **SAVE TRANSACTION** no SQL Server:

- Diferente do **SAVEPOINT** em outros bancos como Oracle ou PostgreSQL, no SQL Server o ponto criado por **SAVE TRANSACTION** não pode ser removido explicitamente (não há equivalente ao **RELEASE SAVEPOINT**).
  
- Você pode criar vários pontos de salvamento em uma transação e reverter para qualquer um deles.

---

## Referências

- [📄 Documentação Microsoft — BEGIN TRANSACTION (Transact-SQL)](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/begin-transaction-transact-sql)  
- [📄 Documentação Microsoft — SAVE TRANSACTION (Transact-SQL)](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/save-transaction-transact-sql)
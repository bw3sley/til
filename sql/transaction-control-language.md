# TCL – Linguagem de Controle de Transações

A **TCL** (*Transaction Control Language*) é um subconjunto do SQL responsável por gerenciar transações em um banco de dados. Os comandos TCL garantem que as operações realizadas em uma transação sejam executadas corretamente e de forma consistente, seguindo as propriedades **ACID** (Atomicidade, Consistência, Isolamento e Durabilidade).

Os comandos TCL permitem confirmar, desfazer ou salvar pontos dentro de uma transação.

</br>

## Principais Comandos TCL

---

### COMMIT

O comando **COMMIT** confirma todas as alterações feitas durante a transação atual, tornando-as permanentes no banco de dados.

Exemplo:

```sql
BEGIN TRANSACTION;

UPDATE Accounts 
SET Balance = Balance - 500 
WHERE AccountID = 1;

UPDATE Accounts 
SET Balance = Balance + 500 
WHERE AccountID = 2;

COMMIT;
```

Neste exemplo, a transferência entre contas só será concluída após o **COMMIT**, garantindo a integridade dos dados.

---

### ROLLBACK

O comando **ROLLBACK** desfaz todas as alterações feitas desde o último **COMMIT** ou **SAVEPOINT**, retornando o banco de dados ao estado anterior.

Exemplo:

```sql
BEGIN TRANSACTION;

DELETE FROM Orders 
WHERE OrderDate < '2023-01-01';

-- Desfaz a exclusão
ROLLBACK;
```

Neste exemplo, o comando **ROLLBACK** cancela a exclusão realizada na transação.

---

### SAVEPOINT

O comando **SAVEPOINT** cria um ponto dentro de uma transação ao qual você pode retornar usando o **ROLLBACK**. Ele permite desfazer apenas uma parte da transação sem cancelar tudo.

Exemplo:

```sql
BEGIN TRANSACTION;

UPDATE Accounts 
SET Balance = Balance - 300 
WHERE AccountID = 1;

SAVEPOINT Save1;

UPDATE Accounts 
SET Balance = Balance + 300 
WHERE AccountID = 2;

-- Desfaz apenas a última atualização
ROLLBACK TO Save1;

COMMIT;
```

Neste exemplo, o **ROLLBACK TO Save1** desfaz apenas a segunda atualização, mantendo a primeira alteração.

---

### SET TRANSACTION

O comando **SET TRANSACTION** define as propriedades da transação atual, como o nível de isolamento.

Exemplo:

```sql
SET TRANSACTION ISOLATION LEVEL SERIALIZABLE;

BEGIN TRANSACTION;

SELECT * FROM Products WHERE Stock > 0;

COMMIT;
```

Este comando define o nível de isolamento como **SERIALIZABLE**, o mais restritivo, garantindo que a transação opere em total isolamento.

## Referências

- [📄 W3Schools — SQL Transactions](https://www.w3schools.com/sql/sql_transactions.asp)  
- [📄 Documentação Microsoft — BEGIN TRANSACTION (Transact-SQL)](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/begin-transaction-transact-sql)
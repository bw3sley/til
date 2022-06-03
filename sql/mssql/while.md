# WHILE

O loop **WHILE** em SQL permite executar uma ou mais instruções repetidamente até que a condição especificada se torne falsa.

Esse controle de fluxo é útil para cenários onde é necessário executar operações iterativas, como atualizações em massa ou geração de dados dinâmicos.

---

## Exemplo:

```sql
DECLARE @Counter INT = 0;

BEGIN
    WHILE (@Counter <= 10)
    BEGIN
        PRINT 'Valor do contador = ' + CAST(@Counter AS VARCHAR);
        SET @Counter = @Counter + 1;
    END
END
GO
```

### O que acontece nesse exemplo:

1. Uma variável **@Counter** é declarada e inicializada com o valor **0**.  
2. O loop **WHILE** verifica se **@Counter <= 10**.  
3. Enquanto a condição for verdadeira:  
   - A instrução **PRINT** exibe o valor atual do contador.  
   - O contador é incrementado em **1** a cada iteração usando **SET**.

O resultado final exibirá:

```
Valor do contador = 0  
Valor do contador = 1  
...  
Valor do contador = 10  
```

---

## Observações

- **BREAK**: Use o comando **BREAK** para sair do loop antecipadamente com base em uma condição.  
- **CONTINUE**: Use o comando **CONTINUE** para pular o restante do código no loop atual e iniciar a próxima iteração.

### Exemplo com **BREAK** e **CONTINUE**:

```sql
DECLARE @Counter INT = 0;

WHILE (@Counter <= 10)
BEGIN
    SET @Counter = @Counter + 1;

    IF @Counter = 5
        CONTINUE; -- Pula o número 5

    IF @Counter = 8
        BREAK; -- Sai do loop ao atingir 8

    PRINT 'Contador = ' + CAST(@Counter AS VARCHAR);
END
```

Resultado:

```
Contador = 1  
Contador = 2  
Contador = 3  
Contador = 4  
Contador = 6  
Contador = 7  
```

---

## Referências

- [📄 W3Schools — SQL WHILE Loop](https://www.w3schools.com/sql/sql_while_loop.asp)  
- [📄 Documentação Microsoft — WHILE (Transact-SQL)](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/while-transact-sql)
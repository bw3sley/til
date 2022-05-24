# IF - ELSE

A declaração **IF...ELSE** é uma instrução de controle de fluxo que permite executar ou ignorar um bloco de comandos com base em uma condição especificada.

Exemplo:

```sql
IF (@Numero > 5)
BEGIN
    PRINT 'Tudo certo!'
END
ELSE
BEGIN
    PRINT 'Deu ruim'
END
```

Nesta sintaxe, se a **expressão booleana** for avaliada como **TRUE**, o bloco de comandos dentro de **BEGIN...END** será executado. Caso contrário, o bloco será ignorado e o controle do programa será passado para a próxima instrução após o **END**.
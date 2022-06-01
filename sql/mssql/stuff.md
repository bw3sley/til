# STUFF

A função **`STUFF()`** exclui uma parte de uma string e insere outra parte no lugar, começando em uma posição especificada.

💡 **Dica:** Veja também a função [`REPLACE()`](https://www.w3schools.com/sql/func_sqlserver_replace.asp).

Exemplo:

```sql
SELECT STUFF('SQL Tutorial', 1, 3, 'TypeScript'); -- Resultado: TypeScript Tutorial
```

Neste exemplo:

- `'SQL Tutorial'` é a string original.  
- `1` é a posição inicial onde a substituição começa.  
- `3` é o número de caracteres a serem removidos.  
- `'TypeScript'` é a nova string inserida.

---

## Referências

- [📄 Documentação Microsoft — STUFF (Transact-SQL)](https://learn.microsoft.com/en-us/sql/t-sql/functions/stuff-transact-sql)
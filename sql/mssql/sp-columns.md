# SP_COLUMNS

No **SQL Server**, você pode usar procedimentos armazenados do sistema para obter informações detalhadas sobre tabelas e colunas.

</br>

## SP_COLUMNS

O procedimento armazenado **sp_columns** retorna informações sobre as colunas de um objeto especificado no ambiente atual, como tabelas, views ou funções com valor de tabela.

Exemplo:

```sql
SP_COLUMNS Customer;
```

Esse comando retorna detalhes como o nome das colunas, tipo de dado, tamanho e se a coluna permite valores nulos.

## Referências

- [📄 Documentação Microsoft — sp_columns (Transact-SQL)](https://learn.microsoft.com/en-us/sql/relational-databases/system-stored-procedures/sp-columns-transact-sql)  
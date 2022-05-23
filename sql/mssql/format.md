# FORMAT

A função `FORMAT()` é usada para formatar um valor de acordo com o padrão especificado. Ela é útil para aplicar máscaras em números, datas e outros tipos de dados.

Exemplo:

```sql
SELECT FORMAT(123456789, '##-##-#####');
```

**Resultado:**  
`12-34-56789`

### Aplicações comuns do `FORMAT()`:

- Formatar números com separadores personalizados.  
- Exibir datas em diferentes formatos regionais.  
- Adicionar máscaras a dados como CPF, CNPJ ou números de telefone.

## Referências

- [📄 Documentação Microsoft — FORMAT (Transact-SQL)](https://learn.microsoft.com/en-us/sql/t-sql/functions/format-transact-sql)
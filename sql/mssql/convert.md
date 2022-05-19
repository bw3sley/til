# CONVERT

A função **CONVERT()** converte um valor (de qualquer tipo) para um tipo de dado especificado. Ela funciona de forma semelhante à função [CAST()](./cast.md).

Exemplo:

```sql
SELECT 
    CONVERT(varchar, Information.Date, 110)
FROM Information;
```

## Convertendo datetime para string

| Com século  | Entrada/Saída                | Padrão                |
| :---------: | :--------------------------: | :------------------: |
| 100         | mon dd yyyy hh:miAM/PM       | Padrão (Default)     |
| 101         | mm/dd/yyyy                   | EUA                  |
| 102         | yyyy.mm.dd                   | ANSI                 |
| 105         | dd-mm-yyyy                   | Italiano/Brasileiro  |
| 110         | mm-dd-yyyy                   | EUA                  |

## Referências

- [📄 W3Schools — SQL CONVERT() Function](https://www.w3schools.com/sql/func_sqlserver_convert.asp)
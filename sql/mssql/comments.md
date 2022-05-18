# Comentários em SQL

Assim como em outras linguagens de programação, os comentários também são importantes em SQL. Eles ajudam a documentar o código e evitam que certas linhas sejam executadas.

</br>

## Comentários de linha única

Comentários que começam e terminam na mesma linha são considerados comentários de linha única. Linhas iniciadas com `--` são tratadas como comentários e não serão executadas.

Exemplo:

```sql
-- comentário de linha única
-- outro comentário
```

## Comentários de múltiplas linhas

Comentários que começam em uma linha e terminam em outra são considerados comentários de múltiplas linhas. Eles iniciam com `/*` e terminam com `*/`.

Exemplo:

```sql
/* comentário de múltiplas linhas
continuação do comentário */
```

## Comentários embutidos em linhas

Os comentários embutidos podem ser inseridos entre comandos SQL e são delimitados por `/*` e `*/`.

Exemplo:

```sql
SELECT * FROM /* tabela de clientes */ Customers;

SELECT * FROM -- tabela de clientes
Customers;
```

## Referências

- [📄 W3Schools — SQL Comments](https://www.w3schools.com/sql/sql_comments.asp)
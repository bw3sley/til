# STRING_AGG

A função **STRING_AGG()** concatena valores de uma coluna em uma única string, separados por um delimitador especificado.

É frequentemente usada para combinar valores de várias linhas em um único resultado agrupado.

## Sintaxe

```sql
STRING_AGG ( expression, separator )  
[ <order_clause> ]
```

- **expression**: A coluna ou valor que será concatenado.  
- **separator**: O delimitador usado para separar os valores concatenados.  
- **<order_clause>** *(opcional)*: Permite ordenar os valores antes da concatenação usando `WITHIN GROUP (ORDER BY column)`.

## Exemplo Básico

Concatenando nomes separados por vírgula:

```sql
SELECT 
    STRING_AGG(Name, ', ') AS NomesConcatenados
FROM Employees;
```

**Resultado:**  
`João, Maria, Pedro, Ana`

## Exemplo com Ordenação

Concatenando nomes em ordem alfabética:

```sql
SELECT 
    STRING_AGG(Name, ', ') WITHIN GROUP (ORDER BY Name ASC) AS NomesOrdenados
FROM Employees;
```

**Resultado:**  
`Ana, João, Maria, Pedro`

## Agrupando por outra coluna

Concatenando nomes por departamento:

```sql
SELECT 
    Department,
    STRING_AGG(Name, ' | ') AS NomesPorDepartamento
FROM Employees
GROUP BY Department;
```

**Resultado:**

| Department  | NomesPorDepartamento        |
|-------------|-----------------------------|
| Vendas      | João | Maria                |
| TI          | Pedro | Ana                 |

## Referências

- [📄 Documentação Microsoft — STRING_AGG (Transact-SQL)](https://learn.microsoft.com/en-us/sql/t-sql/functions/string-agg-transact-sql)
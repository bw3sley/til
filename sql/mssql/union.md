# UNION

O operador **UNION** é usado para combinar o conjunto de resultados de duas ou mais instruções **SELECT**.

### Regras do **UNION**:

- Cada instrução **SELECT** dentro do **UNION** deve ter o mesmo número de colunas.  
- As colunas devem ter tipos de dados semelhantes.  
- As colunas em todas as instruções **SELECT** devem estar na mesma ordem.  
- O **UNION** retorna apenas valores distintos (remove duplicados).  
- Use **UNION ALL** para incluir valores duplicados.

---

## Exemplo:

```sql
SELECT 
    City, 
    Country 
FROM Customers
WHERE Country = 'Germany'

UNION

SELECT 
    City, 
    Country 
FROM Suppliers
WHERE Country = 'Germany'

ORDER BY 
    City;
```

Neste exemplo, os resultados de **Customers** e **Suppliers** onde o país é **Germany** são combinados em um único conjunto, sem valores duplicados por padrão.

---

### **UNION ALL** (Incluindo duplicados)

```sql
SELECT 
    City, 
    Country 
FROM Customers
WHERE Country = 'Germany'

UNION ALL

SELECT 
    City, 
    Country 
FROM Suppliers
WHERE Country = 'Germany'

ORDER BY 
    City;
```

Aqui, o **UNION ALL** retornará todos os resultados, incluindo valores duplicados.

---

## Referências

- [📄 W3Schools — SQL UNION Operator](https://www.w3schools.com/sql/sql_union.asp)  
- [📄 Documentação Microsoft — UNION (Transact-SQL)](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/set-operators-union-transact-sql)
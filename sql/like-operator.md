# LIKE

O comando **LIKE** é usado em uma cláusula **WHERE** para buscar um padrão específico em uma coluna.

Você pode usar dois curingas com o **LIKE**:

- `%` — Representa zero, um ou vários caracteres.  
- `_` — Representa um único caractere (*no MS Access usa-se o ponto de interrogação `?`*).

</br>

## Curinga `%`

### Começa com

Seleciona todos os registros que começam com o padrão especificado (`algo%`).

Exemplo:

```sql
SELECT 
    * 
FROM Customer 
WHERE Customer_Name LIKE 'w3sLeYY%';
```

---

### Termina com

Seleciona todos os registros que terminam com o padrão especificado (`%algo`).

Exemplo:

```sql
SELECT 
    * 
FROM Customer 
WHERE Customer_Name LIKE '%w3sLeYY';
```

---

### Contém

Seleciona todos os registros que contêm o padrão especificado (`%algo%`).

Exemplo:

```sql
SELECT 
    * 
FROM Customer 
WHERE Customer_Name LIKE '%w3sLeYY%';
```

---

### Começa e termina com

Seleciona todos os registros que começam e terminam com um padrão específico (`s%g`).

Exemplo:

```sql
SELECT 
    * 
FROM Customer 
WHERE Customer_Name LIKE 'w%y';
```

</br>

## Curinga `_`

### Tamanho

Seleciona todos os registros que começam com a letra "a" e têm pelo menos 3 caracteres.

Exemplo:

```sql
SELECT 
    * 
FROM Customers
WHERE Customer_Name LIKE 'a__%';
```

---

## Referências

- [📄 W3Schools — SQL LIKE Operator](https://www.w3schools.com/sql/sql_like.asp)
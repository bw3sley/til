# JOINS

A cláusula **JOIN** é usada para combinar linhas de duas ou mais tabelas, com base em uma coluna relacionada entre elas.

</br>

## Diferentes Tipos de JOINS

### INNER JOIN

Retorna os registros que possuem correspondência em ambas as tabelas.

Exemplo:

```sql
SELECT 
    Orders.OrderID, 
    Customers.CustomerName
FROM Orders
INNER JOIN Customers 
    ON Orders.CustomerID = Customers.CustomerID;
```

O **INNER JOIN** seleciona todas as linhas das duas tabelas, desde que haja correspondência entre as colunas. Se existirem registros na tabela "Orders" que não possuem correspondência em "Customers", esses registros não serão exibidos.

---

### LEFT JOIN

Retorna todos os registros da tabela da esquerda e os registros correspondentes da tabela da direita.

Exemplo:

```sql
SELECT 
    Customers.CustomerName, 
    Orders.OrderID
FROM Customers
LEFT JOIN Orders 
    ON Customers.CustomerID = Orders.CustomerID
ORDER BY 
    Customers.CustomerName;
```

O **LEFT JOIN** retorna todos os registros da tabela à esquerda (Customers) e os registros correspondentes da tabela à direita (Orders). Se não houver correspondência, os campos da tabela da direita serão nulos.

---

### RIGHT JOIN

Retorna todos os registros da tabela da direita e os registros correspondentes da tabela da esquerda.

Exemplo:

```sql
SELECT 
    Orders.OrderID, 
    Employees.LastName, 
    Employees.FirstName
FROM Orders
RIGHT JOIN Employees 
    ON Orders.EmployeeID = Employees.EmployeeID
ORDER BY 
    Orders.OrderID;
```

O **RIGHT JOIN** retorna todos os registros da tabela à direita (Employees) e os registros correspondentes da tabela à esquerda (Orders). Se não houver correspondência, os campos da tabela da esquerda serão nulos.

---

### FULL OUTER JOIN

Retorna todos os registros quando há correspondência em qualquer uma das tabelas (esquerda ou direita).

Exemplo:

```sql
SELECT 
    Customers.CustomerName, 
    Orders.OrderID
FROM Customers
FULL OUTER JOIN Orders 
    ON Customers.CustomerID = Orders.CustomerID
ORDER BY 
    Customers.CustomerName;
```

O **FULL OUTER JOIN** retorna todos os registros das tabelas esquerda e direita, combinando-os quando há correspondência. Caso contrário, retorna valores nulos para as colunas da tabela sem correspondência.

---

### SELF JOIN

O **SELF JOIN** é um tipo de JOIN em que uma tabela é unida a ela mesma.

Exemplo:

```sql
SELECT 
    CustomerA.CustomerName AS CustomerNameA, 
    CustomerB.CustomerName AS CustomerNameB, 
    CustomerA.City
FROM Customers CustomerA, Customers CustomerB
WHERE CustomerA.CustomerID <> CustomerB.CustomerID
    AND CustomerA.City = CustomerB.City
ORDER BY 
    CustomerA.City;
```

Neste exemplo, estamos comparando clientes da mesma cidade, mas com IDs diferentes.

---

## Referências

- [📄 W3Schools — SQL Joins](https://www.w3schools.com/sql/sql_join.asp)
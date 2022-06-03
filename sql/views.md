# Views

Em **SQL**, uma **view** é uma tabela virtual baseada no conjunto de resultados de uma instrução **SELECT**.

Uma **view** contém linhas e colunas, assim como uma tabela real. Os campos em uma **view** vêm de uma ou mais tabelas reais do banco de dados.

Você pode adicionar instruções SQL e funções em uma **view** e apresentar os dados como se estivessem vindo de uma única tabela.

---

### **Regras para Manipulação de Dados em Views**:

- Você **não pode** realizar operações de **INSERT** ou **DELETE** em uma **view** que contenha um **JOIN**. Apenas **UPDATE** é permitido.  
- Você **pode** realizar **INSERT**, **DELETE** e **UPDATE** em uma **view** que **não contém JOIN**.

---

## Criando uma View

Exemplo:

```sql
CREATE VIEW Report AS
    SELECT 
        Customer.Name,
        Customer.Gender,
        Customer.Email,
        Address.City,
        Address.UF
    FROM Customer
    LEFT JOIN Address
        ON Customer.Customer_Id = Address.FK_Customer_Id
    WHERE Customer.Email IS NOT NULL;
```

Essa **view** chamada **Report** exibe informações dos clientes e seus respectivos endereços, filtrando apenas aqueles com e-mail cadastrado.

---

## Consultando uma View

Exemplo:

```sql
SELECT * FROM Report;
```

Aqui, você consulta os dados da **view** da mesma forma que faria com uma tabela normal.

---

## Deletando uma View

Exemplo:

```sql
DROP VIEW Report;
```

Esse comando remove a **view** do banco de dados.

---

## Referências

- [📄 W3Schools — SQL Views](https://www.w3schools.com/sql/sql_view.asp)  
- [📄 Documentação Microsoft — CREATE VIEW (Transact-SQL)](https://learn.microsoft.com/en-us/sql/t-sql/statements/create-view-transact-sql)
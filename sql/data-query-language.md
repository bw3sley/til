Aqui está o TIL sobre **DQL - Data Query Language** traduzido para o português, seguindo o padrão atual:

---

# DQL - Linguagem de Consulta de Dados

Os comandos **DQL** (*Data Query Language*) são usados para realizar consultas nos dados presentes em objetos do esquema do banco de dados. O objetivo principal do comando DQL é obter informações com base nas consultas realizadas, permitindo extrair, filtrar e organizar dados conforme a necessidade.

Em termos simples, o DQL é a parte do SQL responsável por recuperar dados do banco e aplicar ordenações ou filtros sobre eles.

## SELECT

Como o próprio nome sugere, o comando **SELECT** é usado para selecionar dados de uma ou mais tabelas do banco de dados.

Exemplo:

```sql
SELECT 
    User.Name, 
    User.Email, 
    User.Gender -- (PROJEÇÃO)

FROM User -- (ORIGEM)

INNER JOIN Address -- (JUNÇÃO)
    ON User.Id = Address.Id_User

WHERE User.Id = 1 -- (SELEÇÃO);
```

### Componentes do exemplo:

- **PROJEÇÃO**: Define as colunas que serão retornadas (`User.Name`, `User.Email`, `User.Gender`).
- **ORIGEM**: Especifica a tabela principal da consulta (`User`).
- **JUNÇÃO (JOIN)**: Conecta a tabela principal a outras tabelas relacionadas (`INNER JOIN Address`).
- **SELEÇÃO**: Filtra os registros de acordo com condições específicas (`WHERE User.Id = 1`).

## Referências

- [📄 W3Schools — SQL SELECT Statement](https://www.w3schools.com/sql/sql_select.asp)
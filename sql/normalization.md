# Normalização

A **normalização** é uma técnica de design de banco de dados que reduz a redundância de dados e elimina características indesejáveis, como anomalias de inserção, atualização e exclusão. As regras de normalização dividem tabelas grandes em tabelas menores e as conectam por meio de relacionamentos. O objetivo da normalização em SQL é eliminar dados redundantes e garantir que as informações sejam armazenadas de forma lógica.

</br>

## Primeira Forma Normal (1FN)

- Cada célula da tabela deve conter apenas um único valor.  
- Cada registro deve ser único.

</br>

## Segunda Forma Normal (2FN)

- Deve estar em 1FN.  
- Possuir uma chave primária de coluna única que não dependa funcionalmente de nenhum subconjunto da chave candidata.

</br>

## Terceira Forma Normal (3FN)

- Deve estar em 2FN.  
- Não deve conter dependências funcionais transitivas.

</br>

Existem outras formas normais que não serão abordadas neste post, mas sinta-se à vontade para conferir mais detalhes em: [O que é Normalização em DBMS](https://www.guru99.com/database-normalization.html)
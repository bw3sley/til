# Usar `git pull --rebase` em vez de `git pull`

O comando `git pull --rebase` é uma alternativa ao `git pull` convencional. Ele garante que seu histórico de commits fique linear, evitando commits extras de merge ao integrar mudanças do repositório remoto.

Para atualizar seu branch local aplicando um rebase em vez de um merge:

```sh
git pull --rebase origin main
```

Isso traz as alterações do repositório remoto e as reaplica sobre seus commits locais, mantendo um histórico mais limpo.

Se houver conflitos durante o rebase, é possível abortar a operação com:

```sh
git rebase --abort
```

Isso reverte seu repositório ao estado antes do rebase, evitando a necessidade de um `git pull` adicional.
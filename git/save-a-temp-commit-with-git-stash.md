# Salvando arquivos temporariamente

O comando `git stash` permite salvar temporariamente alterações em seu repositório sem precisar fazer um commit. Isso é útil quando você precisa trocar de branch ou testar algo sem perder o que já foi modificado.

## Como Funciona?

Quando você executa:

```bash
git stash
```

O Git remove as mudanças não commitadas do seu diretório de trabalho e as salva em uma pilha de mudanças temporárias.

### Principais Comandos do git stash

**1. Guardar as mudanças**

```bash
git stash
```

Armazena todas as mudanças não commitadas.

**2. Guardar apenas arquivos modificados, sem os arquivos novos**

```bash
git stash -u
```

Ignora arquivos não rastreados (untracked).

**3. Aplicar a última mudança armazenada**

```bash
git stash apply
```

Restaura as mudanças do stash mais recente sem removê-las da pilha.

**4. Aplicar e remover a última mudança armazenada**

```bash
git stash pop
```

Restaura as mudanças do stash mais recente e remove esse stash da pilha.

**5. Listar stashes salvos**

```bash
git stash list
```

Mostra todas as mudanças salvas no stash.

**6. Aplicar um stash específico**

```bash
git stash apply stash@{n}
```

Onde n é o índice do stash na lista.

**7. Remover um stash específico**

```bash
git stash drop stash@{n}
```

**8. Remover todos os stashes**

```bash
git stash clear
```

Cuidado! Isso apagará todas as mudanças armazenadas no stash.
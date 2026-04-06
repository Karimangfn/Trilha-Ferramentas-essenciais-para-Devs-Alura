# Manipulação de Versões no Git: `git stash` e `git restore`

## Interrompendo e Retomando Trabalho com `git stash`

* Criação de novo branch: `git switch -c`.
* Estado inválido: código em implementação pode não estar pronto para commit.
* `git stash`: Guarda alterações temporariamente.
* `git stash pop`: Aplica alterações armazenadas e remove da pilha.
* `git stash drop`: Remove alterações da pilha.
* `git stash apply`: Aplica alterações armazenadas, mantendo na pilha.
* `git stash list`: Visualiza alterações guardadas.
* `git stash clear`: Remove todas as stashes.
* `git stash push -m "mensagem"`: Adiciona mensagem descritiva ao stash.
* Stash funciona como uma pilha (LIFO).

## Desfazendo Alterações com `git restore`

* `git restore`: Restaura arquivos para o último commit (como "Ctrl + Z").
* `git restore .`: Restaura todos os arquivos no diretório atual.
* Alternativa a `git checkout`.
* Permite restaurar arquivos para estado de commit anterior.

## Manipulando Versões e "Staging Area" com `git restore`

* Introdução ao conceito de "staging area".
* `git restore --staged <arquivo>`: Remove arquivo da staging area.
* `git restore <arquivo>`: Desfaz alterações no arquivo.
* `git restore --source=<hash> <arquivo>`: Restaura arquivo para estado de commit anterior.
* `git status`: Informa sobre "working tree" e "staging area".
* Preparação para gerenciar versões e criar releases.
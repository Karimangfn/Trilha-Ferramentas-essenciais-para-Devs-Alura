# Gerenciamento de Commits e Comandos Específicos do Git

## `git cherry-pick`: Compartilhando Commits Entre Branches

* Cenário: duas branches (`funcionalidade1` e `funcionalidade2`) dependem da mesma alteração.
* `git cherry-pick`: Aplica um commit específico de uma branch na branch atual.
* Processo:
    * Criar e alternar entre branches.
    * Fazer commits em uma branch.
    * `git log`: Visualizar commits de outra branch e copiar o hash.
    * `git cherry-pick <hash>`: Aplicar o commit na branch atual.
* `git push`: Enviar branches para o repositório remoto.
* Merge das branches na branch `main`.

## `git blame`: Identificando Autores de Alterações

* `git blame`: Mostra autor, data e hash do commit responsável por cada linha do arquivo.
* Ajuda a entender o histórico de modificações e consultar desenvolvedores.

## Revisão Geral do Git

* Visualização de Commits:
    * `git log`: Histórico de commits.
    * `git log --graph`: Visualização gráfica.
    * `git log -p`: Detalhes das alterações.
    * `git log --oneline`: Visualização compacta.
* Branches:
    * `git branch`: Criar e listar branches.
    * `git switch`: Alternar entre branches.
    * `git merge`: Unir branches.
    * `git rebase`: Reescrever histórico.
* Manipulação de Alterações:
    * `git stash`: Guardar alterações temporariamente.
    * `git restore`: Desfazer alterações.
    * `HEAD`: Ponteiro para o último commit.
    * Staging area: Área de preparação para commits.
    * Working tree: Diretório de trabalho.
* Tags e Releases:
    * Tags: Marcar versões do projeto.
    * Annotated tags: Tags com informações adicionais.
    * Releases: Versões publicadas no GitHub.
* Comandos Específicos:
    * `git cherry-pick`: Aplicar commits específicos.
    * `git blame`: Identificar autores de alterações.
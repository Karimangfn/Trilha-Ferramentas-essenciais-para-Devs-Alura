# Colaboração, Branches, Merge e Rebase no Git

## Colaboração em Projetos e Conflitos

* Importância de usar o usuário correto ao realizar `push`.
* Simulação de conflitos ao trabalhar no mesmo arquivo (`index.html`).
* Necessidade de `git pull` para integrar alterações remotas e realizar merge.
* Complexidade de gerenciar alterações em projetos grandes com múltiplos colaboradores.
* Introdução ao uso de branches para evitar problemas organizacionais.

## Organização com Branches

* Importância de não realizar commits diretamente na branch principal (`main`).
* Apresentação do site Visualizing Git para entender o funcionamento do Git (https://git-school.github.io/visualizing-git/).
* Comandos para gerenciamento de branches:
    * `git branch`: Lista branches existentes. Também pode ser usado para criar (`git branch nome-da-branch`), renomear (`git branch -m nome-antigo nome-novo`) e excluir branches (`git branch -d nome-da-branch` para excluir localmente e `git branch -D` para forçar a exclusão).
    * `git push origin --delete nome-da-branch`: Remove uma branch remota.
    * `git branch -d :minhabranch`: Remove uma branch remota.
    * `git checkout -b nome-da-branch`: Cria uma nova branch e já muda para ela.
    * `git switch -c nome-da-branch`: Cria uma nova branch e já muda para ela.
    * `git checkout` ou `git switch`: Alterna entre branches existentes.
* Criação de branches para funcionalidades específicas, evitando alterações diretas na branch principal.
* Preparação para a união de branches, utilizando `git merge` ou `git rebase`, conforme necessário.

## União de Branches com `git merge`

* Revisão da criação e alternância entre branches.
* Uso de pull requests no GitHub.
* `git merge`: Mescla alterações de uma branch em outra.
* Conceito de fast forward: avanço da branch principal sem novo commit.
* Merge commit: criação de um commit ao mesclar branches com evoluções independentes.

## Atualização de Branches com `git rebase`

* Criação de branch `nova-funcionalidade` a partir de `main`.
* `git rebase main`: Atualiza a branch `nova-funcionalidade` com os commits mais recentes de `main`.
* Diferença entre `merge` e `rebase`.
* Vantagens do rebase: integração de funcionalidades e histórico linear.
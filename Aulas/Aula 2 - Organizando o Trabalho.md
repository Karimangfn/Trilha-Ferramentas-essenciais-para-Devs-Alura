# Colaboração, Branches, Merge e Rebase no Git

## Colaboração em Projetos e Conflitos

* Importância de usar o usuário correto ao realizar `push`.
* Simulação de conflitos ao trabalhar no mesmo arquivo (`index.html`).
* Necessidade de `git pull` para integrar alterações remotas e realizar merge.
* Complexidade de gerenciar alterações em projetos grandes com múltiplos colaboradores.
* Introdução ao uso de branches para evitar problemas organizacionais.

## Organização com Branches

* Importância de não realizar commits diretamente na branch principal (`main`).
* Apresentação do site Visualizing Git para entender o funcionamento do Git.
* Comandos para gerenciamento de branches:
    * `git branch`: Cria, lista, renomeia e remove branches.
    * `git checkout` ou `git switch`: Alterna entre branches.
* Criação de branches para funcionalidades específicas.
* Preparação para a união de branches.

## União de Branches com `git merge`

* Revisão da criação e alternância entre branches.
* Uso de pull requests no GitHub.
* `git merge`: Mescla alterações de uma branch em outra.
* Conceito de fast forward: avanço da branch principal sem novo commit.
* Merge commit: criação de um commit ao mesclar branches com evoluções independentes.
* Remoção de branches desnecessárias.
* Importância de entender estratégias de mesclagem.

## Atualização de Branches com `git rebase`

* Revisão do conceito de branches e desenvolvimento paralelo.
* Criação de branch `nova-funcionalidade` a partir de `main`.
* `git rebase main`: Atualiza a branch `nova-funcionalidade` com os commits mais recentes de `main`.
* Diferença entre `merge` e `rebase`.
* Vantagens do rebase: integração de funcionalidades e histórico linear.
* Importância de conhecer políticas de merge da empresa.
* Preparação para trabalhar eficientemente com branches atualizadas.
# Tags e Releases no Git e GitHub

## Criando Tags

* Tags funcionam como checkpoints para marcar estados específicos do código.
* `git tag nome_da_tag`: Cria uma tag que aponta para o commit atual.
* Tags apontam para o mesmo commit, mesmo com novos commits adicionados.
* Criação de tags para commits específicos usando o hash do commit.
* `git tag`: Visualiza as tags criadas.
* Envio de tags para o repositório remoto no GitHub.
* Tags podem ser usadas para disponibilizar versões do projeto para download.

## Annotated Tags

* Tags são ponteiros para commits.
* Annotated tags possuem informações adicionais (mensagens, autor).
* `git tag -d nome_da_tag`: Apaga uma tag existente.
* `git tag -a nome_da_tag -m "mensagem da tag"`: Cria uma annotated tag.
* `git push origin nome_da_tag`: Envia a tag para o repositório remoto.
* GitHub exibe informações de annotated tags (mensagem, autor).
* Tags com mensagens são automaticamente consideradas annotated tags.

## Tags e Releases

* Annotated tags: contêm informações adicionais (commit, autor, mensagens).
* `git tag -v nome_da_tag`: Verifica informações de uma annotated tag.
* Unannotated tags: apelidos para commits, sem informações adicionais.
* Releases: disponibilizam versões do projeto (documentos, changelogs, binários).
* Criação de releases: escolha de tag, título, notas de lançamento, arquivos adicionais.
* Releases documentam e compartilham novas versões no GitHub.
* Releases podem ser criadas manualmente ou via GitHub Actions.
# Análise de Mudanças no Git

## Introdução:
    * O curso "Git e GitHub: dominando controle de versão de código" foca em visualizar alterações, trabalhar com branches, manipular alterações e usar tags.
    * Destinado a quem já tem familiaridade com Git.

## Analisando Commits com `git log`:
    * Permite visualizar o histórico de commits, facilitando o acompanhamento das mudanças no projeto (Apertar a tecla "q" para sair dos logs).
    * `git log`: Visualiza o histórico de commits (hash, autor, data, mensagem).
    * `git log --oneline`: Visualização compacta (hash reduzido e mensagem).
    * `git log -p`: Detalhes das alterações (diff).
    * `git log --graph`: Visualização gráfica do histórico.
    * `git log --pretty`: Personalização da exibição.
    * `git log --format`: Personalização da exibição, permitindo o uso de especificadores como `%H` (hash completo), `%h` (hash reduzido), `%an` (autor), `%ad` (data), entre outros.
    * `git log --help`: Informações sobre opções disponíveis.

## Analisando Detalhes de Commits com `git show`:
    * Exibe detalhes específicos de um commit, útil para entender as alterações introduzidas.
    * `git show {hash do commit}`: Detalhes do commit (autor, data, mensagem, diff).
    * `git show`: Mostra o último commit (HEAD) por padrão.
    * `git show --help`: Informações sobre opções disponíveis.
    * HEAD: Ponteiro para o último commit da branch atual.

## Analisando Mudanças com `git status` e `git diff`:
    * Permitem verificar o estado atual do repositório e as diferenças entre as versões dos arquivos.
    * `git status`: Verifica a ramificação e alterações não commitadas (mostra mudanças não staged).
    * `git diff`: Visualiza diferenças entre o estado atual e o último commit.
    * `git diff <commit1>..<commit2>`: Compara diferenças entre dois commits (se eu colocar apenas 1 commit, ele será comparado com o HEAD).
    * `git add`: Adiciona arquivo ao stage.
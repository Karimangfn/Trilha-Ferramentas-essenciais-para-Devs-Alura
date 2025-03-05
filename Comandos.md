## Comandos Git Essenciais

### Informações e Histórico

* `git log` – Visualiza o histórico de commits.
    * Exemplo: `git log`
* `git log --oneline` – Visualização compacta dos commits.
    * Exemplo: `git log --oneline`
* `git log -p` – Exibe detalhes das alterações (diff) em cada commit.
    * Exemplo: `git log -p`
* `git log --graph` – Visualização gráfica do histórico de commits.
    * Exemplo: `git log --graph`
* `git log --pretty` ou `git log --format` – Personaliza a exibição dos commits.
    * Exemplo: `git log --pretty=format:"%h %s"`
* `git log --help` – Exibe informações sobre opções disponíveis do `git log`.
    * Exemplo: `git log --help`
* `git show {hash do commit}` – Detalhes de um commit específico.
    * Exemplo: `git show a1b2c3d4`
* `git blame <arquivo>` – Mostra autor, data e hash do commit responsável por cada linha do arquivo.
    * Exemplo: `git blame arquivo.txt`

### Branches

* `git branch` – Cria, lista, renomeia e remove branches.
    * Exemplo: `git branch nova-branch`
* `git branch -d <nome>` - Deleta um branch local.
    * Exemplo: `git branch -d nova-branch`
* `git checkout <nome>` – Muda para uma branch existente.
    * Exemplo: `git checkout nova-branch`
* `git switch <nome>` – Alterna entre branches (alternativa moderna ao checkout).
    * Exemplo: `git switch nova-branch`
* `git switch -c <nome>` – Cria e muda para uma nova branch.
    * Exemplo: `git switch -c nova-branch`
* `git merge <nome>` – Mescla alterações de uma branch em outra.
    * Exemplo: `git merge nova-branch`
* `git rebase main` – Atualiza a branch atual com os commits mais recentes de main.
    * Exemplo: `git rebase main`

### Staging e Commits

* `git status` – Verifica a ramificação e alterações não commitadas.
    * Exemplo: `git status`
* `git diff` – Visualiza diferenças entre o estado atual e o último commit.
    * Exemplo: `git diff`
* `git diff <commit1>..<commit2>` – Compara diferenças entre dois commits.
    * Exemplo: `git diff a1b2c3d4..e5f6g7h8`
* `git add <arquivo>` – Adiciona arquivo ao stage.
    * Exemplo: `git add arquivo.txt`
* `git add .` - Adiciona todas as alterações no diretório atual para a área de staging.
    * Exemplo: `git add .`
* `git commit -m "mensagem"` – Cria um novo commit com a mensagem especificada.
    * Exemplo: `git commit -m "Adiciona nova funcionalidade"`
* `git commit --amend` - Permite modificar o último commit.

### Desfazendo Alterações

* `git restore <arquivo>` – Restaura arquivos para o último commit.
    * Exemplo: `git restore arquivo.txt`
* `git restore .` – Restaura todos os arquivos no diretório atual.
    * Exemplo: `git restore .`
* `git restore --staged <arquivo>` – Remove arquivo da staging area.
    * Exemplo: `git restore --staged arquivo.txt`
* `git restore --source=<hash> <arquivo>` – Restaura arquivo para estado de commit anterior.
    * Exemplo: `git restore --source=a1b2c3d4 arquivo.txt`
* `git reset --hard <commit>` - Reseta o repositório para um commit anterior, perdendo todas as alterações posteriores.
    * Exemplo: `git reset --hard HEAD~2`

### Stash

* `git stash` – Guarda alterações temporariamente.
    * Exemplo: `git stash`
* `git stash pop` – Aplica alterações armazenadas e remove da pilha.
    * Exemplo: `git stash pop`
* `git stash apply` – Aplica alterações armazenadas, mantendo na pilha.
    * Exemplo: `git stash apply`
* `git stash list` – Visualiza alterações guardadas.
    * Exemplo: `git stash list`
* `git stash clear` – Remove todas as stashes.
    * Exemplo: `git stash clear`
* `git stash push -m "mensagem"` – Adiciona mensagem descritiva ao stash.
    * Exemplo: `git stash push -m "alterações temporárias"`

### Tags e Releases

* `git tag nome_da_tag` – Cria uma tag que aponta para o commit atual.
    * Exemplo: `git tag v1.0.0`
* `git tag` – Visualiza as tags criadas.
    * Exemplo: `git tag`
* `git tag -d nome_da_tag` – Apaga uma tag existente.
    * Exemplo: `git tag -d v1.0.0`
* `git tag -a nome_da_tag -m "mensagem da tag"` – Cria uma annotated tag.
    * Exemplo: `git tag -a v1.0.0 -m "versão inicial"`
* `git push origin nome_da_tag` – Envia a tag para o repositório remoto.
    * Exemplo: `git push origin v1.0.0`
* `git tag -v nome_da_tag` – Verifica informações de uma annotated tag.
    * Exemplo: `git tag -v v1.0.0`

### Comandos Específicos

* `git cherry-pick <hash>` – Aplica um commit específico de uma branch na branch atual.
    * Exemplo: `git cherry-pick a1b2c3d4`

### Remoto

* `git remote add origin <url>` - Adiciona um repositório remoto.
    * Exemplo: `git remote add origin https://github.com/usuario/repositorio.git`
* `git push origin <branch>` - Envia commits para um repositório remoto.
    * Exemplo: `git push origin main`
* `git pull origin <branch>` - Baixa commits de um repositório remoto e mescla com o branch local.
    * Exemplo: `git pull origin main`
* `git clone <url>` - Clona um repositório remoto para a máquina local.
    * Exemplo: `git clone https://github.com/usuario/repositorio.git`
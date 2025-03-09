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
* Diferença entre `merge` e `rebase`:  
  * `merge` cria um commit de junção, preservando o histórico paralelo das branches.  
  * `rebase` reaplica os commits da branch atual sobre a `main`, resultando em um histórico linear.  
* Vantagens do rebase:  
  * Integração de funcionalidades de forma mais limpa.  
  * Histórico linear facilita a leitura e depuração.  
  * Evita commits de merge desnecessários.  

## Exemplo de `git rebase`

### 1. Criando a branch
```bash
git checkout -b nova-funcionalidade main
```
Isso cria e muda para a branch `nova-funcionalidade` baseada na `main`.

### 2. Fazendo commits na branch
```bash
echo "Linha 1" >> arquivo.txt
git add arquivo.txt
git commit -m "Adiciona linha 1"

echo "Linha 2" >> arquivo.txt
git add arquivo.txt
git commit -m "Adiciona linha 2"
```
Agora, temos dois commits na branch `nova-funcionalidade`.

### 3. `main` recebeu novos commits
Enquanto trabalhamos, novos commits foram adicionados à branch `main`:

```
A---B---C  (main atualizado)
 \
  D---E   (nova-funcionalidade)
```

### 4. Fazendo o rebase
Para atualizar `nova-funcionalidade` com as mudanças mais recentes da `main`:

```bash
git checkout nova-funcionalidade
git rebase main
```

Isso reaplica os commits `D` e `E` sobre a `main`, resultando no seguinte histórico:

```
A---B---C---D'---E'  (nova-funcionalidade atualizado)
```

Agora a branch `nova-funcionalidade` tem um histórico linear sem um commit de merge.

### 5. Resolvendo conflitos (se necessário)
Se houver conflitos durante o rebase, Git pausa e exibe mensagens. Para resolver:

1. Edite os arquivos conflitantes.
2. Adicione as mudanças com `git add arquivo.txt`.
3. Continue o rebase com:

```bash
git rebase --continue
```

Se quiser cancelar o rebase:

```bash
git rebase --abort
```

### 6. Finalizando e enviando para o repositório remoto
Após o rebase, precisamos forçar o push porque o histórico foi reescrito:

```bash
git push origin nova-funcionalidade --force
```

⚠️ **Cuidado ao usar `--force`, pois isso pode sobrescrever mudanças no remoto.**

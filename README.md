# Git Katas

## Início Rápido

### Execute na Nuvem
Abra a opção que deja abaixo

[![Open in Cloud Shell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://console.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/cmendesfirmino/git-katas-br.git)

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/cmendesfirmino/git-katas-br.git)

[![Open in Gitpod](https://github.com/codespaces/badge.svg)](https://github.com/cmendesfirmino/git-katas-br/codespaces)

- Vá até o diretório do exercício que deseja resolver
- Execute o script `setup.sh`
- Há uma descrição do exercício no arquivo README.md
```bash
cd basic-commits
. ./setup.sh
```

### Execute Localmente

Com o git instalado em sua máquina local, se não tiver instalado siga esses passos [Configuração Git](configure-git/README.md). 

Em seguida execute os passos abaixo.
- Clone este repositório
- Vá até o diretório do exercício que deseja resolver
- Execute o script `setup.sh`
- Há uma descrição do exercício no arquivo README.md

```bash
git clone https://github.com/cmendesfirmino/git-katas-br.git
cd git-katas-br/basic-commits
. ./setup.sh
```

### Recursos Valiosos

🚀 **Importante configurar o Git antes de iniciar, siga esses passos aqui [Configuração Inicial Git](configure-git/README.md).**

💡 **Entender alguns comandos de shell script podem te ajudar muito também, veja mais sobre eles aqui [Comandos Básicos de Shell](SHELL-BASICS.md).**


## Propósito do Git Katas

Este repositório é uma coleção de exercícios de Git. Ele foi traduzido do repositório original [Git-Katas](https://github.com/eficode-academy/git-katas.git), que foi baseado no trabalho de  [Schauderhaft.de](http://blog.schauderhaft.de/gitkata/).

Traduzi e adaptei esse repositório para utilizar nas aulas que ministro. Portanto, servem para quem deseja praticar conhecimentos de git. Toda contribuição é válida e bem vinda. 

Para verificar o status da tradução de cada item abaixo, consulte aqui [Status Tradução](Status%20Tradução.md)

Os diretórios que iniciam com basic- são os iniciais, importante para quem tem pouco ou nenhum conhecimento. Os demais variam os níveis de dificuldade.

Para obter uma visão geral dos exercícios consulte
[Visão Geral.md](Overview.md).

Sinta-se à vontade para usar esses exercícios, é por isso que eles são públicos!

## Trilha Sugerida

Se você está acessando este repositório em busca de conhecimentos básicos sobre Git, é recomendado seguir os exercícios na ordem a seguir.
Existem mais exercícios do que esses, mas estes devem abranger tudo o que é necessário para usar o Git de forma eficaz no dia a dia.

- [Basic Commits](./basic-commits/README.md)
- [Basic Staging](./basic-staging/README.md)
- [Investigation](./investigation/README.md)
- [Basic Branching](./basic-branching/README.md)
- [Fast Forward Merge](./ff-merge/README.md)
- [3 way Merge](./3-way-merge/README.md)
- [Merge Mergesort](./merge-mergesort/README.md)
- [Rebase Branch](./rebase-branch/README.md)
- [Basic Revert](./basic-revert/README.md)
- [Reset](./reset/README.md)
- [Basic Cleaning](./basic-cleaning/README.md)
- [Amend](./amend/README.md)
- [Reorder the History](./reorder-the-history/README.md)
- [Advanced Rebase Interactive](./advanced-rebase-interactive/README.md)
- [Rebase using autosquash](./rebase-interactive-autosquash/README.md)
- [Basic Stashing](./basic-stashing/README.md)

Veja [Visão Geral.md](Overview.md) para a lista completa.

## Contribuição

Se você sentir falta de exercícios ou encontrar erros em algum deles, sinta-se à vontade para aprimorá-los e fazer uma solicitação de pull.

Você também pode criar uma issue para que possamos perceber uma oportunidade de melhoria!

Obrigado!

## Dicas Úteis

Uma coleção de comandos úteis para serem utilizados ao longo dos exercícios:

```shell
# Inicializando um repositório Git vazio.
git init            # Inicializa um repositório Git vazio no diretório atual.

# Clonando um repositório
git clone https://github.com/praqma-training/git-katas.git      # Clona este repositório para o diretório de trabalho atual

# Configurações Git (nível de usuário e repositório)
git config --local user.name "Nome de Usuário no Nível de Repositório"          # Define um nome de usuário no nível de repositório.
git config --local user.email "Email-de-Usuario@Exemplo.com" # Define um email de usuário no nível de repositório.
                                                            # --global -> Configuração git no nível de usuário armazenada em <user-home>/.gitconfig, por exemplo, ~/.gitconfig
                                                            # --local -> Configuração no nível de repositório armazenada no diretório principal do repositório em .git/config


# Verificar alterações locais
git status                  # Mostra o status da árvore de trabalho
git diff                    # Mostra alterações no diretório de trabalho (ainda não preparadas)
git diff --cached           # Mostra alterações atualmente preparadas para commit

# Adicionar arquivos ao staging (antes de um commit)
git add myfile.txt          # Adiciona myfile.txt ao staging
git add .                   # Adiciona todo o diretório de trabalho ao staging

# Fazer um commit
git commit                              # Cria um novo commit com as alterações na área de staging. Isso abrirá um editor para uma mensagem de commit.
git commit -m "Eu amo documentação"    # Cria um novo commit com uma mensagem de commit a partir da linha de comando
git commit -a                           # Cria um novo commit e "adiciona" automaticamente alterações de todos os arquivos conhecidos
git commit -am "Eu ainda amo!"            # Uma combinação dos anteriores
git commit --amend                      # Refaz a mensagem de commit do commit anterior (não faça isso depois de fazer push!)
                                        #   Nunca alteramos a "história pública"
git reset <file>                        # Desfaz o staging de um arquivo, mantendo-o no diretório de trabalho sem perder alterações.
git reset --soft [commit_hash]          # Reseta o branch atual para <commit>. Não afeta a área de staging ou a árvore de trabalho.
                                        # O modo --hard descartaria todas as alterações.

# Configurar um editor diferente
## Evitar o Vim, mas permanecer no terminal:
- `git config --global core.editor nano`

## Para Windows:
- Usar o Bloco de Notas:
`git config --global core.editor notepad`

- ou, por exemplo, o Notepad++:
`git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`


# Ver histórico
git log             # Mostra os logs de commits
git log --oneline   # Formata os commits em uma única linha (atalho para --pretty=oneline  --abbrev-commit )
git log --graph     # Mostra um gráfico de commits e branches
git log --pretty=fuller     # Para ver detalhes do log de commit com detalhes do autor e committer, se diferentes.
git log --follow <file>     # Lista o histórico de um arquivo além de renomeações
git log branch2..branch1    # Mostra commits alcançáveis a partir de branch1, mas não de branch2

# Armazenamento temporário
git stash                               # Adia (armazena temporariamente) alterações no branch de trabalho e permite fazer checkout para um novo branch
git stash list                          # Lista as stashes armazenadas.
git stash apply <stash>                 # Aplica a <stash> dada, ou se nenhuma for dada, a última da lista de stash.


# Trabalhando com Branches
git branch my-branch       # Cria um novo branch chamado my-branch
git switch my-branch     # Muda para um branch diferente para trabalhar nele
git switch -c my-branch  # Cria um novo branch chamado my-branch E muda para ele
git branch -d my-branch    # Deleta o branch my-branch que foi mesclado com o master
git branch -D my-branch    # Deleta forçadamente um branch my-branch que não foi mesclado com o master

# Mesclando
git merge master         # Mescla o branch master no branch atualmente verificado.
git rebase master        # Rebase no branch atual sobre o branch master

# Trabalhando com Remotos
git remote              # Mostra seus remotos atuais
git remote -v           # Mostra seus remotos atuais e suas URLs
git push                # Publica seus commits no master upstream do branch atualmente verificado
git push -u origin my-branch  # Envia o novo branch criado para o repositório remoto, configurando-o para rastrear o branch remoto de origin.
                              # Não é necessário especificar o nome do branch remoto ao fazer 'git pull' nesse branch.
git pull                # Puxa alterações do remoto para o branch atualmente verificado

# Adicionando/Removendo arquivos sob controle de versão
git rm <path/to/the/file>                 # Remove um arquivo e coloca a alteração em staging para ser commitada.
git mv <source/file> <destination/file>   # Move/renomeia um arquivo e coloca a alteração em staging para ser commitada.

# Alias - é possível criar aliases para comandos frequentemente utilizados
#   Isso é frequentemente feito para encurtar um comando ou adicionar flags padrão

# Adicionando um atalho "sw" para "switch"
git config --global alias.sw "switch"
# Uso:
git sw master     # Faz um "git switch master"

## Logging
git log --graph --oneline --all # Mostra um gráfico agradável dos commits anteriores
## Adicionando um alias chamado "lol" (log oneline..) que mostra o acima
git config --global alias.lol "log --graph --oneline --all"
## Usando o alias
git lol     # Faz um "git log --graph --oneline --all"
```

## Testando

Há um teste muito simples que você pode executar no PowerShell ou Bash. Ele está contido nos scripts test.sh e test.ps1.

### Limpeza

Você pode remover artefatos de teste, diretórios exercise, com o comando git clean:

```sh
git clean -ffdX
```

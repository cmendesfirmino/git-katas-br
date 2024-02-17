# Git Kata: Staging Básico

Este kata examinará a área de preparação  do git, que se chama staging, vamos utilizar o termo em inglês.

No git estamos trabalhando com três áreas diferentes:

* O **área de trabalho** onde você está fazendo suas alterações.
* A **área staging** onde todas as suas alterações são adicionadas quando você utiliza o comando `git add`.
* O repositório onde todos o histórico de commits vão. Para colocar suas alterações que estão na staging lá, utilizamos o comando `git commit`.

Um arquivo pode ter mudanças em ambas áreas, área de trabalho e staging, no mesmo tempo.
Estas alterações não precisam ser as mesmas.

Nós também vamos trabalhar com `git restore` para restaurar as alterações de um arquivo na staging, e `git checkout` para retornar um arquivo no estado anterior.

## Configuração

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## A Tarefa

Você está em seu próprio repositório. Há um arquivo chamado `file.txt`.

1. Qual é o conteúdo do arquivo `file.txt`?
2. Sobrescreva o conteúdo em `file.txt`: `echo 2 > file.txt` para mudar o estado do seu arquivo na **área de trabalho** (ou `sc file.txt '2'` no PowerShell)
3. O que `git diff` te diz?
4. O que `git diff --staged` te diz? Porque está vazio?
5. Execute `git add file.txt` para enviar ao stage suas alterações da **área de trabalho**.
6. O que `git diff` te diz?
7. O que `git diff --staged` te diz?
8. Sobrescreva o conteúdo em `file.txt`: `echo 3 > file.txt` para alterar o estado do seu arquivo no **área de trabalho**  (ou `sc file.txt '3'` no PowerShell).
9. O que `git diff` te diz?
10. O que `git diff --staged` te diz?
11. Explique o que está acontecendo
12. Execute `git status` e observe que `file.txt` está presente duas vezes na saída.
13. Execute `git restore --staged file.txt` para retirar a mudança da área de stage.
14. O que `git status` te diz agora?
15. Stage a mudança e faça um commit --> **Perceba que utilizamos o termo em inglês Stage com verbo, isso será sinônimo de utilizar o `git add`**
16. Como o log parece?
17. Sobrescreva o conteúdo em `file.txt`: `echo 4 > file.txt` (ou `sc file.txt '4'` no PowerShell)
18. Qual é o conteúdo de  `file.txt`?
19. O que `git status` nos diz?
20. Run `git restore file.txt`
21. Qual é o conteúdo de `file.txt`?
22. O que `git status` nos diz?

## Comandos Úteis

- `git add`
- `git commit`
- `git commit -m "My lazy short commit message"`
- `git log`
- `git log -n 5`
- `git log --oneline`
- `git log --oneline --graph`
- `git restore --staged`

## Aliases

Você pode definir alguns aliases como:
`git config --global alias.lol 'log --oneline --graph --all'`
Isso pode ser útil para você.

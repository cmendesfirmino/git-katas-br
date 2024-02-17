# Git Kata: Commits Básicos
Este kata irá apresentá-lo aos comandos `git add` e `git commit`.

Este é um kata muito introdutório, se você já usou extensivamente `git status`, `git log --oneline --graph`, `git add` e `git commit` você provavelmente pode pular.

Se ainda não fez a configuração inicial do Git, acesse esse conteúdo [Configuração Inicial Git](../configure-git/README.md)

## Configuração:

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## A Tarefa

1. Use `git status` para em qual branch vovê está.
2. Como `git log` está?
3. Crie um arquivo 💡**Dica**: Lembra do comando `touch`?
4. Como a saída do `git status` está agora?
5. `add` o arquivo para a área de staging
6. Como o `git status` está agora?
7. `commit` o arquivo para o repositório
8. Como o `git status` está agora?
9. Altere o conteúdo do arquivo que você acabou de criar 💡**Dica**: Lembra do comando `>>`?
10. Como o `git status` está agora?
11. `add` o arquivo alterado
12. Como o `git status` está agora?
13. Altere novamente o arquivo
14. Faça um `commit`
15. Como o `status` está agora? E o `log`?
16. Adicione e commit a nova alteração

## Comandos Úteis
- `git add`
- `git commit`
- `git commit -m "My commit message"`
- `git log`
- `git log -n 5`
- `git log --oneline`
- `git log --oneline --graph`
- `touch filename` para criar um arquivo (ou `sc filename ''` no PowerShell)
- `echo content > file` para sobrecrever o arquivo escrevendo *content* (ou `sc filename 'content'` no PowerShell)
- `echo content >> file` para adicionar ao arquivo escrevendo *content* (ou `ac filename 'content'` no PowerShell)

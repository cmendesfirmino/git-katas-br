# Visão geral dos Exercícios do Git Kata

## Status Tradução

Para verificar o status da tradução de cada item abaixo, consulte aqui [Status Tradução](Status%20Tradução.md)

## Setup

1. [configure-git](configure-git/README.md) - Se o git não estiver configurado, algumas passos básico para configurar

## Katas Básicos do Git na Ordem Sugerida

1. [basic-commits](basic-commits/README.md) - Primeiros passos com commits
2. [basic-staging](basic-staging/README.md) - Interagindo com o stage (index).
3. [basic-branching](basic-branching/README.md) - O primeiro passo para a ramificação (branch).
4. [ff-merge](ff-merge/README.md) -  Um passeio pelo merge mais trivial.
5. [3-way-merge](3-way-merge/README.md) - Um merge básico, envolvendo múltiplas branches divergentes.
6. [merge-conflict](merge-conflict/README.md) - Um merge básico entre branches que se divergem com conjuntos de alterações incompatíveis (mas simples).
7. [merge-mergesort](merge-mergesort/README.md) - Um conflito de merge com código
8. [rebase-branch](rebase-branch/README.md) - Utilizando rebase como alternativa ao merge.
9. [basic-revert](basic-revert/README.md) - Utilize o revert para reverter uma alteração.
10. [reset](reset/README.md) - Reset é um comando poderoso e um pouco perigoso se você não souber o que está fazendo. Passe pelos três modos de reset aqui.
11. [basic-cleaning](basic-cleaning/README.md) - Limpeza do espaço de trabalho.
12. [amend](amend/README.md) - Modificando commits anteriores.
13. [reorder-the-history](reorder-the-history/README.md) - Talvez tenhamos criado nossos commits em uma ordem inadequada, pratique corrigir esse cenário aqui.
14. [squashing](squashing/README.md) - Muitos commits pequenos são bons quando você está trabalhando localmente, mas para compartilhar seu código, pode ser mais benéfico entregar suas alterações de código em conjuntos maiores. Vá aqui para experimentar isso. Escreva um bom commit.
15. [advanced-rebase-interactive](advanced-rebase-interactive/README.md) - Pratique o uso dos comandos interativos de rebase.
16. [basic-stashing](basic-stashing/README.md) - O primeiro passo para fazer stash.
17. [ignore](ignore/README.md) - Os fundamentos do uso do arquivo .gitignore. E usando git rm.
18. [submodules](submodules/README.md) - Submódulos são odiados por muitos. Execute este exercício para entender o que está acontecendo.
19. [git-tag](git-tag//README.md) - Tags são convenientes para manter o controle de commits que aumentam um número de versão. Neste exercício, você irá listar, adicionar e excluir tags.

## Katas que resolvem problemas padrão

1. [commit-on-wrong-branch](commit-on-wrong-branch/README.md) - Se acidentalmente colocarmos commits não enviados no branch errado, como podemos efetivamente movê-los para outro branch antes do nosso trabalho nesse branch.
2. [commit-on-wrong-branch-2](commit-on-wrong-branch-2/README.md) - Outro exercício sobre o que fazer se você tiver cometido acidentalmente no branch errado.
3. [reverted-merge](reverted-merge/README.md) -  Revertemos um merge, mas, após correções serem adicionadas ao branch mesclado, queremos as alterações do merge e as novas correções.
4. [save-my-commit](save-my-commit/README.md) - Se você deletar acidentalmente ou intencionalmente um commit, vá aqui para tentar salvá-lo. Você usará o reflog.
5. [detached-head](detached-head/README.md) - O Git reclama que você está em um "You are in 'detached HEAD' state". O que fazer?


## Katas Sobre Recursos Avançados

1. [git-attributes](git-attributes/README.md) - O arquivo .gitattributes permite que você especifique como o Git lida com arquivos, como terminações de linha em arquivos de texto ou como diferenciar um arquivo binário.
2. [Bad-commit](bad-commit/README.md) - Usando git bisect para encontrar um commit ruim.
3. [bisect](bisect/README.md) - Outro kata usando git bisect.
4. [pre-push](pre-push/README.md) - Um exercício rápido sobre o uso dos hooks do Git.
5. [Investigation](investigation/README.md) - Descubra o que está acontecendo em um repositório Git, entenda como é sob o capô.
6. [Objects](objects/README.md) - Um pequeno exercício sobre os internos do Git.
7. [merge-driver](merge-driver/README.md) - Definindo um driver de merge personalizado.
8. [rebase-exec](rebase-exec/README.md) - Execute testes em cada commit usando git rebase --exec

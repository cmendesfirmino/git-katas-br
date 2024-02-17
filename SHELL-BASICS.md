# Guia de Sobrevivência do Shell

## Diretórios
Todos diretórios iniciam com `/`

No Windows o drive C: é assim `/c/`

A pasta inicial do seu usuário é `/c/users/myname`

`~` serve como um atalho para sua pasta inicial, então:

`~/projects` equivale à `/c/users/myname/projects`

`.` é o diretório atual.

`..` é um diretório acima (pai).

## Imprimir no Terminal o Diretório de Trabalho
`pwd`

Output:
`/c/users/myname`

## Lista de Conteúdos de Uma Pasta
`ls` (lista arquivos)

`ls -l` (lista arquivos em forma longa)

`ls -a` (lista todos arquivos, incluindo os ocultos)

## Alterar Diretório
`cd <nome_arquivo>`

`cd ..` (vá para um diretório acima)

`cd project` (vá para o diretório __project__)

## Trabalhando com Arquivos

`cat file.txt` imprime no termial o conteúdo do arquivo *file.txt*

`less file.txt` imprime no terminal o conteúdo do arquivo *file.txt* com paginação. Para sair pressione `q`.

`echo "Hello world" > file.txt`
Escreva a string __Hello World__ em um arquivo chamado *file.txt* no diretório atual, sobrescrevendo o conteúdo atual do arquivo se tiver, ou criando um novo arquivo.

`echo "More stuff" >> file.txt` adiciona **More stuff** no final do arquivo *file.txt* em uma nova linha.

`touch file.txt`
Cria um arquivo vazio. Se `file.txt` existir, somente irá atualizar com a data e hora atual. 


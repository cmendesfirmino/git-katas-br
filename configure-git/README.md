# Git Kata: Configurando o Git

Este kata não tem um script `setup.sh`. Basta ler e seguir.

## Download e Instalação 

### Windows

* Faça Download em [https://git-scm.com/download/win](https://git-scm.com/download/win) (ou use [Chocolatey](https://chocolatey.org/))
* Instale utilizando as configurações padrões
* Após a instalação, abra o Git Bash para seguir com as etapas de configuração abaixo.

### Linux - Ubuntu
* Abra o terminal e siga os comandos
```bash
sudo apt update
sudo apt install git
```

### Leia mais
Caso tenha algum outro sistema operacional, neste link você deve encontrar. 
[Instalação Git](https://github.com/git-guides/install-git)


## Git Configuração Inicial

O Git deseja saber quem deve ser registrado como o autor das alterações, etc. Para fazer isso, configure o nome de usuário e o endereço de e-mail do usuário no Git com os seguintes comandos:

1. `git config --global user.name "John Doe"`
2. `git config --global user.email "johndoe@example.com`

### Configuração do editor

Às vezes, o Git precisa que você edite um arquivo que ele cria, por exemplo, a mensagem de um commit que você cria. Como padrão, o Git é configurado com VIM, mas tem uma curva de aprendizado acentuada, então talvez seja melhor usar outra ferramenta de sua preferência:

Se você quiser usar o editor Nano baseado em CLI:
- `git config --global core.editor nano`

Para a galera do Windows pode usar o famoso Bloco de Notas:
- `git config --global core.editor notepad`

Ou outras ferramentas que já seja familiar:
- `git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`
- `git config --global core.editor "atom --wait"`
- `git config --global core.editor "code --wait"`

### Aliases (Apelidos)

Para facilitar sua vida, você pode definir aliases como exemplo:
* `git config --global alias.lol 'log --oneline --graph --all'`

Isso pode ser muito útil quando desejamos ver o comando Git graph
Cole no seu terminal e tente com `git lol`.

Outros aliases podem ser encontrado no kata alias.


### Autenticação SSH
Um recurso muito útil, pois em repositórios privados só conseguimos interagir logado, e uma das formas é via SSH.

- Veja https://help.github.com/articles/generating-an-ssh-key para detalhes sobre autenticação em repositórios com SSH habilitados
- Ou execute `ssh-keygen` para gerar um par de chaves SSH `%USERPROFILE%/.ssh/`:

  `ssh-keygen -t rsa -b 4096 -C "johndoe@example.com"`

  Isto gera uma chave pública e uma privada chavamada `id_rsa.pub`/`id_rsa`, respectivamente
- A chave pública `id_rsa.pub` precisa ser enviada para seu servidor de repositório:
  - Para GitHub, está em _Settings_ -> _SSH and GPG keys_
  - Para BitBucket, está em _Manage Account_ -> _SSH Keys_

🔥**IMPORTANTE**
 - **NUNCA** compartilhe a sua chave privada `id_rsa`, este arquivo deve ficar na sua máquina.
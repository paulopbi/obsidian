#git #cli #configuração

## Configuração Inicial

Depois de fazer a instalação do #git é importante fazer as configurações iniciais como definir nome de usuário, email, ao configurar o nome e email estaremos informando o git qual é o usuário que está fazendo o commit:

```bash
git config --global user.name "Paulo Victor" # configura o nome
git config --global user.email paulovictor@email.com # configura o email

git config --list # irá exibir todas as configurações do git
```

> [!NOTE] Essa configuração de email e usuário é feita apenas uma vez!

## Configuração de Branch

Podemos configurar a branch padrão do #git, isso irá evitar conflitos ou nomes de branch desatualizados, o padrão do git é o _"master"_ porém essa nomeação de branch é antiga, as branch's atuais são chamadas de _"main"_, dito isso, podemos configurar com o seguinte comando: 

```bash
git config --global init.defaultBranch <name>
```

## Ajuda

Se você precisar de ajuda para usar o Git, há três formas de acessar a página do manual de ajuda (_manpage_) para qualquer um dos comandos Git:

```bash
# comandos de ajuda
git help <verbo>
git <verbo> --help
man git -<verbo>

# exemplo
git help config # mostra as opções de config
```
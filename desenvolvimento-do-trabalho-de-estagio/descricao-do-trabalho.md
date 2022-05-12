# Descriçāo do Trabalho

## Criaçāo de um novo ambiente de trabalho no macOS

Inicialmente surgiram alguns conflitos, porque iniciei o trabalho em um utilizador já existente no macOS, onde várias ferramentas já estariam configuradas com o respetivo utilizador, dai surgirem os conflitos quando tentei configurar essas mesmas com as minhas credenciais. Por exemplo no SourceTree, uma das ferramentas essenciais para o meu projeto, foi necessário configurá-la com a minha conta do GitHub, para posteriormente fazer um pull request em meu nome das alterações feitas no projeto, surgindo ai conflitos relacionados com permissões do usário do macOS em que me encontrava.

Foram necessários os seguintes passos para criar um novo ambiente de trabalho, para evitar novamente futuros conflitos:

### Criaçāo de um novo user no macOS como admin

### Dar permissões no SSD ao novo user

### Setups de todas as ferramentas necessárias para o desenvolvimentos do projeto nomeadamente:

#### Chrome

Organizaçāo todas as tabs recorrentes, como por exemplo o ClickUp;

#### Slack

Login na conta

#### UnityHub

Instalaçāo da versāo correta para o projeto

Login e abertura do projeto

#### SourceTree

Login com a conta do GitHub, utilizando a respetiva chave SHH da conta

Abertura do repositório TunnyStones que já se encontra no SSD

Instalação do “homebrew” a partir do terminal

Instalação do “git-lfs” a partir do terminal do SorceTree

Git-lfs pull

Verificaçāo do estado do repositório através da linha de comandos para verificar se não                existem  comits pendentes($git status)

#### Rider

Activaçāo da licença do Rider a partir das credencias já existentes

Abertura do projeto TunnyStones

## Criaçāo e Configuracao da SSH key

Para ser possivel a criaçāo de pull requests para o repositório do projeto, foi necessáio configurar o SourceTree com a conta pessoal do GitHub e respetiva SSH key, e para isso foi necessário gerar uma seguindo os proximos passos.

### Abrir o terminal e introduzir os seguintes comandos&#x20;

#### Para criar a SSH key

```shell
$ ssh-keygen -t ed25519 -C "your_email@example.com"
```

&#x20; Se estivermos a usar um "Legacy System" que nao suporta o algoritmo Ed25519

```shell
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

#### Adicionar a SSH key ao ssh-agent

```shell
$ eval "$(ssh-agent -s)"
```

### Configurar a minha conta do GitHub com a SSH key

Nas configuracões do github, foi necessário adicionar a nova SSH key gerada, e para isso bastou:&#x20;

* No Finder <img src="https://help.apple.com/assets/61D4C1B5425F2576373C512A/61D4C1B7425F2576373C5132/pt_PT/058e4af8e726290f491044219d2eee73.png" alt="" data-size="line">, selecionar Go > Go to Folder > Macintosh HD, abrir o user no qual a sessāo está iniciada, visualizar os ficheiros ocultos (Cmd+ Shift + <img src="../.gitbook/assets/computer_key_Greater_than_Period.png" alt="" data-size="line">) , e obter a SHH key publica .

#### Introduzir no terminal&#x20;

```shell
$ ssh-add "private SSH key"
```

## Criaçāo da wind animation e hook up da mesma no projeto

### Criaçāo da wind animation

#### Ajuste dos frames do sprite, para a criaçāo da animaçāo

![ Sprite de exemplo utilizada no projeto em questāo](<../.gitbook/assets/Screenshot 2022-05-12 at 11.19.57.png>)

#### Criaçāo da animaçāo e implementaçāo da mesma no projeto

![Criaçāo de um objeto para implementar implementar a animaçāo](../.gitbook/assets/AnimatonImpl.png)

#### &#x20;
